# CertiChain
A blockchain application to verify the essential documents required by the applicant for an interview process. This enhances the transparency and prevents any user from faking his identity. The blockchain technology provides immutability and publicly verifiable transactions, these  properties  of  Blockchain  can  be  used  to  generate  the  digital  certificate  which are  anti-counterfeit  and easy to verify.


Working:
A blockchain application to make the certification process easier for the HR interviewer. It constructs a Merkle Tree which contains nodes consisting of the hashes generated by the data given by the universities (Name, CPI, College Name and Year of Graduation). The root of this Merkle tree is the combined hash of all the individual hashes, this root is then put on the blockchain.

<p align="center">
 <img  src="./static/images/Hash_Tree.png" alt="Merkle Tree">
</p>

A smart contract is written to map the College and the Year of Graduation to the root hash, this contract is then deployed using Ganache, Ethereum local blockchain.  

When the applicant uploads his resume, it parses the resume and extracts significant details like Name, CPI, College Name and Year of Graduation using NLP techniques and stores it in a json format and creates a hash of that and combine it with the neighboring hashes and generates the root hash. 

<p align="center">
 <img  src="./static/images/resumeparser.png" alt="Merkle Tree">
</p>

It then verifies this root hash with the hash on the blockchain and accordingly decides the validity of the resume.

A distributed and automated system for background verification could address several challenges in hiring:
    Assessing information accurately, without manual effort
    Depending on third-party vendors for verification, adding to hiring costs
    Inability to verify employment if the last place of work has gone out of business
