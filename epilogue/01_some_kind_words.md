!SLIDE
# let's talk shop!

!SLIDE 
# it's not all bad.

!SLIDE
# active_record vs. mongoid

!SLIDE bullets
# LOC
* ActiveRecord 2.3.8: _47342_
* ActiveRecord 3.0.5: _20142_
* ActiveModel 3.0.5: _3565_
* ARel 2.0.9: _5653_

!SLIDE bullets
# LOC
* MongoMapper: _13857_
* Plucky: _723_
* Mongoid: _8331_
* (Validatable): _2557_


!SLIDE
# mongo query syntax vs. SQL

!SLIDE code
    @@@ Ruby
    Post.tagged_with('foo').all

!SLIDE code
    @@@ SQL
    "SYNTAX ERROR NEAR 'JOIN taggings ON'"...
