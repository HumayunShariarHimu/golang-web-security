# golang-web-security

> A curated and organized collection of resources related to **golang-web-security**.


# Golang Web Security

Secure Golang web app with best practices: authentication, authorization, input validation, CSRF protection, and secure headers. Example code for secure development.



## Table of Contents
- [Tools](#tools)
  - [Web Framework Hardening](#web-framework-hardening)
  - [Security Libraries](#security-libraries)
  - [Static Code Analysis](#static-code-analysis)
  - [Vulnerabilities and Security Advisories](#vulnerabilities-and-security-advisories)
  - [Private Key Infrastructure](#private-key-infrastructure)
- [Educational](#educational)
  - [Hacking Playgrounds](#hacking-playgrounds)
  - [Articles, Guides & Talks](#articles-guides--talks)
  - [Reporting Bugs](#reporting-bugs)
- [License](#license)

# Tools

## Web Framework Hardening

*Middleware and utilities to secure your Go web applications at the framework level.*

- [nosurf](https://github.com/justinas/nosurf) - CSRF protection middleware for Go.
- [gorilla/csrf](https://github.com/gorilla/csrf) - Provides Cross-Site Request Forgery (CSRF) prevention middleware for Go web applications & services.
- [gorilla/securecookie](https://github.com/gorilla/securecookie) - Encodes and decodes authenticated and optionally encrypted cookie values for Go web applications.
- [secure](https://github.com/unrolled/secure) - Secure is an HTTP middleware for Go that facilitates most of your security needs for web applications (e.g., HSTS, CSP, etc.).
- [unindexed](https://github.com/jordan-wright/unindexed) - A drop-in replacement for `http.Dir` which disables directory indexing.
- [beego-security-headers](https://github.com/gosecguy/beego-security-headers) - Beego framework filter for easy security headers management.
- [echox/sessions](https://github.com/labstack/echo-contrib/tree/master/sessions) - Secure cookie-based session management for the Echo framework.
- [gin-contrib/secure](https://github.com/gin-contrib/secure) - A Gin middleware for quick implementation of security headers.

## Security Libraries

*General-purpose libraries for implementing specific security controls.*

- [paseto](https://github.com/o1egl/paseto) - Platform-Agnostic Security Tokens implementation in GO (Golang).
- [hsts](https://github.com/StalkR/hsts) - Go HTTP Strict Transport Security library.
- [jwt-go](https://github.com/dgrijalva/jwt-go) - Golang implementation of JSON Web Tokens (JWT). (Note: This library is now archived; it's recommended to look at [golang-jwt/jwt](https://github.com/golang-jwt/jwt) instead).
- [golang-jwt/jwt](https://github.com/golang-jwt/jwt) - A community-maintained fork of the popular `jwt-go` library.
- [httprobe](https://github.com/tomnomnom/httprobe) - Take a list of domains and probe for working HTTP and HTTPS servers (useful for recon).
- [bcrypt](https://pkg.go.dev/golang.org/x/crypto/bcrypt) - The official Go implementation of bcrypt for password hashing.
- [scrypt](https://pkg.go.dev/golang.org/x/crypto/scrypt) - The official Go implementation of the scrypt key derivation function.
- [argon2](https://pkg.go.dev/golang.org/x/crypto/argon2) - The official Go implementation of the Argon2 key derivation function (password hashing).
- [acmetool](https://github.com/hlandau/acme) - An easy-to-use command-line tool for automatically getting TLS certificates from Let's Encrypt.

## Static Code Analysis

*Tools to analyze your source code for potential security flaws.*

- [safesql](https://github.com/stripe/safesql) - Static analysis tool for Golang that protects against SQL injections. It does not seem to be actively maintained at the moment.
- [gosec](https://github.com/securego/gosec) - Inspects source code for security problems by scanning the Go AST and matching it with a set of rules. Comes bundled in a Docker container [securego/gosec](https://hub.docker.com/r/securego/gosec).
- [gometalinter](https://github.com/alecthomas/gometalinter) - Concurrently runs most of the existing go linters and normalizes their output. (Consider using [golangci-lint](https://github.com/golangci/golangci-lint) as a more modern and faster alternative).
- [golangci-lint](https://github.com/golangci-lint/golangci-lint) - A fast Go linters runner. It runs many linters in parallel, including `gosec`, and can be integrated into your CI/CD pipeline.
- [CodeQL](https://securitylab.github.com/tools/codeql) - A tool that lets you query your code like data, in order to find vulnerabilities and bugs. See also [LGTM.com](https://lgtm.com) for pull request integration and running queries in the cloud. (Note: LGTM.com has been sunset, but CodeQL remains available).
- [ChainJacking](https://github.com/Checkmarx/chainjacking) - Find which of your Go lang direct GitHub dependencies is susceptible to ChainJacking attack.
- [Semgrep](https://semgrep.dev/) - A fast, open-source static analysis tool that supports Go and can be used to find security issues by writing custom rules.

## Vulnerabilities and Security Advisories

*Sources for staying informed about known vulnerabilities in Go and its ecosystem.*

- [golang-announce](https://groups.google.com/forum/#!forum/golang-announce) - The golang release mailing list. Language-specific security issues are announced here.
- [Go Vulnerability Database](https://vuln.go.dev/) - The official Go vulnerability database, maintained by the Go team.
- [GoCenter Security](https://jfrog.com/blog/gocenter-reveals-go-module-vulnerabilities-with-xray/) and [JFrog VSCode Extension for Go](https://marketplace.visualstudio.com/items?itemName=JFrog.jfrog-vscode-extension) - Free vulnerability data around Go Modules.
- [snyk Vulnerability DB](https://snyk.io/vuln?type=golang) - Commercial but free listing of known vulnerabilities in libraries.
- [Common Vulnerabilities and Exposures](https://www.cvedetails.com/vulnerability-list/vendor_id-14185/Golang.html) - Vulnerabilities that were assigned a CVE. Covers the language and packages.
- [National Vulnerability Database](https://nvd.nist.gov/vuln/search/results?form_type=Basic&results_type=overview&query=golang&search_type=all) - Golang known vulnerabilities in the National Vulnerability Database.
- [OSV.dev](https://osv.dev/list?q=golang) - A distributed vulnerability database for open source, with good support for Go.

## Private Key Infrastructure

*Tools for managing certificates and PKI.*

- [CloudFlare SSL](https://github.com/cloudflare/cfssl) - CFSSL is CloudFlare's PKI/TLS swiss army knife. It is both a command line tool and an HTTP API server for signing, verifying, and bundling TLS certificates.
- [step-ca](https://github.com/smallstep/certificates) - A private certificate authority (CA) and ACME server for secure automated certificate management.

# Educational

## Hacking Playgrounds

*Intentionally vulnerable applications to practice security testing and exploitation in Go.*

- [govwa](https://github.com/0c34/govwa) - A vulnerable golang application including the most common vulnerabilities found in web applications today.
- [Lambhack](https://github.com/wickett/lambhack) - A very vulnerable serverless application in AWS Lambda.
- [go-dvwa](https://github.com/eze-kiel/go-dvwa) - A Go version of the popular Damn Vulnerable Web Application (DVWA).
- [gin-vulnerable](https://github.com/bloom42/gin-vulnerable) - An intentionally vulnerable API built with the Gin framework for educational purposes.

## Articles, Guides & Talks

*Presentations, written guides, and example projects for secure Go development.*

- [gosea](https://github.com/komand/gosea) - Go Secure Example Application (GOSEA).
- [Go - Secure Coding Practices](https://www.owasp.org/images/2/2b/Owasp-171123063052.pdf) by OWASP - [PDF] Talk given by Sulhaedir at the OWASP Jakarta meetup.
- [OWASP Go - Secure Coding Practices](https://github.com/OWASP/Go-SCP) by Checkmarx - Go programming language secure coding practices guide.
- [Memory Security in golang](https://cryptolosophy.org/memory-security-go/) - Handling data securely in memory.
- [golang-tls](https://github.com/denji/golang-tls) - Simple Golang HTTPS/TLS Examples.
- [Hacking with Go](https://github.com/parsiya/Hacking-with-Go) - Hacking with Go for security professionals.
- [ReDoS in Go](https://www.checkmarx.com/2018/05/07/redos-go/) by Checkmarx - Diving Deep into Regular Expression Denial of Service (ReDoS) in Go.
- [Attacking Go](https://blog.trailofbits.com/2019/11/07/attacking-go-vr-ttps/): A detailed description on Security assessment techniques for Go projects.
- [The IoC of Go Generics](https://www.arp242.net/go-generics.html) - A discussion on how generics impact code clarity and potential security implications.

## Reporting Bugs

- [Go Security Policy](https://golang.org/security) - How to responsibly report security issues to the Go team.

# License

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](http://creativecommons.org/publicdomain/zero/1.0/)


---

**golang-web-security** — Represented By [Humayun Shariar Himu](https://github.com/HumayunShariarHimu)

*A Passionated Psychologist & Tech Lover*

### Connect

- [GitHub](https://github.com/HumayunShariarHimu)
- [YouTube](https://youtube.com/@HumayunShariarHimu)
- [Facebook](https://www.facebook.com/humayunshariarhimu)
- [CodePen](https://codepen.io/HumayunShariarHimu)
- [Google Bug Hunters](https://bughunters.google.com/profile/b97693e9-aa31-4451-9c65-f7548e85bfc9)
