# macel

Multi-Architecture Code Emission Library (macel) is a library which implements
a low-level intermediate representation meant to expose on machine-level
details such as registers, intended for use as a compiler backend.

Macel functions are represented with a `Proc` which represents a CFG of basic
blocks. Each block comprises of a sequence of `Inst`s.

Macel is intended as superset of the supported architectures: Instructions from
all possible target CPUs are representable. Users of this library are able to
query whether each instruction form is valid for a given backend and pick the
appropriate form. If such control is not required and performance is not a
concern, renormalization can be done so that the instruction is appropriately
emulated on the target.
