# Release process

This is a proposed workflow, not authorization to publish.

1. Keep development, CI, keys, customer data, and build logs in private systems. Build the approved source revision in an isolated, recorded build environment. Record source revision and dirty status, dependencies, toolchain, and artifact hashes. Review provenance and the final package contents.
2. Adopt customer terms and review third-party licenses and all GPL source obligations. Include matching notices and source. Inspect archives, executable signatures, network destinations, sample data, and secrets. Do not include a real user's profile or ownership file.
3. Build and Authenticode-sign a direct-download Windows package with a trusted timestamp. Test the exact signed package on clean supported Windows installations, including install, upgrade, uninstall, missing WebView2, activation, and recovery as practical. Confirm the Personal purchase and restore paths and any paid-service terms without initiating real charges during automation.
4. Prepare release notes, a SHA-256 checksum file, GPL source, and an artifact manifest. Public release attestations protect published assets but do not by themselves prove which private source produced the binaries; retain separately verifiable private CI build provenance. Protect signing keys and restrict release permissions.
5. Obtain explicit owner approval of the exact repository tree, notes, assets, checksums, and version. Only then create a separate public repository and draft release. Enable GitHub immutable releases when available, attach all approved assets, recheck them, and publish the draft. Do not make the development repositories public.

If any asset changes after approval, obtain approval again. Store-submission MSIX files are not substitutes for a signed, independently installable direct-download package.
