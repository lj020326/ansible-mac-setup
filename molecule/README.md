## Molecule testing framework


### Installing Molecule

```

pip3 install molecule

```

### Using Molecule

```

- Create a new role with molecule
molecule init role test-role

- Test role

molecule test

- And test it but leave the container running for debugging
molecule converge

set a breakpoint using fail: in the tasks

```