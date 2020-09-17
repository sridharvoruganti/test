## Sprint Review 17.Sep.2020
### Summary:

- **#1669** [docker-contract] - scratch transaction initiation with `ml-testing-toolkit` - **Completed**

  **Goal**: As a OSS developer, I want to test the end to end PISP transfer with the ml-testing-toolkit
  
  **Tasks**  

  :heavy_check_mark: Update ml-testing-toolkit config in pisp/docker-contract
  
  :heavy_check_mark: Configure PISP calls POST /thirdpartyRequests/transactions/{id} TTK calls a POST /authorizations callback
  
  :heavy_check_mark: Configure PISP calls PUT /authorizations/{id}, TTK calls a PATCH /thirdpartyRequests/transactions/{id}
  
  :heavy_check_mark: Add postman examples for 2x async api calls above
  
  
  
- **#1670** [thirdparty-scheme-adapter] - end to end PISP side transaction with ml-testing-toolkit - **Blocked**

  **Goal**: 
      As a OSS developer, I want to be able to prove the thirdparty-scheme-adapter can handle the PISP side of a thirdparty transaction
      
  **Tasks**        
  
     :heavy_check_mark: docker-compose configuration for testing toolkit + thirdparty-scheme-adapter (this can be copied from docker-contract)
     
     :x: Write a set of tests which target the thirdparty-scheme-adapter's outbound api for initiating PISP transactions - happy path only
     
     

- **#1705**  Migrate `POST /thirdpartyRequests/transactions` from sdk-scheme-adapter to thirdparty-scheme-adapter - **In Progress**

  **Goal**: 
      As a oss developer, I want to Migrate POST /thirdpartyRequests/transactions from sdk-scheme-adapter to thirdparty-scheme-adapter
      
  **Tasks**        
  
     :heavy_check_mark:  Outbound POST /thirdpartyRequests/transactions
     
     :heavy_check_mark:  Outbound GET /thirdpartyRequests/transactions/{ID}
     
     :x:  Inbound PATCH /thirdpartyRequests/transactions/{ID}
     
     :x:  Inbound PUT /thirdpartyRequests/transactions/{ID}/error
     
     
                                                                                                                             
                                                                                                            
