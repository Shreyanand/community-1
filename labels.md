# Open Services Group GitHub Labels

## Table of Contents

- [Intro](#intro)
  - [Why these labels?](#why-these-labels)
  - [How do I add a new label?](#how-do-i-add-a-new-label)
- [Labels that apply to all repos, for both issues and PRs](#labels-that-apply-to-all-repos-for-both-issues-and-prs)
- [Labels that apply to all repos, only for issues](#labels-that-apply-to-all-repos-only-for-issues)
- [Labels that apply to all repos, only for PRs](#labels-that-apply-to-all-repos-only-for-prs)
- [Labels that apply to open-services-group/community, for both issues and PRs](#labels-that-apply-to-open-services-groupcommunity-for-both-issues-and-prs)
- [Labels that apply to open-services-group/okr, for both issues and PRs](#labels-that-apply-to-open-services-groupokr-for-both-issues-and-prs)


## Intro

This file was auto generated by the [label_sync](https://git.k8s.io/test-infra/label_sync/) tool,
based on the [labels.yaml](./labels.yaml) file that it uses to
sync github labels across repos in the [Open Services Group github org](https://github.com/open-services-group)

### Why these labels?

The rule of thumb is that labels are here because they are intended to be produced or consumed by
our automation (primarily prow) across all repos. There are some labels that can only be manually
applied/removed, and where possible we would rather remove them or add automation to allow a
larger set of contributors to apply/remove them.

### How do I add a new label?

- Add automation that consumes/produces the label
- Open a PR, _with a single commit_, that:
  - updates [labels.yaml](./labels.yaml) with the new label(s)
  - runs `label_sync` (to regenerate the label descriptions and associated CSS)
- After the PR is merged, a prow job is responsible for syncing labels

You can run `label_sync` in a container using:

```sh
podman run --rm -v ./:/community:z \
       gcr.io/k8s-prow/label_sync:latest \
       --action docs \
       --config /community/labels.yaml \
       --docs-template /community/labels.md.tmpl \
       --docs-output /community/labels.md
```


## Labels that apply to all repos, for both issues and PRs

| Name | Description | Added By | Prow Plugin |
| ---- | ----------- | -------- | --- |
| <a id="committee/steering" href="#committee/steering">`committee/steering`</a> | Denotes an issue or PR intended to be handled by the steering committee.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/bug" href="#kind/bug">`kind/bug`</a> | Categorizes issue or PR as related to a bug. <br><br> This was previously `bug`, | anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/cleanup" href="#kind/cleanup">`kind/cleanup`</a> | Categorizes issue or PR as related to cleaning up code, process, or technical debt.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/demo" href="#kind/demo">`kind/demo`</a> | This is an Issue or PR someone want to give a demo or request a demo.| human |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/deprecation" href="#kind/deprecation">`kind/deprecation`</a> | Categorizes issue or PR as related to a feature/enhancement marked for deprecation.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/documentation" href="#kind/documentation">`kind/documentation`</a> | Categorizes issue or PR as related to documentation.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/feature" href="#kind/feature">`kind/feature`</a> | Categorizes issue or PR as related to a new feature. <br><br> This was previously `enhancement`, `kind/enhancement`, | anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/question" href="#kind/question">`kind/question`</a> | Categorizes issue or PR as a support question. <br><br> This was previously `close/support`, `question`, `triage/support`, | humans | |
| <a id="lifecycle/active" href="#lifecycle/active">`lifecycle/active`</a> | Indicates that an issue or PR is actively being worked on by a contributor. <br><br> This was previously `active`, | anyone |  [lifecycle](https://git.k8s.io/test-infra/prow/plugins/lifecycle) |
| <a id="lifecycle/frozen" href="#lifecycle/frozen">`lifecycle/frozen`</a> | Indicates that an issue or PR should not be auto-closed due to staleness. <br><br> This was previously `keep-open`, | anyone |  [lifecycle](https://git.k8s.io/test-infra/prow/plugins/lifecycle) |
| <a id="lifecycle/rotten" href="#lifecycle/rotten">`lifecycle/rotten`</a> | Denotes an issue or PR that has aged beyond stale and will be auto-closed.| anyone |  [lifecycle](https://git.k8s.io/test-infra/prow/plugins/lifecycle) |
| <a id="lifecycle/stale" href="#lifecycle/stale">`lifecycle/stale`</a> | Denotes an issue or PR has remained open with no activity and has become stale. <br><br> This was previously `stale`, | anyone |  [lifecycle](https://git.k8s.io/test-infra/prow/plugins/lifecycle) |
| <a id="priority/awaiting-more-evidence" href="#priority/awaiting-more-evidence">`priority/awaiting-more-evidence`</a> | Lowest priority. Possibly useful, but not yet enough support to actually get it done.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="priority/backlog" href="#priority/backlog">`priority/backlog`</a> | Higher priority than priority/awaiting-more-evidence.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="priority/critical-urgent" href="#priority/critical-urgent">`priority/critical-urgent`</a> | Highest priority. Must be actively worked on as someone's top priority right now.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="priority/important-longterm" href="#priority/important-longterm">`priority/important-longterm`</a> | Important over the long term, but may not be staffed and/or may need multiple releases to complete.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="priority/important-soon" href="#priority/important-soon">`priority/important-soon`</a> | Must be staffed and worked on either currently, or very soon, ideally in time for the next release.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="sig/community-experience" href="#sig/community-experience">`sig/community-experience`</a> | Denotes an issue or PR relevant to SIG Community Experience.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="sig/data-science" href="#sig/data-science">`sig/data-science`</a> | Denotes an issue or PR relevant to SIG Data Science.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="sig/services" href="#sig/services">`sig/services`</a> | Denotes an issue or PR relevant to SIG Services.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="triage/duplicate" href="#triage/duplicate">`triage/duplicate`</a> | Indicates an issue is a duplicate of other open issue. <br><br> This was previously `close/duplicate`, `duplicate`, | humans | |
| <a id="triage/needs-information" href="#triage/needs-information">`triage/needs-information`</a> | Indicates an issue needs more information in order to work on it. <br><br> This was previously `close/needs-information`, | humans | |
| <a id="triage/not-reproducible" href="#triage/not-reproducible">`triage/not-reproducible`</a> | Indicates an issue can not be reproduced as described. <br><br> This was previously `close/not-reproducible`, | humans | |
| <a id="triage/unresolved" href="#triage/unresolved">`triage/unresolved`</a> | Indicates an issue that can not or will not be resolved. <br><br> This was previously `close/unresolved`, `invalid`, `wontfix`, | humans | |
| <a id="wg/byon-build-pipelines" href="#wg/byon-build-pipelines">`wg/byon-build-pipelines`</a> | Categorizes an issue or PR as relevant to WG BYON Build Pipelines.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="wg/devsecops" href="#wg/devsecops">`wg/devsecops`</a> | Categorizes an issue or PR as relevant to WG DevSecOps| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="¯\_(ツ)_/¯" href="#¯\_(ツ)_/¯">`¯\_(ツ)_/¯`</a> | ¯\\\_(ツ)_/¯| humans |  [shrug](https://git.k8s.io/test-infra/prow/plugins/shrug) |

## Labels that apply to all repos, only for issues

| Name | Description | Added By | Prow Plugin |
| ---- | ----------- | -------- | --- |
| <a id="epic" href="#epic">`epic`</a> | Tags an issue as an Epic.| humans | |
| <a id="tide/merge-blocker" href="#tide/merge-blocker">`tide/merge-blocker`</a> | Denotes an issue that blocks the tide merge queue for a branch while it is open. <br><br> This was previously `merge-blocker`, | humans | |

## Labels that apply to all repos, only for PRs

| Name | Description | Added By | Prow Plugin |
| ---- | ----------- | -------- | --- |
| <a id="approved" href="#approved">`approved`</a> | Indicates a PR has been approved by an approver from all required OWNERS files.| approvers |  [approve](https://git.k8s.io/test-infra/prow/plugins/approve) |
| <a id="do-not-merge/blocked-paths" href="#do-not-merge/blocked-paths">`do-not-merge/blocked-paths`</a> | Indicates that a PR should not merge because it touches files in blocked paths.| prow |  [blockade](https://git.k8s.io/test-infra/prow/plugins/blockade) |
| <a id="do-not-merge/hold" href="#do-not-merge/hold">`do-not-merge/hold`</a> | Indicates that a PR should not merge because someone has issued a /hold command.| anyone |  [hold](https://git.k8s.io/test-infra/prow/plugins/hold) |
| <a id="do-not-merge/invalid-owners-file" href="#do-not-merge/invalid-owners-file">`do-not-merge/invalid-owners-file`</a> | Indicates that a PR should not merge because it has an invalid OWNERS file in it.| prow |  [verify-owners](https://git.k8s.io/test-infra/prow/plugins/verify-owners) |
| <a id="do-not-merge/work-in-progress" href="#do-not-merge/work-in-progress">`do-not-merge/work-in-progress`</a> | Indicates that a PR should not merge because it is a work in progress.| prow |  [wip](https://git.k8s.io/test-infra/prow/plugins/wip) |
| <a id="hacktoberfest-accepted" href="#hacktoberfest-accepted">`hacktoberfest-accepted`</a> | PR that has been accepted for hacktoberfest!| humans |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="lgtm" href="#lgtm">`lgtm`</a> | Indicates that a PR is ready to be merged.| reviewers or members |  [lgtm](https://git.k8s.io/test-infra/prow/plugins/lgtm) |
| <a id="needs-ok-to-test" href="#needs-ok-to-test">`needs-ok-to-test`</a> | Indicates a PR that requires an org member to verify it is safe to test.| prow |  [trigger](https://git.k8s.io/test-infra/prow/plugins/trigger) |
| <a id="needs-rebase" href="#needs-rebase">`needs-rebase`</a> | Indicates a PR cannot be merged because it has merge conflicts with HEAD.| prow |  [needs-rebase](https://git.k8s.io/test-infra/prow/external-plugins/needs-rebase) |
| <a id="size/L" href="#size/L">`size/L`</a> | Denotes a PR that changes 100-499 lines, ignoring generated files.| prow |  [size](https://git.k8s.io/test-infra/prow/plugins/size) |
| <a id="size/M" href="#size/M">`size/M`</a> | Denotes a PR that changes 30-99 lines, ignoring generated files.| prow |  [size](https://git.k8s.io/test-infra/prow/plugins/size) |
| <a id="size/S" href="#size/S">`size/S`</a> | Denotes a PR that changes 10-29 lines, ignoring generated files.| prow |  [size](https://git.k8s.io/test-infra/prow/plugins/size) |
| <a id="size/XL" href="#size/XL">`size/XL`</a> | Denotes a PR that changes 500-999 lines, ignoring generated files.| prow |  [size](https://git.k8s.io/test-infra/prow/plugins/size) |
| <a id="size/XS" href="#size/XS">`size/XS`</a> | Denotes a PR that changes 0-9 lines, ignoring generated files.| prow |  [size](https://git.k8s.io/test-infra/prow/plugins/size) |
| <a id="size/XXL" href="#size/XXL">`size/XXL`</a> | Denotes a PR that changes 1000+ lines, ignoring generated files.| prow |  [size](https://git.k8s.io/test-infra/prow/plugins/size) |
| <a id="tide/merge-method-merge" href="#tide/merge-method-merge">`tide/merge-method-merge`</a> | Denotes a PR that should use a standard merge by tide when it merges.| humans | |
| <a id="tide/merge-method-rebase" href="#tide/merge-method-rebase">`tide/merge-method-rebase`</a> | Denotes a PR that should be rebased by tide when it merges.| humans | |
| <a id="tide/merge-method-squash" href="#tide/merge-method-squash">`tide/merge-method-squash`</a> | Denotes a PR that should be squashed by tide when it merges. <br><br> This was previously `tide/squash`, | humans | |

## Labels that apply to open-services-group/community, for both issues and PRs

| Name | Description | Added By | Prow Plugin |
| ---- | ----------- | -------- | --- |
| <a id="area/communication" href="#area/communication">`area/communication`</a> | Issues or PRs related to Communication| label | |
| <a id="area/governance" href="#area/governance">`area/governance`</a> | Issues or PRs related to Org Governance| label | |
| <a id="area/metrics" href="#area/metrics">`area/metrics`</a> | Issues or PRs related to Metrics| label | |

## Labels that apply to open-services-group/okr, for both issues and PRs

| Name | Description | Added By | Prow Plugin |
| ---- | ----------- | -------- | --- |
| <a id="area/aiops" href="#area/aiops">`area/aiops`</a> | all Key Results belonging to the AIOps endeavor <br><br> This was previously `aiops`, | label | |
| <a id="area/odh-et" href="#area/odh-et">`area/odh-et`</a> | all Key Results belonging to the ODH ET endeavor <br><br> This was previously `odh-et`, | label | |
| <a id="area/operate-first" href="#area/operate-first">`area/operate-first`</a> | all Key Results belonging to the Operate First initiative <br><br> This was previously `operate-first`, | label | |
| <a id="area/project-thoth" href="#area/project-thoth">`area/project-thoth`</a> | all Key Results belonging to Project Thoth| label | |
