Answer 1 . The relationship between the "Products" and the "Product_Category" entities. "category_id" in 'product table' is foreign key and connected to "id" in 'product_category' which is primary key.

Answer 2 . Insert all valid categories into the 'category' table. then, ensure that the 'category_id' you assign to each product exists in the 'category' table.

Answer 3 . Schema

const mongoose = require('mongoose');
const { Schema } = mongoose;

const userSchema = new Schema({
    name: {
        type: String,
        required: true
    },
    email: {
        type: String,
        required: true,
        unique: true
    },
    password: {
        type: String,
        required: true
    },
    date: {
        type: Date,
        default: Date.now
    }
  });


const Users = mongoose.model('Users', userSchema);
module.exports = Users;
