# Rails Associations

# belongs_to

![image](https://user-images.githubusercontent.com/24316133/138257835-ec1774da-5b0c-4b07-830b-5ca3e3f2020e.png)

```
class Book < ApplicationRecord 
belongs_to :author

end

# must be singular
#setsup a 1:1 connection with another model ---> to author in this example
#Books are associated to author via 'author_id' on books table

```

# has_many

![image](https://user-images.githubusercontent.com/24316133/138258130-5b9a8c66-af3b-43f8-a3cc-6e5c218f13c3.png)

```
class Author < ApplicationRecord
  has_many :books
end


# naming is plural
# indicates a one to many connection
# an author can have many books in this example
# books associated via 'author_id'
```
# has_one

![image](https://user-images.githubusercontent.com/24316133/138258562-854c61ea-08c4-4c6e-9699-7bb1cf5b3b00.png)

```
class Supplier < ApplicationRecord
  has_one :account
end

# only contains one instance of another model
# Supplier will only ever have a single account in this example
# Account associate via 'supplier_id'

```
# has_many :through 

## sets up a many-to-many association using another model

![image](https://user-images.githubusercontent.com/24316133/138258928-61ed1ee2-1800-485b-b574-5c544f6850e1.png)


```
class Physician < ApplicationRecord
  has_many :appointments
  has_many :patients, through: :appointments
end

# the appointment table would have both a 'physician_id' and 'patient_id' column

class Appointment < ApplicationRecord
  belongs_to :physician
  belongs_to :patient
end



class Patient < ApplicationRecord
  has_many :appointments
  has_many :physicians, through: :appointments
end
```

Source: https://guides.rubyonrails.org/association_basics.html
