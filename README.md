# uriparse-rs

[![LICENSE](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Build Status](https://travis-ci.org/sgodwincs/uriparse-rs.svg?branch=master)](https://travis-ci.org/sgodwincs/uriparse-rs)
[![Crates.io Version](https://img.shields.io/crates/v/uriparse.svg)](https://crates.io/crates/uriparse)

Implementation of [RFC3986](https://tools.ietf.org/html/rfc3986) including URIs and URI references.

[Documentation](https://docs.rs/uriparse/)

# Normalization

No normalization is done on any parsed URIs. This needs to be done separately if desired. Specifically, this includes percent encoding normalization, path segment normalization (i.e. `.` and `..` are not handled), and any scheme/protocol-based normalization.

# Equality

Equality of URIs or URI references is based on percent encoding normalization, though the original strings are never normalized directly. Case-sensitivity of equality depends on each specific part (e.g. the host is case-insensitive).
