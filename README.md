# frameworks-automation-chart

Toy stand-in for `rancher/charts` in the release-automation playground.

In production this repo holds embedded helm charts that rancher consumes;
tags of upstream components like `webhook` and `remotedialer-proxy` produce
helm-chart artifacts that need to land here on the matching `dev-v<rancher-minor>`
branch before rancher can be bumped to the new component version.

For playground purposes this is modelled as a Go module so the same bumper
can drive it. No releases of its own — branches are continuously updated.

Branch layout mirrors rancher's minor lines:

| Branch     | Matching Rancher |
|------------|------------------|
| dev-v2.16  | main             |
| dev-v2.13  | release/v2.13    |
