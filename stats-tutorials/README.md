# Bayesian statistics

During this session the following topics will be discussed:

1. Bayesian statistics in practice (ch.1 Bayesian methods for hackers)

   - _showcase the process_: brief visualization of Bayesian posteriors
   - _automation_: introduce a Bayesian toolbox, PyMC
   - _examples_: inference with PyMC

   **notebook:** https://colab.research.google.com/drive/1e1De9_qUryjxR2WiCEuKfPQbUHr-gTjU?usp=sharing

2. CKM matrix determination (HEP exercise)

   **notbook:** https://colab.research.google.com/drive/1rPQmHO4-_xORlKFFcJEuS9EB-0wBAn2m?usp=sharing

3. Markov Chain Monte Carlo (custom notebook)

   - let's build our simple Metropolis MCMC

   **notebook:** https://colab.research.google.com/drive/16lxk_x44atMkt2YJ-ZQ5bOg5vvuqmJkC?usp=sharing

Already mentioned above, an interesting resource about Bayesian statistics libraries and
MCMC is the ["Bayesian methods for
hackers"](https://github.com/CamDavidsonPilon/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers)
book.

In particular, it is especially valuable to take a look at its [chapter
3](https://github.com/CamDavidsonPilon/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers/blob/5b33f77a803a1a07dcadabae6cc382c9fd2c77d7/Chapter3_MCMC/Ch3_IntroMCMC_PyMC_current.ipynb).

## Further tools

PyMC is an example of a family, whose structure follows more or less always the
following pattern: a probability and inference library in Python built on top of a
Python tensor library.

- **PyMC**, originally built on top of **Theano**, then **Aesara**, now
  **PyTensor** (just a fork chain)
- **TensorFlow Probability**, obviously built on top of **TensorFlow**
- **Pyro**, on top of **Pytorch**
- **NumPyro**, on top of **JAX**

A further inference library, publishing Python bindings, is **Stan**.
Stan is a different and very popular library, following a more statistically-oriented
approach (as opposed to a more software oriented one), essentially with its own
declarative language.
