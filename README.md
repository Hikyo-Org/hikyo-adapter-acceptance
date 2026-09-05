# Hikyo GitHub adapter acceptance fixture

Dedicated nonproduction repository for the Hikyo GitHub adapter contract.
The workflow is copied byte-for-byte from the public Hikyo test fixture. It
accepts synthetic test names and publishes only SHA-256 hashes of consumed
values. Do not store production secrets in this repository or its environment.

The `contract` environment permits deployments from `main` without manual
review. Tests create uniquely prefixed `HIKYO_CONTRACT_` secrets and variables
and remove their own values afterward. The protected environment is retained
so tests can verify that a settings-free environment PUT preserves its policy.

Minimum-permission and deliberately insufficient credentials are supplied to
the external test runner; they are never committed here.
