# dependabot-cargo-test

Test case for dependendabot Cargo file fetching.

- [`detached_crate_success`](detached_crate_success/Cargo.toml): Has path dependency to [`workspace/nested_one/nested_two/Cargo.toml`](workspace/nested_one/nested_two/Cargo.toml)
and [`detached_workspace_member/Cargo.toml`](detached_workspace_member/Cargo.toml), and is able to resolve their workspace root [`workspace/Cargo.toml`](workspace/Cargo.toml) by searching
parent directories & checking `package.workspace` key
- [`detached_crate_fail_1`](detached_crate_fail_1/Cargo.toml): Has path dependency to [`incorrect_workspace/Cargo.toml`](incorrect_workspace/Cargo.toml), but fails to find its workspace root
when searching parent directories
- [`detached_crate_fail_2`](detached_crate_fail_2/Cargo.toml): Has path dependency to [`incorrect_detached_workspace_member/Cargo.toml`](incorrect_detached_workspace_member/Cargo.toml),
but fails to find its workspace root based on `package.workspace` key
