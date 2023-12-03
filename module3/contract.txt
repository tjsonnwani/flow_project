pub contract holder {
  //creating dictionary named person
    pub var person : {Address : details }
//creating struct named accountdetails
    pub struct details {
      pub let name : String
      pub let age  : UInt64
      pub let occupation : String
      pub let bankbalance : UInt64
     
      pub let account : Address

    
    // initializing struct 
    init(_name : String , _age: UInt64, _occupation: String , _bankbalance : UInt64 , _account  : Address ){

      self.name = _name
      self.age = _age 
      self.occupation = _occupation
      self.bankbalance = _bankbalance
     
      self.account = _account

      
    }
    }
//creating function for transaction 
    pub fun insert(name:String , age  : UInt64 , occupation  :String, bankbalance : UInt64 , account : Address ){
       let newentry  = details(_name:name , _age:age , _occupation:occupation , _bankbalance:bankbalance, _account : account )
    
       self.person[account] = newentry
       
    }
  //initializing dictionary here 
    init(){
      self.person = {}
    }
}
