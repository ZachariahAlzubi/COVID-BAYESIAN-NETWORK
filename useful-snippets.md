# Useful Snippets

## Anaconda/Mamba

To create the environment from the `environment.yml` file:

```bash
mamba env create -f environment.yml
```

To export the environment changes in an OS-agnostic form:

```bash
mamba env export --from-history > environment.yml
```