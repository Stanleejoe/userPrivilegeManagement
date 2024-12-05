let user = {  
    role: "admin", 
    experience: 6, 
    active: true, 
    department: "IT" 
};  
 
let accessLevel = (user.role === "admin") ?   
    (user.active ?   
        (user.experience > 5 && user.department === "IT" ? "Full IT Admin Access" :  
         user.experience > 5 ? "Full General Admin Access" :  
         "Limited Admin Access") :  
        "Admin Access Revoked") :  
    (user.role === "manager") ?  
    (user.active ?  
        (user.experience > 3 && user.department === "Sales" ? "Full Sales Manager Access" :  
         user.experience > 3 ? "Full Manager Access" :  
         "Limited Manager Access") :  
        "Manager Access Revoked") :  
    (user.role === "user") ?  
    (user.active ?  
        (user.department === "Support" ? "Priority Support Access" :  
          "User Access") :  
        "User Access Revoked") :  
    "Invalid Role";  

 
console.log(accessLevel);
