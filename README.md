# Meibel published policies

The terms, policies and price list Meibel publishes on [meibel.ai](https://www.meibel.ai), every version, as
published. This repository is a public record: it only ever receives approved versions that are public on the
website (or announced to customers ahead of their effective date), and nothing in it is ever changed or removed.
A correction is a new version with a new effective date.

## Layout

    pages/<page>/<effective-date>/
        index.md          the page's text, as published
        index.html        the same text as HTML
        release.json      what it is, where it is published, who approved it, SHA-256 of each file
        timestamp.tsr     RFC 3161 timestamp (FreeTSA) over release.json
        timestamp.ots     OpenTimestamps proof over release.json (timestamp.bitcoin.ots once anchored in Bitcoin)
        notice.md         for a change announced ahead of its date: the notice as sent
        effective.json    added when an announced change takes effect (with its own .tsr and .ots)
        withdrawal.json   added if an announced change is withdrawn (with its own .tsr and .ots)
        captured.html     for a page published before this record began: the page as served when captured

Each version is tagged `<page>/<effective-date>`. The newest effective date on or before today is the version in
force. `release.json` also gives an Internet Archive snapshot of the live page.

## Verifying a version

    sha256sum pages/<page>/<date>/index.md                 # compare with "files" in release.json
    openssl ts -verify -data release.json -in timestamp.tsr \
        -CAfile cacert.pem -untrusted tsa.crt              # FreeTSA certificates: https://freetsa.org
    ots verify -f release.json timestamp.bitcoin.ots       # https://opentimestamps.org

The timestamps prove the record existed, unchanged, by the time shown, independently of Meibel and of GitHub.

## Notice

Copyright meibel.ai Inc. Published for reference. The text is not licensed for reuse.
