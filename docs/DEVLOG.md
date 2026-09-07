# Release preparation

2026-09-06: Prepared a portable setup recipe from accepted framework `63446a28111a21a0cb7e8b5106c3614c898fc4b5`.
The release snapshot keeps functional code and title seed bytes, adds the bounded setup backport, and excludes private input/history.
Consulted the local release process, PSX-PUB-016, the accepted title handoff, and [Git orphan-branch documentation](https://git-scm.com/docs/git-checkout).
The shared archive gate now accepts only exact hashes for two intentional SDK path-example files; changed and relocated fixtures still fail.
Native CI and Windows package acceptance are pending.

2026-09-07: Native canary gates required the existing PSX-BUILD-024 C-linkage correction and the exact public recomp-ui be8ac1d portable tool text fix. The package now carries all four complete public dependency identities (PSX-PUB-027). No game runtime behavior or recipe settings changed in this update. Native build and package checks remain required.

2026-09-07: Canonical12-track setup verified its disc digest, then rejected the lowercase boot filename retained by the old Windows-only recipe. The actual ISO9660 entry is SCUS_943.51. Portable EXE and generated-file names now use that exact case. This is the PSX-TOOL-011 path-identity boundary; no retail bytes, seed tokens, or runtime settings changed. Verify-disc and reader mapping had already passed; preparation and the final source build are rerun.
