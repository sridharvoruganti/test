## Sprint Review 03.Sep.2020
### Summary:

- #367 thirdparty-scheme-adapter: Handle Outbound `POST /thirdpartyRequests/transactions/{id}/authorizations` 

  **Goal**: As a DFSP, I want to be able to ask the switch to verify a thirdparty transaction so I can proceed with a thirdparty transaction
  
  **Tasks**  

  :heavy_check_mark: Implement outbound POST /thirdpartyRequests/transactions/{id}/authorizations call (DFSP -> Switch)
  
  :heavy_check_mark: Implement state machines as required
  
  :heavy_check_mark: Unit tests
  
  :x: Integration tests 
  
  
- #365 thirdparty-scheme-adapter: Handle Inbound  `PUT /thirdpartyRequests/transactions/{id}/authorizations`

  **Goal**: 
      As a DFSP I want to receive a successful authorization result from the auth-service so I know to proceed with a thirdparty transaction
      
  **Tasks**        
  
     :heavy_check_mark: Implement inbound request handler
     
     :heavy_check_mark: Make necessary changes to the state machines
     
     :heavy_check_mark: Determine whether or not this should live in the sdk-scheme-adapter or the thirdparty-scheme-adapter
     
     :heavy_check_mark:  Unit tests
     
     :x: Integration tests (Integration tests will likely just cover the integation between the 'cache' and state machine)
     

> 367 `thirdparty-scheme-adapter` ------> `thirdparty-api-adapter`  ------> `auth-service(ml-testing-toolkit)`

> 365 `thirdparty-scheme-adapter` <------ `thirdparty-api-adapter`  <------ `auth-service(ml-testing-toolkit)`                                                                                                                                
                                                                                                            
