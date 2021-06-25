// validates the brand
	// brand should always start with a upper case alphabet 
	// and can be followed by one or more alphabets (lower case or upper case) 
	public Boolean isValidBrand(String brand){
		String regex="[A-Z][A-Za-z]{1,}";
		return brand.matches(regex);
	}



	// validates the IMEINumber
	// it should be a 16 digit number 

public Boolean isValidIMEINumber(Long iMEINumber) {
		String number=iMEINumber.toString();
		if(number.length()==16) {
			return true;
		}
		else {
			return false;
		}
	}



 public Boolean isValidStatus(IssueStatus status)
 {
	// Your Code Goes Here
     String sta=status.toString().toUpperCase();
     if(sta.equals("OPEN")||sta.equals("IN_PROGRESS")) {
	 return true;
     }

	return false;
 }
}





	// validates the contact number
	// should contain 10 numeric characters and should not contain 10 repetitive characters
	public Boolean isValidContactNumber(Long contactNumber) {
		String check = Long.toString(contactNumber);
		String regex = "([0-9]{10})";
		String regexAvoid = "([0-9])\\1{9}";
		if(check.matches(regexAvoid))
			return false;
		else if(check.matches(regex))
			return true;
		return false;
	}
	
	
	// validates the customer name
	// should contain at least one word and each word separated by a single space should contain at least one letter.
	// the first letter of every word should be an upper case character 
	public Boolean isValidCustomerName(String customerName) {
		String regex="(([A-Z])([a-z])+([\\s]?))+";
		if(customerName.matches(regex))
		return true;
		else return false;
	}
}



public Boolean isValidName (string name)
{
//your code goes here
String regex-"[A-Za-z]{3,}";
if(name!=null &&name.matches(regex)
return true;
else
return false;
}



public Boolean isValidPublisher(String publ1isher)
{
// your code goes her 
if((publisher.equalsIgnorecase("DCD") || publisher.equalsIgnoreCase("MARVAL") &&
(Publisher!=null) && (publisher.isEmpty()) && (publisher.isBlank()))
return true;
else
return false;




 public BooleanisValidPhoneNo(Long phoneNo)
{

String regex = "([0-9]) (\\1{9})"; 
String regex1 = "[0-9]{10}"; 
return (phoneNo.toString().matches(regex1)&& !phoneNo.toString().matches(regex) ) ;
}


 public Boolean isValidUserName (String userName)
{
if(userName.isBlank() || userName.isEmpty()) 
{ 
return false;
}
String regex ="([A-Z] [A-Za -z]+) ([A-Z][A-Za-z]+)?"; 
return userName.matches(regex);

}


//valid applicant name

public Boolean isValidApplicantName(String applicantName) 
{
	String regexString="([A-Za-z]{3,})+";
	if(applicantName!=null)&&(!applicantName.isBlank())&&(!applicantName.isEmpty())&&(applicantName.matches(regex))
	{
		return true;
	}
	else 
		return false;
			
}

public Boolean isValidBookId(Integer bookId)
{
return bookId.toString().length()==6;
}

public Boolean isValidGenre(String genre)
{
String regex="(Adventure|Mystery|Fiction|History)";
return genre.matches(regex);
}

public Boolean isValidName(String name)
{
if(name.isEmpty()||name.isBlank())
{
return false;
}
return name.matches("([A-Z][a-z]+)([A-Z][a-z]+){0,9})";
}
}
