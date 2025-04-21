# FEC-Blockbase
> Task 1
added     function isRegistered(address _addr) public view returns (bool) {
    return people[_addr].walletAddress != address(0);
} to blockbase.sol to make a function Check if a user is registered
then called the function from app.js by the code
const checkIsRegistered = async () => {
  if (!contract || !checkAddress) {
    alert("Contract not loaded or address empty");
    return;
  }
  try {
    const result = await contract.isRegistered(checkAddress);
    alert(result ? "Registered" : "Not registered");
  } catch (err) {
    alert("Error: " + err.message);
  }
};
and also added a button for this


> Task 2
  added the code
 <p>Total Registered Users: {people.length}</p>
  in app.js to display the total number of registered users
