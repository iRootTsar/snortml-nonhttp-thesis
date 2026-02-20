SnortML non-HTTP thesis workspace

Goal
Extend SnortML to support ML-based detection for non-HTTP traffic in a way that is practical for IDS and IPS use. The work explores how additional protocol data can be provided to the ML inspector and evaluates prototype binary models using public PCAPs with offline PCAP analysis and realistic constraints in mind.

Repository layout
docs/        Documentation, setup notes, experiment logs
scripts/     Build and run scripts, dataset handling, evaluation
configs/     Snort configs, inspector configs, experiment configs
metadata/    Dataset references, hashes, labeling rules, versions
results/     Metrics, plots, tables, summarized outputs
samples/     Optional small allowed sample inputs
external/    Optional pinned source repos (submodules) or pointers

Setup
Read docs/installation_manual.md or docs/installation_manual.pdf first.
The build installs Snort 3, LibDAQ, and LibML into an isolated prefix:
~/snortml-research/install

Reproducibility
This repo does not store full datasets or PCAPs. Use scripts under scripts/ and references under metadata/.
Record exact commit hashes for snort3, libml, libdaq in docs/versions.md.

Quick verify
Run the verification script after building:
~/snortml-research/scripts/verify_install.sh
