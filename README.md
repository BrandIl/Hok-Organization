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
 
##### PaymentMethod (Required at least 1 of the properties: bankAccount or creditCard)
 * bankAccount
    * bankId (Required, Type: Number, length: 2)
    * branchId (Required, Type: string, length: 3)
    * accountNumber (Required, Type: string)
 * creditCard
    * creditNumber (Required, Type: string)
    * expiringDate (Required, Type: Mm/yyyy)
    * cvv2 (Required, Type: string, length: 3)

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


## Page Navigation

|  |  |
| ------ | ------ |
| / | Redirect to / organization |
| /organization | Organization lists |
| /organization/:id/edit | Edit organization details |
| /organization/:id/view | View organization details |
| /organization/:id/project | List of organization project |
| /organization/:id/project/create | New organization project |

