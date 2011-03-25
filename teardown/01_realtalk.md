!SLIDE 
# active_record

!SLIDE code
    @@@ Ruby
    Post.new(
      {
        title: "title",
        text: "text",
        "tag_names": "foo, bar"
      }
    )

!SLIDE
# cheat.

!SLIDE
# acts_as_taggable_on

  
!SLIDE code
    @@@ Ruby
    Post.tagged_with('foo').all

!SLIDE
# rails integration.

!SLIDE
# ActiveModel

!SLIDE
# abstraction.

!SLIDE
# MongoMapper

!SLIDE center
![](mongomapperdotcom.jpg)

!SLIDE
# lé \*sigh\*

!SLIDE
# Mongoid

!SLIDE
# has documentation.

!SLIDE
# has no stable version for rails 3

!SLIDE
# (But any day now...)

!SLIDE code
    @@@ Ruby
    class Person
      include Mongoid::Document
      references_one :policy
      references_many :prescriptions
    end

!SLIDE
# POLS

!SLIDE
# lé \*sigh\*

!SLIDE
# amazing work.
