## Bazel build on linux of [solid-sim-tutorial-gpu](https://github.com/phys-sim-book/solid-sim-tutorial-gpu)

```bash
# Install sfml on linux
sudo apt-get install libsfml-dev

# modify the cuda archs in file .bazelrc to your case(need sm_80+)
build --cuda_archs=compute_89:compute_89,sm_89
run --cuda_archs=compute_89:compute_89,sm_89

# run example
bazel run //solid_sim_muda/1_mass_spring:mass_spring_main
```