# WriteUps for CSoC Infosec Week - 1

## Challenge 1 - picoCTF Challenges

### 1. Information 
 
    first extract Metadata by running exif in temrinal by using exiftool,
    the license has a string which looks like base64, decode it using cyberchef on google 

 ### 2. Matryoshka doll 
 first download the doll image and then go to the terminal and below are all the commands i ran for the flag 

    cd Downloads/
    ls 
    binwalk -e dolls.jpg
    ls
    cd _dolls.jpg.extracted/
    ls
    cd base_images
    ls
    binwalk -e 2_c.jpg

    continue the above process till you get an extracted file _4_c.jpg.extracted 

    cd _4_c.jpg.extracted 
    ls
    cat flag.txt 

### 3. tunn3l v1s10n
first Download the file given and then head to as usual terminal and open the dowloads folder 

    hexedit tunn3l_v1s10n
    
    look at the headers and copy them and go google, it's bitmap file 

    now change the extenion of the file 

    mv tunn3l_v1s10n tunn3l_v1s10n.bmp
    eog tunn3l_v1s10n.bmp

    file won't open as it is corrupted so repair it in a hexeditor by comparing it to a sample.bmp i downloaded from google

    after repairing the bad bytes it was wriitten in place of bytes so edited the byte entries 

    eog tunn3l_v1s10n.bmp

    pic opens and it gives a msg but however the image feels a bit small so readjust the size by changing the bits for height of the image 

    for bytes reponsibl for the size go google and search file signatures and then go to wikipedia and locate the .BMP file and look for the info 

    after repairing it we get to see the flag 

### 4. MacroHard WeakEdge 
i took a bit of hint from challenge and looked for Macros using olevba but found nothing and then searched about ppts on gpt and it told me that .ppt files are also zip file so then i took the below approach 

    unzip Forensics\ is\ fun.pptm
    cd /ppt/slideMasters/
    cat Hidden     (it gives a string )
    echo "<string>" | tr -d ' ' 
    
    now copy the string decode it using a base64 decoder on cyberchef 

### 5. Enhance 

    strings drawing.svg

    look carefully in the ending you will find a closing brace with a string inside and now look for opening brace now see a pattern you will se picoCTF written there

    strings drawing.svg | grep "tspan"

    now write the flag manually 

### 6. Advanced-potion-making 

    open the file in hexeditor and copy the headers and go google, the header is closest match to a png image and now change the extension.
    
    also you will see that 12 13 14 bytes are corrupted when you comapare them with a sample .png image so edit them too.

    open the image, you will see a complete red color image, to check for layers go to Aperisolve and check it and after analysis you will get the flag 

### 7. File types 

    sh FLAG.pdf
    file flag 
    mv flag flag.ar
    ar -x flag.ar
    ls 
    fie flag
    mv flag flag.cpio 
    cpio -idmv < flag.cpio 
    ls
    file flag
    mv flag flag.bz2
    bzip2 -d flag.bz2
    file flag
    mv flag flag.gz
    gzip -d flag.gz 

    repeat like this till you get flag with ASCII text 

    copy the hex inside the flag and convert it to ASCII text from cyberchef on google 

### 8. hideme

    ls 
    binwalk -e flag.png 
    ls 
    cd _flag.png.extracted 
    ls 
    cd secret/
    ls 
    eog flag.png 

### 9. MSB 

    search google for python image steganography 
    and then do the RGB analysis of the image in StegSolve 
    and then copy the text 

    vim 
    paste the text here then 

    vim/ picoCTF

    you will get the flag 

### 10. extensions

    ls
    cat flag.txt
    file flag.txt
    mv flag.txt flag.png 
    eog flag.png 


## Challenge 2 - Sakura Room 

### Task 1

    simply copy the "Let's Go!" and paste it as answer

### Task 2

    wget <link>
    ls 
    exiftool sakurapwnedletter.svg

    now look at the path you will se the username SakuraSnowAngelAiko

### Task 3

    google the username SakuraSnowAngelAiko 
    go to the github page 
    go to the PGP repo 
    there is a pgp key now convert the pgp key to ascii text and then you will get the email 

    and as for the real name go back to the search results on google you will see a twitter account scroll down her posts there she has mentioned her other account which has her real name Aiko Abe 

### Task 4

    in the same git page go to Repos and 
    open ETH then open mining script then click on history and then open the "create miningscript" 
    there you will get the address of the wallet 

    now for cryptocurrency just search the address on google and you will get to know that attacker was dealing in Ethereum 

    now you can also see his transactions and sort them by date, now look for the asked date and see the mining pool - Ethermine 

    for exchanges look for outgoing payements and see the transactions you will find thate exchange was in Tether 

### Task 5 

    like i googled before the username i found a twitter page and there is her twitter handle SakuraLoverAiko 

    use the hint on side pane and copy the url and paste it as answer 

    and as for wifi bssid use the previous hint to retrive the SSID from git scrnshot and then head to google type search bssid by ssid you will find a site Wigle and now just enter the SSID and you can locate her home and can get her BSSID

### Task 6

    as for the airport asked about first take a look in the picture and zoom it to the monumnent in the back, it's the Washington Monumnent if you don't know about it you can also do reverse image search of the monumnent on google and now search of the airport in Washinton DC it's the DCA 

    for the first layover look at the image carefully it's the first class suite of Japanese Airlines you can just search it on google JAL first class lounge Sakura lounge you will find an image of the lounge which is at Haneda airport mentioned on the image site 

    for the lake see the japanese map and try to math out the topography and curves of the map pic posted on twitter and you will find that the lake is Inwashiro lake 

    and as for her home when you found her BSSID on wigle you can find that she lives is Hirosaki 


## Challenge 2 - OSIT Exercise by Sofia Santos 

### Exercise 6 

    just search the image by google lens and you will find many image links showing that it was the image of car bomb blast in IRAQ by AL-Qaeda 

### Exercise 4

    for resort name again use google image search and then you will find an exact image with a facebook account so you get the name - OAN Resort

    and now just search OAN resort, OAN island, Wonip 
    you will find it and now just get the coordinates from here - 7.362829221264985, 151.75644754123084

    as for direction of camera go to google earth and paste the coordinates and now try to adjust your view according to the image and you will find that the camera is facing N-W direction 

### Exercise 3

    location - search the image on google img search and yandex image searh you will find on of the article mentioning about the Presidential complex of turkey and to confirm go to google maps and look at the entrance of the Presidential complex of Turkey, it matches 
    and thus from google maps you can also get the coordinates 

### Exercise 14

    search for Earthquakes in september 2016 on google and look for the same date and around the same time of the video on the site Volcandiscovery then you will find that it was an earthquake of magnitude 5.8 18kms away from Romania in Vrancea and now google search again Vrancea earthquake 2016 video and look for it you will find exactly same video with the caption Cutremur Chisinau, translate it and you find it was recorded in Chisinau, Moldova

    and now search the building which you can see in the background you will find out about a karoke centre of the builing which is located on Centre -Bd constantin Negruzz 2/4 and then search for it in google maps and now you will find the building which is Atrium Shopping centre
    now google street view try to find the best possible location and you will see that camera wasmost probably installed on V Continental Business Centre 

### Exercise 26 
following the order of the archive in numbering the images  

     1st image - use google lens and you will get the result Chorsu Bazaar 

     2nd image - just use google lens you will get the  answer Anhor lokomotiv park 

     3rd image - time for brainstorming, you won't get it directly from google image search or yandex but all you can make it from now is that the person is still in Tashkent and is going from Anhor lokomotiv to railway station as the 1st video was a train video
     so now look around you will see a samsung galaxy board, Navien Board and a cut out 'O' sign, bus stops and a subway entrance (i guess) so search on the route from the park to railway station on the google map where you can find something ending with 'O' and bustop with Kapital Bank poster and subway entrance together so now on google street view after so much narrowing down i found this place near Oybek metro station and the 'O' poster is actually VERO written on it. here in this case he was most probably travelling by taxi 

     4th file (video) - looking at the video notice 2 things 1st is the railway crossing and Mountains with strange Lines so for this look in the Uzbekistan Map along with Railway map as train direction is required and so wtih elimation we make out that the train is heading S-W direction and the crossing is somehwere near Jizzakh region probably 
     and most Probably train is Afrosiyob travelling at 210 Km/hr
     also the train station from which user boarded was Stantsiya Tashkent Pass Tsentr.

     5th img - unable to find anything about it 





