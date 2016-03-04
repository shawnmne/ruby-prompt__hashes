---
title: Hashes
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is a Hash?

A Hash is a collection of key-value pairs like this: "employee" => "salary". It is similar to an Array, except that indexing is done via arbitrary keys of any object type, not an integer index.

# What are some examples of information that would be Hashes as opposed to some other data type?

The cat hash below is a great example of a hash.  The key is not and can not be an integer and therefore an array would not work as a data type.  The key here is the hair type of a cat. 
The corresponding value to each key represents the breed of the cat.
cats = Hash.new
cats[:longhair] = "persian"
cats[:shorthair] = "siamese"

# How are Hashes and Arrays similar? How are they different?

They are similar because they are both indexed collection of object references.  They are different because you index arrays with integers only and hashes can be indexed with objects of any type: strings, regular expressions, and so on.

# How do you retrieve a particular value from a Hash?

You can retrieve the value of a hash by indexing the hash with its key.
cats[:longhair]

# How do you add information to a Hash?

Simply add a new key with corresponding information
cats[:bald] = "sphynx"

# How would you perform an operation on every element inside a Hash?

It appears there is no clean way to do so but can use .each method

cats.each { |key, value| puts "My #(key} cat is a #{value}."}  outputs
My longhair cat is a persian.
My shorthair cat is a siamese.
My bald cat is a sphynx.

# How would you change the value of a particular element in a Hash?

Reference the element with the proper key and set it = to the new information
cats[:longhair] = "maine coon"

# How do you delete an element from a Hash?

use the .delete method
cats.delete("bald")

# What happens if you try to retrieve an element from a Hash that does not exist in the Hash?

if you attempt to access a hash with a key that does not exist, the method will return nil.

# How do you determine how many elements are in a Hash?

hash.size returns the size or length of hash as an integer