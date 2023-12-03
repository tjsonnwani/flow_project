import holder from 0x05 //imported holder contract
//using systax for trasaction 
transaction(name:String , age:UInt64 , occupation:String , bankbalance: UInt64, account: Address){
  //verifying user who is chnaging data in contract holder
   prepare(signer : AuthAccount){
    log(signer)
   }

  //using execute statement inserting new value of parameters of person for specific address
   execute {
    holder.insert(name: name, age: age, occupation: occupation, bankbalance: bankbalance, account: account) 
     //giving msg that all insertion is sucessfully done 
    log("Succsessfully logged aacount information ! ")
   }
}
