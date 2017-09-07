# sm-pgres

Hacking Postgres database code in order to learn more 

## 1. Build and deploy your own version of postgres database server

    1.  Run  configure script first
    2.  Run make -j4
    3.  Run make test
    4.  Run make install
    5.  Run initdb command  in order to initialize the psotgres instance
    6.  Start the postgres server using the pg_ctrl command

##  2. Run and debug postgres server

    1. Change the global makefile under the source directory to add -g compiler option.
    2. Follow steps 2 to 6
    3. Run psql and enter the following command
         -  select pg_backend_pif();
       The output should be the pid of the Postgres server.
    4. Run gdb -p <pid> in sudo mode 
    5. Create a breakpoint at exec_simple_query or any other function 
