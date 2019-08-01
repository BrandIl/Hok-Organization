# Hok-Organization

## Models

##### Organization
 * name (Required, Type: string, max-length:25)
 * communication (Required, Type: Communication)
 * masavData (Required at least 1 of the properties: credit or charge)
    * Credit
      * CodeNosse (Type: string, length:8)
      * senderCode (Type: string, length:5)
    * Charge
      * CodeNosse (Type: string, length:8)
      * senderCode (Type: string, length:5)
 * concats (Type: [ Concat ])
 * paymentAgreement
    * minPrice (Required, Type: Number)
    * feePerUnit (Required, Type: Number)
    * dayOfCharge (Required, Type: Number, range: 1-28)
    * paymentMethod (Required, Type: PaymentMethod)
    
##### Concat
 * name (Required, Type: string, max-length:35)
 * celular (Required, Type: string, length:10)
 * email (Type: Email, max-length:50)
 * remarks  (Type: Email, max-length:50)
 
##### Project
 * Name (Required, Type: string, max-length:25)
 * Organization (Required, Type: ObjectId)


## Endpoints

|  |  |   |
| ------ | ------ | ------ |
| GET | /organization | Organization lists |
| GET | /organization/:id/ | Get organization |
| POST | /organization | Create organization |
| PUT | /organization/:id/ | Update organization |
| POST | /project | Create project |
| GET | /project/:id/ | Get project |
| PUT | /project/:id/ | Update project |
