## Cat Tinder Backend 2/2/24 Indica

### Main branch
1. Read Trello/place in the appropriate swimming lane, team members join the card

2. Create empty github repo

3. Create the rails app

4. Connect the empty github repo and rails app

5. Start the server

6. Make the initial commit

7. Ping the instructor and ask for branch protections

8. Ensure the trello card is in its appropriate swimming lane

9. Respond according to the instructors emoji

10. Perform github/git hygiene

### Backend-structure
[Cat Tinder API Intro](https://github.com/learn-academy-2023-india/syllabus/blob/main/cat-tinder/backend/api-intro.md)  

As a developer, I can create a RSpec testing suite in my Rails application.
- rspec gem and install added on the main branch

As a developer, I can add a resource for Cat that has a name, an age, what the cat enjoys doing, and an image.
- rails g resource CatFight name:string age:integer enjoys:text image:text
- rails db:migrate

As a developer, I can add cat seeds to the `seeds.rb` file.

https://github.com/learn-academy-2023-india/syllabus/blob/main/cat-tinder/backend/seeds.md

Instead of scaffolding data entries in the rails console, 
`> CatFight.create(name: 'Jack', age: 5, enjoys: 'Furrrrociously hunting bugs.', image: 'https://images.unsplash.com/photo-1492370284958-c20b15c692d2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1049&q=80')`  

We will now use the seeds file to create some mock data for the application.

a) Create an array with objects that have the expected key:value pairs for each instance. 
```rb
cats = [
  {
    name: 'Clawdzilla',
    age: 2,
    enjoys: 'Climb in, on, and around cardboard boxes',
    image: 'https://images.unsplash.com/photo-1574144611937-0df059b5ef3e?w=800&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8N3x8Y2F0JTIwZmlnaHR8ZW58MHx8MHx8fDA%3D'
  },
  {
    name: 'Thunderpaws',
    age: 12,
    enjoys: 'Racing around the house for no apparent reason',
    image: 'https://images.unsplash.com/photo-1503362516536-635096dd5a80?w=800&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTN8fGNhdCUyMGZpZ2h0fGVufDB8fDB8fHww'
  },
  {
    name: 'The Litterbox Legend',
    age: 5,
    enjoys: 'Sitting on computer keyboards',
    image: 'https://media.istockphoto.com/id/1200175491/photo/ferocious-red-cat-bites-its-owner-in-the-arm-with-all-its-power.jpg?s=612x612&w=0&k=20&c=Srh2wiUHMsOsU4xa_vOapCCdLM7JCxNsGK1syMNGjYU='
  }
]
```

cats.each do |each_cat|
  Cat.create each_cat
  puts "creating cat #{each_cat}"
end

creating cat {:name=>"Felix", :age=>2, :enjoys=>"Long naps on the couch, and a warm fire.", :image=>"https://images.unsplash.com/photo-1529778873920-4da4926a72c2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1036&q=80"}
creating cat {:name=>"Homer", :age=>12, :enjoys=>"Food mostly, really just food.", :image=>"https://images.unsplash.com/photo-1573865526739-10659fec78a5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1015&q=80"}
creating cat {:name=>"Jack", :age=>5, :enjoys=>"Furrrrociously hunting bugs.", :image=>"https://images.unsplash.com/photo-1492370284958-c20b15c692d2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1049&q=80"}

https://github.com/learn-academy-2023-india/syllabus/blob/main/cat-tinder/backend/api-cors.md

## CORS stands for Cross-Origin Resource Sharing