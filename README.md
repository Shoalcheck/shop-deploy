# shop-deploy

The manifests the shop's payments service is deployed from, and the gate every pull request passes first.

`.github/workflows/shoalcheck.yml` builds a cluster from `main`, then lays the pull request's manifests over a
read-only reading of it with `shoalcheck gate --with`. Nothing is applied: the gate says what the change would add,
and the pull request cannot merge while it reports a new critical or high finding.

A demo repository for [Shoalcheck](https://shoalcheck.com).
