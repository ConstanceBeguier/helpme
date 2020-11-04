# Conda

## Main commands
@tags: conda create activate deactivate remove list

```
# Create an environment
$ conda create --name <name> python=3.7 [--prefix <path>]

# Activate an environment
$ conda activate my_env

# Deactivate an environment
$ conda deactivate

# Delete an environment
$ conda env remove --name my_env

# Show all environments
$ conda env list

# Show all packages of one environment
$ conda activate my_env
$ conda list

# Save an environment
$ conda activate my_env
$ conda env export > env.yml

# Create an environment from a file
$ conda env create --file env.yml

# Show history of all changes made on the environment
$ conda list --revisions
```
