# Stretch Goals for the *nix Scavenger Hunt

The following goals are meant to provide a way for more experienced users to
extend their knowledge of the *nix command line.

* Use `curl` to look up the URL `https://www.imdb.com/title/tt0070948/`. The title of this film will lead you to the answer. *What is the answer?*

42
 *besides being his house number, it's also the answer to Life, the Universe, and Everything*

 -----
STEP 1:

 cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix$ curl https://www.imdb.com/title/tt0070948/ | more
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0







<!DOCTYPE html>
<html
    xmlns:og="http://ogp.me/ns#"
    xmlns:fb="http://www.facebook.com/2008/fbml">
    <head>

        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">

    <meta name="apple-itunes-app" content="app-id=342792525, app-argument=imdb:///title/tt0070948?src=mdot">



        <script type="text/javascript">var IMDbTimer={starttime: new Date().getTime(),pt:'java'};</script>

<script>
    if (typeof uet == 'function') {
      uet("bb", "LoadTitle", {wb: 1});
    }
</script>
  <script>(function(t){ (t.events = t.events || {})["csm_head_pre_title"] = new Date().getTime(); })(IMDbTimer);</script>
        <title>Zardoz (1974) - IMDb</title>
  <script>(function(t){ (t.events = t.events || {})["csm_head_post_title"] = new Date().getTime(); })(IMDbTimer);</script>
<script>
    if (typeof uet == 'function') {
      uet("be", "LoadTitle", {wb: 1});


STEP 2: 

cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix$ grep -r "Zardoz" /home/cabox/workspace/wats1030-intro-to-unix
/home/cabox/workspace/wats1030-intro-to-unix/challenge_files/test2/explicabo_dolor.txt:Aperiam ipsam perferendis ut non est. Harum numquam officia veniam eavel dolor. Unde vel vitae minima optio quas aliquam vel. Enim voluptatem autem culpa saepe. Alias ipsa Zardoz praesentium occaecati qui quaerat voluptas.

STEP 3:

cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix$ cd challenge_files/test2
cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix/challenge_files/test2$ more explicabo_dolor.txt
Quis autem aliquam sequi dolorem ipsum consequatur pariatur. Tenetur optio minus consequuntur molestias non. Et ad rerum delectus reprehenderit quia esse qui
a nihil.
Aperiam ipsam perferendis ut non est. Harum numquam officia veniam ea vel dolor. Unde vel vitae minima optio quas aliquam vel. Enim voluptatem autem culpa sa
epe. Alias ipsa Zardoz praesentium occaecati qui quaerat voluptas.
Velit qui dolores eos est. Et itaque qui numquam rerum sit. Voluptatum qui inventore sequi delectus ut soluta et.
Aut autem quo aliquam hic tempora. Odio qui saepe consequatur consequatur molestiae. Rem quod magnam doloribus sed omnis.
Tempore ut corrupti deleniti rerum exercitationem. Provident eligendi quaerat non molestias animi dolor amet. Fugiat sint cum sit ut possimus.

serial-numbers/quia_id.txt

STEP 4:

cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix/challenge_files/test2$ cd ..
cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix/challenge_files$ ls
01                       Beverlee-Moen.user      credit_cards.txt       Harland-Schoen.user     Lilly-Kohler.user      Rosalind-Wisozk.user
2015_special_stuff.demo  Brad-Thiel.user         Dannielle-Green.user   Harrell-Quitzon.user    Lissie-Strosin.user    Rosena-Simonis.user
Afton-Jast.user          Brayan-Douglas.user     Deedee-Jacobson.user   Hillard-Ziemann.user    Mannie-Ritchie.user    Sandie-Balistreri.user
Aimee-Maggio.user        Bria-Satterfield.user   Desiree-Marks.user     Isadora-Leffler.user    Masako-Lind.user       scooter-double-mamba.demo
Alfonso-Gottlieb.user    Bridgette-Reichel.user  Deven-Rutherford.user  Jaxen-Gleichner.user    Melisa-Yundt.user      serial-numbers
Allen-Kemmer.user        Britta-Hammes.user      Doyle-Jones.user       Jayme-Rodriguez.user    Michelina-Kuphal.user  Sharen-Hansen.user
Almina-Cormier.user      Britt-Erdman.user       Dustyn-O'Connell.user  Jenni-O'Connell.user    Minnie-Jacobi.user     Sherrill-Russel.user
Alta-Lemke.user          Bryant-Kuhic.user       Elza-Mraz.user         Johny-Borer.user        Murdock-Leffler.user   Sherwin-Kovacek.user
Amina-McGlynn.user       Bryton-Aufderhar.user   Emory-Crona.user       Kassandra-Barrows.user  Mychal-Corkery.user    Sherwood-Rath.user
Anabel-Hammes.user       Caitlin-Grady.user      Erin-Walker.user       Keely-Hilpert.user      Nakita-Nader.user      Shyheim-Murazik.user
Ancel-Conn.user          Carroll-Hartmann.user   Estela-Schultz.user    Kenyatta-Hickle.user    Nayely-Dare.user       Siobhan-Kirlin.user
Anjali-Halvorson.user    Claudie-McClure.user    Fernanda-Tromp.user    Kiana-Kulas.user        Nicholas-Strosin.user  test2
Ardath-Kuvalis.user      Clemente-Haley.user     files.txt              Kirstin-Hoppe.user      Niles-Runte.user       tmp
Avah-Dickinson.user      Cleo-VonRueden.user     Fletcher-Rice.user     Kwame-Schmitt.user      Nina-Sporer.user       Tomas-Kutch.user
Ayaan-Stiedemann.user    cloaked-wookie.demo     Fred-Ryan.user         Ladonna-Lueilwitz.user  Noreta-Steuber.user    wow
Aylin-Grant.user         Codie-Romaguera.user    Genie-Abshire.user     Lala-Will.user          Ovid-Bogan.user
Bedford-Sipes.user       Cooper-Reynolds.user    Grace-Tromp.user       Leia-Hudson.user        Randell-Sauer.user
Benita-King.user         Corrie-Bogisich.user    Grant-Cronin.user      Leia-Ziemann.user       Remy-Renner.user
Benito-Stoltenberg.user  credit_cards2.txt       Hali-Roob.user         Lillard-Purdy.user      Ronna-Hermann.user
cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix/challenge_files$ cd /serial-numbers
-bash: cd: /serial-numbers: No such file or directory
cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix/challenge_files$ cd serial-numbers
cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix/challenge_files/serial-numbers$ more quia_id.txt
Where are those droids you are looking for?

Et inventore sit omnis quidem quas dolor. Voluptas recusandae modi quia. Quo aliquid sunt libero eveniet et veniam vitae ipsum. Voluptatibus at ut nobis amet
.
Est dolore quibusdam quaerat voluptate dicta. Velit omnis omnis aut harum ut corporis vero. Consequatur commodi doloribus dolorem illo repellendus nostrum se
d vel.
Voluptas sunt rerum excepturi officiis fugit eum ratione molestiae. Tempore enim consectetur dolores nobis tempore quibusdam temporibus ut. Quos ullam exerci
tationem sit ratione. Nihil odio est vel dolores.
Incidunt laboriosam officiis culpa. Aspernatur distinctio dolores temporibus sunt. Voluptates recusandae saepe perferendis quo omnis.
Autem deserunt aut ut eaque ut iusto. Delectus architecto voluptates veniam odio provident. Eveniet voluptatum officiis cum tempora. Tempore eligendi dolore
quasi quo architecto non.

STEP 5:

cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix$ grep -r "droids" /home/cabox/workspace/wats1030-intro-to-unix
/home/cabox/workspace/wats1030-intro-to-unix/challenge_files/serial-numbers/quia_id.txt:Where are those droids you are looking for?
/home/cabox/workspace/wats1030-intro-to-unix/challenge_files/01/maiores_quaerat.txt:Quas nulla sit et vitae ut omnis iste. The droids you are looking for are found in the difference between maiores_quaerat.txt and maiores_quaerat2.txt. Rem quis harum sequi dolore accusantium omnis. Nam ea eum molestiae quia sequi. Libero molestiae reiciendis repellendus quod eaque.
/home/cabox/workspace/wats1030-intro-to-unix/challenge_files/01/maiores_quaerat2.txt:Quas nulla sit et vitae ut omnis iste. The droids you are looking for are found in the difference between maiores_quaerat.txt and maiores_quaerat2.txt. Rem quis harum sequi dolore accusantium omnis. Nam ea eum molestiae quia sequi. Libero molestiae reiciendis repellendus quod eaque.
/home/cabox/workspace/wats1030-intro-to-unix/challenge_files/01/autem_repellat.txt:Quas nulla sit et vitae ut omnis iste. The droids you are looking for arefound in the difference between maiores_quaerat.txt and maiores_quaerat2.txt. Rem quis harum sequi dolore accusantium omnis. Nam ea eum molestiae quia sequi. Libero molestiae reiciendis repellendus quod eaque.

STEP 6: 

cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix$ cd challenge_files/01
cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix/challenge_files/01$ diff maiores_quaerat.txt maiores_quaerat2.txt
1a2
> tmp/
5a7
> ipsa
8a11
> _ut
9a13
> .txt

STEP 7:

cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix/challenge_files/01$ cd ..
cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix/challenge_files$ cd tmp
cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix/challenge_files/tmp$ more ipsa_ut.txt
Find the house number for Jayme Rodriguez. That is the answer.

STEP 8: 

cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix/challenge_files/tmp$ cd ..
cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix/challenge_files$ ls
01                       Beverlee-Moen.user      credit_cards.txt       Harland-Schoen.user     Lilly-Kohler.user      Rosalind-Wisozk.user
2015_special_stuff.demo  Brad-Thiel.user         Dannielle-Green.user   Harrell-Quitzon.user    Lissie-Strosin.user    Rosena-Simonis.user
Afton-Jast.user          Brayan-Douglas.user     Deedee-Jacobson.user   Hillard-Ziemann.user    Mannie-Ritchie.user    Sandie-Balistreri.user
Aimee-Maggio.user        Bria-Satterfield.user   Desiree-Marks.user     Isadora-Leffler.user    Masako-Lind.user       scooter-double-mamba.demo
Alfonso-Gottlieb.user    Bridgette-Reichel.user  Deven-Rutherford.user  Jaxen-Gleichner.user    Melisa-Yundt.user      serial-numbers
Allen-Kemmer.user        Britta-Hammes.user      Doyle-Jones.user       Jayme-Rodriguez.user    Michelina-Kuphal.user  Sharen-Hansen.user
Almina-Cormier.user      Britt-Erdman.user       Dustyn-O'Connell.user  Jenni-O'Connell.user    Minnie-Jacobi.user     Sherrill-Russel.user
Alta-Lemke.user          Bryant-Kuhic.user       Elza-Mraz.user         Johny-Borer.user        Murdock-Leffler.user   Sherwin-Kovacek.user
Amina-McGlynn.user       Bryton-Aufderhar.user   Emory-Crona.user       Kassandra-Barrows.user  Mychal-Corkery.user    Sherwood-Rath.user
Anabel-Hammes.user       Caitlin-Grady.user      Erin-Walker.user       Keely-Hilpert.user      Nakita-Nader.user      Shyheim-Murazik.user
Ancel-Conn.user          Carroll-Hartmann.user   Estela-Schultz.user    Kenyatta-Hickle.user    Nayely-Dare.user       Siobhan-Kirlin.user
Anjali-Halvorson.user    Claudie-McClure.user    Fernanda-Tromp.user    Kiana-Kulas.user        Nicholas-Strosin.user  test2
Ardath-Kuvalis.user      Clemente-Haley.user     files.txt              Kirstin-Hoppe.user      Niles-Runte.user       tmp
Avah-Dickinson.user      Cleo-VonRueden.user     Fletcher-Rice.user     Kwame-Schmitt.user      Nina-Sporer.user       Tomas-Kutch.user
Ayaan-Stiedemann.user    cloaked-wookie.demo     Fred-Ryan.user         Ladonna-Lueilwitz.user  Noreta-Steuber.user    wow
Aylin-Grant.user         Codie-Romaguera.user    Genie-Abshire.user     Lala-Will.user          Ovid-Bogan.user
Bedford-Sipes.user       Cooper-Reynolds.user    Grace-Tromp.user       Leia-Hudson.user        Randell-Sauer.user
Benita-King.user         Corrie-Bogisich.user    Grant-Cronin.user      Leia-Ziemann.user       Remy-Renner.user
Benito-Stoltenberg.user  credit_cards2.txt       Hali-Roob.user         Lillard-Purdy.user      Ronna-Hermann.user
cabox@wats1030-intro-to-unix:~/workspace/wats1030-intro-to-unix/challenge_files$ more Jayme-Rodriguez.user
Rodriguez, Jayme
Labadie, Rohan and Powlowski
42 Stracke Meadow
McClurestad, GU 80868

STEP 9:

Realize that the answer did not have a question because that was what Earth was supposed to be doing. Side note: I am currently rereading "The Ultimate Hitchhiker's Guide to the Galaxy" to refresh my mind before the book club meetup https://www.meetup.com/pnwbookclub/events/257092278/ 