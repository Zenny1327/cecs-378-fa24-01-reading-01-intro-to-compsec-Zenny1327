# CECS 378 Reading Assignment: Introduction to Computer Security

1.  Computer Security deals with computer related assests that may be subject to various threats and or harm that
    devises many protocols to protect said assets. 

2.  Passive attacks are in a similar field as spying, such as monitoring and or obtaining private information
    Active attacks actively modify data that is being passed through whether its being redirected, stored, or changed. 

3.  An Attack Surface is basically a reachable exploitation of a vulnerablity, whether it be through means of
    network, software or human attacks.
    A Attack Tree is more like a plan or blueprint for how an attacker will/could infiltrate/exploit a vulnerability. Like the data structure: there are nodes, branches, and leaves that all represent ways an attacker may reach their goal(the root). 

4.  Confidentiality:  At most, the two risks of confidentiality are the users pin and their card itself, if a user 
    were to lose/forget either of these things they wouldnt be able to access an ATM and if lost, their funds may be at risk if an attacker has both. This risk could be considered low since most ATMS have a pin shield, and cards can be cancelled if lost. 
    Integrity: A loss of integrity could be slightly worse, if an attacker were to obtain more than just a pin and a card, they could theoretically get bank information access which could lead to many other long term fradulent issues. Risk level should be considered mild.
    Availability: The hightest level of risk that should be considered, given the entire purpose of an ATM is to allow a user to access their funds, if service is denied or servers are down, the entire machine becomes obselote. 

5.  Simililarily to the ATM, a phone switching system may face different kinds of threats. 
    Confidentiality: Human error being the biggest threat to confidentiality in this system with scam calls being the highest form of data leaks, the only real way to combat this is through education or at a higher technical standpoint, banning/disabling scam calls in some way. Risk level is mild. 
    Integrity: There isn't much information that i can think of that could be stolen from this type of service, so I'd rate it a risk level of low. Similiar to Confidentiality, human error persists as its greatest threat. 
    Availability: The highest risk factor I believe to be is availability, similar to the ATM, access to sucha  service should be the highest priority, as its main purpose is to provide that service. 

6.  Economy of mechanism: the design of security measures that have to do with both hardware and software should
    be  as small as possible, with a ease of access to test.
    
    Fail-Safe default: Access decisions should be based on permissions rather than exclusion.
    
    Complete Mediation: every access must be verified and checked amongst the controll mechanism. 
    
    Open Design: The design should be open rather than secret
    
    Separation of privilege: Requirong multiple priviledge attributes to be able to access restricted resources. 
    
    Least privilege: Maintaining that every user should have the least amount of privileges needed necessary to perform their tasks. 
    
    Least common mechanism: Minimize functions that are shared by different users, leading to mutual security. 
    
    Psychological acceptability: Meet the needs of those who have authorized access while not hindering the usability or accessibility of resources that users may need. 
    
    Isolation: Isolate public access from critical resources to prevent tampering, isolate process and files of indvidual users  from one another, lastly, isolating security mechanisms for the sake of preventing access to the those mechanisms. 
    
    Encapsulation: Special form or isolation, isolating certain procedures and data obejects so that they may only be accessed through designated entry ports. 
    
    Modularity: provide common security functions and services with regards to the development of security functions as seperate protected modules. 
    
    Layering: use of multiple overlapping protection approaches addressing the people, tech, and operational aspects of information systems.
    
    Least Astonishment: a progrma or user interface should always respond in the way to least likely astonish the user.

7.  1)  If a hospital or government organization handled sensitive information such as medical history or tax and social security
    information, confidentiality would be the highest requirement. 
    2)  Similarly, in a hospital, patient information about allergies or high risk medications would be integral to patient saftey, making the integrity of this information have the highest inmportantance.
    3)  If a coffee shops menu is updated through such a service, employees who would use the computer to select orders and drinks and process payments would need that system and documents to be readily available.

8. 1)   Confidentiality: low; since the info is public access. Integrity: high; since it should be kept accurate. Availability: mild; to keep accessible but also making sure that the infomation is still accurate. 
    2)  Confidentiality: High; highly sensitive documents. Integrity: mild; maintain accuracy without leakage. Availability: low; slow or limited access isnt as bad as leaked classified documents. 
    3)  confidentiality: low; rotuine information. Integrity: mild; maintain accurate info with low risk. Availability: high; in order to keep the buisness fully functioning at its best.
    4)  For both: Confidentiality should be the highest priority for both sensitive and adminstrative information. Integrity should be mild in order to both maintain accuracy since it is a information system. Availability would be low as ther is likely a bigger threat of data leakage. 
    5) Confidentiality: low; it is an energy plant so leak of data isnt a high concern. Integrity: mild; as statisitcs and logged readings should be monitored heavily and accuracy maintained. Availability: High; as this information should be readily accesible in case of disaster circumstances. 

9.  root: access to money in safe. Branch 1: explosives. Branch 2: cracking the code -> leaf 1: having the code prior. Leaf 2: threatening/harming teller/worker for combination

10. It seems that dwRet is checked if access is allowed, then if and only if it says its denied, then it wont persist. But if function returns anything else besides that statement,  itll allow it. I think the fix would be to originally deny the access until something provided were to grant access. 

    ``` C
    DWORD dwRet = IsAccessAllowed(...);
    if (dwRet == Success) { // Security check passed.
    // Inform user that access is accepted. } else {
    // access denied. inform of denial
    }
    ```
