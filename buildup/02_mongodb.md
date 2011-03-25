!SLIDE
# webscale.

!SLIDE 
# MongoDB

!SLIDE
# document.

!SLIDE
# stuff that belongs together.

!SLIDE
# tags.

!SLIDE
# don't try this at home.

!SLIDE code
    @@@ SQL
    INSERT INTO posts (title, text) 
      VALUES ('title', 'text');
    SELECT * FROM tags 
      WHERE tags.name IN ('foo', 'bar');
    INSERT INTO tags (name) VALUES ('foo');
    INSERT INTO taggings 
      (tag_id, taggable_id, taggable_type) 
      VALUES (12, 42, 'Post');
!SLIDE code
    @@@ Javascript
    {
      "title": "title",
      "text": "text",
      "tags": ["foo", "bar"]
    }
!SLIDE code
    @@@ SQL
    SELECT posts.* FROM posts
      JOIN taggings ON
        taggings.taggable_id = posts.id 
        AND taggings.taggale_type = 'Post'
      JOIN tags ON
        taggings.tag_id = tags.id
      WHERE
        tags.name = 'foo'

!SLIDE code
    @@@ Javascript
    {
      "tags": "foo"
    }
    
!SLIDE
# excursion

!SLIDE
# PostgreSQL has arrays.

!SLIDE code
    @@@ SQL
    INSERT INTO posts (title, text, tags)
      VALUES (
      'title', 'text',
      {'foo', 'bar'}
    )
!SLIDE code
    @@@ SQL
    SELECT * FROM posts WHERE 
      'foo' = ANY(tags)

!SLIDE
### Tip: Arrays are not sets; searching for specific array elements can be a sign of database misdesign. *Consider using a separate table with a row for each item* that would be an array element. This will be easier to search, and is likely to scale better for a large number of elements.
### [http://www.postgresql.org/docs/9.0/interactive/arrays.html](http://www.postgresql.org/docs/9.0/interactive/arrays.html)

!SLIDE
# rich structure, queryable.

!SLIDE
# flexible, changeable.




!SLIDE
# migrations.

!SLIDE
# first scaling hurt.