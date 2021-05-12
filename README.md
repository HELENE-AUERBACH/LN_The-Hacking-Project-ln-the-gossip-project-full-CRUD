# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

ruby 2.7.1p83 (2020-03-31 revision a0c7c23c9c) [x86_64-linux]

* Rails version

Rails 5.2.3

* Configuration

$ rm ln-the-gossip-project-full-CRUD/Gemfile.lock

$ gem uninstall rails
(=> 3. All versions)

$ gem uninstall railties
(=> 3. All versions)

$ cd ln-the-gossip-project-full-CRUD

ln-the-gossip-project-full-CRUD$ bundle install

ln-the-gossip-project-full-CRUD$ rails -v
(=> Rails 5.2.3)

* Database creation

Mettre à jour le fichier config/database.yml (il faut "personnaliser" le nom de la database, - ainsi qu'éventuellement le username et le host -, pour le development).

ln-the-gossip-project-full-CRUD$ RUBYOPT='-W:no-deprecated -W:no-experimental' rails db:create

ln-the-gossip-project-full-CRUD$ RUBYOPT='-W:no-deprecated -W:no-experimental' rails db:migrate

* Database initialization

ln-the-gossip-project-full-CRUD$ RUBYOPT='-W:no-deprecated -W:no-experimental' rails db:seed 

Exemple d'exécution :

Warning: the running version of Bundler (2.1.4) is older than the version that created the lockfile (2.2.16). We suggest you to upgrade to the version that created the lockfile by running `gem install bundler:2.2.16`.
The dependency tzinfo-data (>= 0) will be unused by any of the platforms Bundler is installing for. Bundler is installing for ruby, x86_64-linux but the dependency is only for x86-mingw32, x86-mswin32, x64-mingw32, java. To add those platforms to the bundle, run `bundle lock --add-platform x86-mingw32 x86-mswin32 x64-mingw32 java`.
Warning: the running version of Bundler (2.1.4) is older than the version that created the lockfile (2.2.16). We suggest you to upgrade to the version that created the lockfile by running `gem install bundler:2.2.16`.
Resetting auto increment ID for users to 1
Resetting auto increment ID for cities to 1
Resetting auto increment ID for gossips to 1
Resetting auto increment ID for tags to 1
Resetting auto increment ID for join_table_tag_gossips to 1
Resetting auto increment ID for private_messages to 1
Resetting auto increment ID for join_table_recipient_pms to 1
Resetting auto increment ID for comments to 1
gossip1 author_id : 5
gossip2 author_id : 10
gossip1 author_id : 6
gossip2 author_id : 11
gossip1 author_id : 7
gossip2 author_id : 3
gossip1 author_id : 5
gossip2 author_id : 5
gossip1 author_id : 5
gossip2 author_id : 2
gossip1 author_id : 5
gossip2 author_id : 8
gossip1 author_id : 8
gossip2 author_id : 4
gossip1 author_id : 8
gossip2 author_id : 6
gossip1 author_id : 10
gossip2 author_id : 7
gossip1 author_id : 4
gossip2 author_id : 9

11 users créés :
ID | FIRST_NAME | LAST_NAME | EMAIL                       | AGE | DESCRIPTION                    | CITY.NAME            | CITY.ZIP_CODE
---|------------|-----------|-----------------------------|-----|--------------------------------|----------------------|--------------
1  | Anonymous  | Anonymous | anonymous@gmail.com         | 91  | Utilisateur créé afin qu'il... | Paris                | 75000        
2  | Chantal    | Adam      | sherrie@yahoo.fr            | 105 | k3juav4xr86hi06f60sblc1hh3n... | Châtellerault        | 86242        
3  | Daphné     | Lucas     | karima.johnston@gmail.com   | 30  | pw6w148q1xef7vhkfwaz2h8bnyt... | Gagny                | 94187        
4  | Lauriane   | Tessier   | harland@hotmail.fr          | 79  | 5v8zwgdldb1qs4l06is51pjtoxe... | Sainte-Marie         | 33998        
5  | Audrey     | Colin     | shonna_daniel@gmail.com     | 90  | 8l0javl4mr8zwj17lfz5t0fpw0w... | Le Perreux-sur-Marne | 44103        
6  | Aline      | Roy       | clay@hotmail.fr             | 72  | ofjrqx6vu5b4do5ypu4i8q18hen... | Troyes               | 33810        
7  | Hilaire    | Lecomte   | verona.nienow@gmail.com     | 69  | 84sr19rel9gbcts6zoqpoamsrsz... | Montrouge            | 83458        
8  | Althée     | Mercier   | jacquline.schimmel@yahoo.fr | 78  | dbd0hze87ht50zk1vcccri7ej8p... | Asnières-sur-Seine   | 25811        
9  | Arsinoé    | Marty     | hank.zulauf@gmail.com       | 15  | bc657f3vpn612ihmuivbexm7wvm... | Metz                 | 67305        
10 | Sabine     | Le Gall   | hunter@gmail.com            | 27  | 1lh7zvne7ng1ofx7soqqn2ycjxi... | Sète                 | 57295        
11 | Éliette    | Cousin    | elvina.denesik@yahoo.fr     | 88  | 6qtdjwuwo0w5nw1iv37l79br8bt... | Maisons-Alfort       | 81785        

11 cities créées :
ID | NAME                 | ZIP_CODE | CREATED_AT              | UPDATED_AT             
---|----------------------|----------|-------------------------|------------------------
1  | Paris                | 75000    | 2021-05-12 16:34:51     | 2021-05-12 16:34:51    
2  | Châtellerault        | 86242    | 2021-05-12 16:34:53     | 2021-05-12 16:34:53    
3  | Gagny                | 94187    | 2021-05-12 16:34:53     | 2021-05-12 16:34:53    
4  | Sainte-Marie         | 33998    | 2021-05-12 16:34:53     | 2021-05-12 16:34:53    
5  | Le Perreux-sur-Marne | 44103    | 2021-05-12 16:34:53     | 2021-05-12 16:34:53    
6  | Troyes               | 33810    | 2021-05-12 16:34:53     | 2021-05-12 16:34:53    
7  | Montrouge            | 83458    | 2021-05-12 16:34:53     | 2021-05-12 16:34:53    
8  | Asnières-sur-Seine   | 25811    | 2021-05-12 16:34:53     | 2021-05-12 16:34:53    
9  | Metz                 | 67305    | 2021-05-12 16:34:53     | 2021-05-12 16:34:53    
10 | Sète                 | 57295    | 2021-05-12 16:34:53     | 2021-05-12 16:34:53    
11 | Maisons-Alfort       | 81785    | 2021-05-12 16:34:53     | 2021-05-12 16:34:53    

20 gossips créés :
ID | TITLE      | CONTENT                        | AUTHOR.FIRST_NAME | AUTHOR.LAST_NAME | TAGS.TITLE 
---|------------|--------------------------------|-------------------|------------------|------------
1  | Xq1ijon    | Unde expedita et. Sit aut q... | Audrey            | Colin            | #minus     
2  | 02caekf7ks | Molestiae fugit tempore. Ap... | Sabine            | Le Gall          | #minus     
3  | Yf45vbp    | Ipsa nihil accusantium.        | Aline             | Roy              | #asperiores
4  | H9t4r1ymr7 | Illo omnis a. Ratione sit m... | Éliette           | Cousin           | #asperiores
5  | J4i56q2    | Ab rerum at.                   | Hilaire           | Lecomte          | #ea        
6  | Sf2lf91wpb | Labore facere eligendi. Qui... | Daphné            | Lucas            | #ea        
7  | Li5y2fl    | Dolorem ut consequuntur. Fa... | Audrey            | Colin            | #vel       
8  | 5k9pd0ytok | Libero saepe eius. Corrupti... | Audrey            | Colin            | #vel       
9  | Zbzxbgr    | Rem tempora libero. Optio e... | Audrey            | Colin            | #omnis     
10 | 83t0pip8dq | Laudantium magni et.           | Chantal           | Adam             | #omnis     
11 | 8ia76r9    | Magnam pariatur ex. Fugiat ... | Audrey            | Colin            | #qui       
12 | Qwzki53fvg | Rem voluptas assumenda. Id ... | Althée            | Mercier          | #qui       
13 | Sb5omzd    | Magni non voluptates.          | Althée            | Mercier          | #enim      
14 | 5dvdx8gqhg | Iste voluptatum eum. Est co... | Lauriane          | Tessier          | #enim      
15 | Lnpo7ik    | Aut natus aut.                 | Althée            | Mercier          | #illo      
16 | 84qdbfiq0y | Eaque natus beatae. Sed nul... | Aline             | Roy              | #illo      
17 | 9sdcdg7    | Vitae molestiae aliquam.       | Sabine            | Le Gall          | #sint      
18 | 6yr4nak93r | Ipsa velit sit. Ut nisi neq... | Hilaire           | Lecomte          | #sint      
19 | Euokbeb    | Ipsa et facilis.               | Lauriane          | Tessier          | #quasi     
20 | N30vldcmtt | Ad omnis maxime. Qui porro ... | Arsinoé           | Marty            | #quasi     

10 tags créés :
ID | TITLE      
---|------------
1  | #minus     
2  | #asperiores
3  | #ea        
4  | #vel       
5  | #omnis     
6  | #qui       
7  | #enim      
8  | #illo      
9  | #sint      
10 | #quasi     

10 private messages créés :
ID | CONTENT                        | SENDER.FIRST_NAME | SENDER.LAST_NAME | RECIPIENTS.FIRST_NAME | RECIPIENTS.LAST_NAME
---|--------------------------------|-------------------|------------------|-----------------------|---------------------
1  | Id corporis fugiat. Aut und... | Hilaire           | Lecomte          | Chantal               | Adam                
2  | Necessitatibus sit fugiat. ... | Arsinoé           | Marty            | Daphné                | Lucas               
3  | Excepturi deleniti numquam.... | Hilaire           | Lecomte          | Hilaire               | Lecomte             
4  | Voluptatem nihil laboriosam... | Audrey            | Colin            | Chantal               | Adam                
5  | Quibusdam voluptatem dignis... | Sabine            | Le Gall          | Sabine                | Le Gall             
6  | Maxime amet assumenda. Qui ... | Sabine            | Le Gall          | Althée                | Mercier             
7  | Aspernatur ab commodi. Labo... | Éliette           | Cousin           | Aline                 | Roy                 
8  | Consectetur animi eaque. Ad... | Aline             | Roy              | Daphné                | Lucas               
9  | Perferendis eos saepe. Aut ... | Audrey            | Colin            | Chantal               | Adam                
10 | Deserunt et voluptas.          | Hilaire           | Lecomte          | Aline                 | Roy                 

20 comments créés :
ID | CONTENT                        | AUTHOR.FIRST_NAME | AUTHOR.LAST_NAME | GOSSIP.TITLE
---|--------------------------------|-------------------|------------------|-------------
1  | Sit corporis eius.             | Sabine            | Le Gall          | 02caekf7ks  
2  | Quos consequatur dolores. A... | Chantal           | Adam             | Xq1ijon     
3  | Repellendus aliquam consequ... | Sabine            | Le Gall          | J4i56q2     
4  | Voluptas temporibus ipsum.     | Althée            | Mercier          | 83t0pip8dq  
5  | Earum ratione nam. Est fugi... | Arsinoé           | Marty            | 02caekf7ks  
6  | Quia temporibus cumque. Pla... | Éliette           | Cousin           | Sf2lf91wpb  
7  | Necessitatibus accusantium ... | Arsinoé           | Marty            | 5k9pd0ytok  
8  | Earum excepturi quisquam. E... | Daphné            | Lucas            | Zbzxbgr     
9  | Excepturi maxime occaecati.... | Éliette           | Cousin           | 8ia76r9     
10 | Fuga suscipit aut. Incidunt... | Althée            | Mercier          | Yf45vbp     


* How to run the server
 
ln-the-gossip-project-full-CRUD$ RUBYOPT='-W:no-deprecated -W:no-experimental' rails server

* Application URL

http://localhost:3000/
