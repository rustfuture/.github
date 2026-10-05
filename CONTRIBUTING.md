# Contributing

Thanks for taking the time to help. This guide applies to every rustfuture repository; a repository's own
README or CONTRIBUTING file wins where it says something different.

By taking part you agree to the [Code of Conduct](CODE_OF_CONDUCT.md). Security problems go through
[SECURITY.md](SECURITY.md), never a public issue.

## Issues

- **Bug:** what you ran, what you expected, what happened, the version (`<tool> --version` or commit) and your OS.
- **Feature:** the problem you want solved before the solution. Open an issue before a large PR so we can
  agree on the shape first.

## Pull requests

1. Branch off `main`. One change per PR.
2. Run the same checks CI runs before you push. Each repository's `.github/workflows/ci.yml` lists them;
   for the Rust projects that is usually:

   ```sh
   cargo fmt --check
   cargo clippy --locked --all-targets -- -D warnings
   cargo test --locked
   ```

   For the Python projects, run the commands in their `ci.yml`.
3. Add a test for new behaviour or a fixed bug, and update the README when user-facing behaviour changes.
4. Write commit messages that say what changed and why in plain English.
5. CI must be green before review. PRs are squash-merged.

## License

Contributions are licensed under the license of the repository you contribute to (see its `LICENSE` file).
