# openWorkBenches-spec

The main product assembly: bench catalogs, compatible component versions, shared images, integration validation, and assembled releases.

Components each have their own assembly, spec, and code repositories:

| Component | Assembly repository |
|---|---|
| Desktop and mobile app | [openWorkBenchesApp](https://github.com/opensoft/openWorkBenchesApp) |
| Installer and CLI | [openWorkBenchesCli](https://github.com/opensoft/openWorkBenchesCli) |
| Organization service | [openWorkBenchesService](https://github.com/opensoft/openWorkBenchesService) |

Component assembly names follow the current openRepoShape naming policy. Product integration will consume exact component revisions; the initial scaffold pins its own spec and code legs.

The **spec leg** of the `openworkbenches` project: requirements, decisions and
acceptance criteria. The implementation lives in
[`opensoft/openWorkBenches-code`](https://github.com/opensoft/openWorkBenches-code).

**Clone the assembly root, not this repository.** This leg is mounted as a
submodule at `spec/` inside
[`opensoft/openWorkBenches`](https://github.com/opensoft/openWorkBenches), which
is what pins the commit of this repository that the project currently is:

```sh
git clone --recurse-submodules https://github.com/opensoft/openWorkBenches.git
cd openWorkBenches
make bootstrap
```

Working here directly is fine — it is an ordinary repository with an ordinary
branch. What advancing this leg does NOT do is advance the project: that is a
commit in the assembly root moving the gitlink, `contracts/spec-pin.yaml` and
any workflow `@<sha>` reference together.

Being the spec leg confers no authority over specifications. The split is
navigation; authority travels in grants, and a project that keeps spec and
code in one repository is reviewed identically.

Topic: `xf-project-openworkbenches`.


## License

Apache-2.0. Copyright 2026 OpenSoft. See [LICENSE](LICENSE) and [NOTICE](NOTICE).
