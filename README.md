# PrivateAVAXVM
Not Completed as I was a solo team.
Hackathon Project to create a Private customized VM Subnet Implementation of the AVM.

The idea of this project was to have a private blockchain for an organization, which only allowed nodes to validate the blockchain if they were allocated in the statedb allow list/whitelist. 

The reason why the spacesvm was forked as a submodule to this project was that it is a vm optimized for storage.

In my implementation this vm will be tweaked to be optimized for storage of organizational data with disaster recovery in mind.

Future state the use of stateful precompiles could be used to augment and optimize the vm for more compatibility with organizational data that comes into the blockchain.

One could modify the state of this blockchain in the vm.go file, by using an if statement if a request is received from a remote address or remoteAddr then you could have a condition that checks if this remote address is in the whitelist, if it is permit access with a 200 response code using the writeheader method call. If the remote address is not in our whitelist issue a 403 response using the writeheader method call. 
