Multi-Facility Demo
===================

Authenticate seamlessly between Computational facilities and orchestrate workflows.

.. note:: Please note that this requires the `remote_interchange` branch from Parsl 
      
```
              +-------AWS---------------------------------+
              |  +----------Jupyter Notebook-----------+  |
              |  |              Parsl                  |  |
              |  |       Theta                Cori     |  | 
              |  |  |Executor, channel       Executor, |  |
              |  |     |       Provider        | ...   |  |
              |  |     |         |             |       |  |
              |  |     |         |              \      |  |
              |  +----/---------/----------------\-----+  |
              +------/---------/------------------\-------+
                    /         /                    \
                   |         /                      \
     +----Theta----|--------|-----+    +-------------|----Cori----+
     | +-----Login-|--+ +---V---+ |   | +-----Login--+----------+ |
     | | Interchange | | Cobalt | |   | |           Interchange | |
     | +---------|---+ +----|---+ |   | +-----------------------+ |
     |           |          V     |   |                           |
     | +---------|---------Job--+ |   |           ...             |
     | | +-------|--node------+ | |   |                           |
     | | |       Manager      | | |   |                           |
     | | |      /      \      | | |   |                           |
     | | | worker      worker | | |   |                           |
     | | +--------------------+ | |   |                           |
     | +------------------------+ |   |                           |
     +----------------------------+   +---------------------------+
```
