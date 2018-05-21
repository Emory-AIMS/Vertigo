# Vertigo

The source code implements VERTIGO with one server and two clients. VERTIGO achieves parameter estimation for distributed logistic regression over vertically partitioned data. Please refer to https://academic.oup.com/jamia/article/23/3/570/2908996 for the paper. The source code is successfully compiled in Julia 0.4.7. To run the source code, please configure the server and client as follow.

For model parameter estimation
1. Server: Configure "DemoServer.jl" in folder "Server"
 - In "NETWORK", input your serverIP, msgPort and dataPort
 - In "users", input userID, username, and password
 - In "jobs", input taskID for userID
 - In "currentTask", input taskID and taskName
 - In "ParaInServer", input lambda (regularization parameter), maxit (max_iteration_number) and tol (tolerance of error)
 
2. Clients: Configure "DemoClient.jl" and "DemoClient2.jl" in folders "Client" and "Client2"
 - Use the same NETWORK and USER as server side
 - Use the full path to get local data X and model parameter for centralized realization (for evaluation)
