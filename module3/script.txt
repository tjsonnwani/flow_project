import holder from 0x05 //importing contract 

//setting up main function which take input parameter address
pub fun main(account :Address ): holder.details {

//returning the person accountdetails using using optionals unwrap -> !  
  return holder.person[account]! 
}
