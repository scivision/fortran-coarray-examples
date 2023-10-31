mpiexec = find_program('mpiexec', required : false)
 # MS-MPI has only mpiexec

# -- Fortran coarray

coarray = dependency('coarray', required : false)

# ---

hello = executable('coarray_hello', 'helloworld.f90', dependencies : coarray)
test('Coarray Hello', hello, timeout: 20, suite: 'coarray', is_parallel : false)

pi = executable('coarray_pi', 'pi.f90', dependencies : coarray)

test('Coarray Pi', pi, timeout: 20, suite: 'coarray', is_parallel : false)
