Έκδοση Αποτελεσμάτων Εκλογών
============================

Σκοπός της εργασίας είναι η συγγραφή προγραμμάτων σε γλώσσα Java για
την έκδοση αποτελεσμάτων εκλογών σύμφωνα με τη μέθοδο Schulze.

Η εργασία είναι προσωπική.

Κάθε φοιτητής θα εργαστεί στο προσωπικό του αποθετήριο στο GitHub. Για
να αξιολογηθεί μια εργασία θα πρέπει να πληροί τις παρακάτω
προϋποθέσεις:

1. Όλη η εργασία θα πρέπει να βρίσκεται σε έναν κατάλογο
  ``assignment-3`` μέσα στο αποθετήριο του φοιτητή.

2. Ο πηγαίος κώδικας του προγράμματος που θα γραφτεί θα πρέπει να βρίσκεται
  σε έναν υποκατάλογο ``src`` του καταλόγου ``assignment-3``.

3. Για τη συγγραφή του κώδικα απαιτείται η χρήση της βιβλιοθήκης
   [json.jar](https://github.com/dmst-algorithms-course/assigmnent-3/blob/master/json.jar)
   η οποία θα πρέπει να τοποθετηθεί σε έναν υποκατάλογο ``lib``
   του καταλόγου ``assignment-3``.
   Το αρχείο ``json.jar`` είναι η μεταγλωττισμένη βιβλιοθήκη JSON από το
   [JSON.org](http://www.json.org/java/)

4. Ο μεταγλωττισμένος κώδικας του προγράμματος που θα γραφτεί θα
  πρέπει να βρίσκεται σε έναν υποκατάλογο ``bin`` του καταλόγου
  ``assignment-2``. Έτσι, αν το αποθετήριο του φοιτητή είναι το
  ``example-repo``, η δομή των καταλόγων θα είναι:
    ```
    example-repo
        assignment-3
            src
            lib
            bin
    ```
5. Το πρόγραμμα θα πρέπει να έχει όνομα ``Schulze``.

6. Το πρόγραμμα θα πρέπει να εκτελείται ως εξής:
    ``` 
    java Schulze example_elections.json
    ```
    Η έξοδος θα πρέπει είναι της μορφής:
    ```
    a = 1 [c]
    b = 2 [a, c]
    c = 0 []
    d = 3 [a, b, c]    
    ```
    Το οποίο σημαίνει ότι ο υποψήφιος d επικρατεί επί τριών άλλων υποψηφίων,
    που παρατίθενται στη συνέχεια, ο υποψήφιος b επικρατεί επί δύο
    άλλων υποψηφίων, ο υποψήφιος a επικρατεί
    επί ενός άλλου υποψηφίου, και ο υποψήφιος c δεν επικρατεί έναντι κανενός
    υποψηφίου.
    
6. Τα αρχεία που θα δίνονται στον πρόγραμμα θα έχουν την εξής μορφή:
   ```
   {
       "candidates": [
           "a", "b", "c", "d"
       ],
       "ballots": [
           [0, 2, 3, 1],
           [0, 2, 3, 1],
           [0, 2, 3, 1],
           [0, 2, 3, 1],
           [0, 2, 3, 1],
           [0, 2, 3, 1],

           [1, 0, 3, 2],
           [1, 0, 3, 2],
           [1, 0, 3, 2],
           [1, 0, 3, 2],
        
           [2, 3, 1, 0],
           [2, 3, 1, 0], 
           [2, 3, 1, 0],

           [3, 1, 0, 2],
           [3, 1, 0, 2], 
           [3, 1, 0, 2],
           [3, 1, 0, 2],        

           [3, 2, 1, 0],
           [3, 2, 1, 0],        
           [3, 2, 1, 0],
           [3, 2, 1, 0]
       ]
    }
   
Αν μια εργασία δεν ικανοποιεί τις παραπάνω απαιτήσεις ***δεν θα είναι
δυνατή η αξιολόγησή της***. Επιβεβαιώστε λοιπόν ότι πράγματι το
πρόγραμμά σας μπορεί να κληθεί ***ακριβώς*** με τις εντολές που δίνονται
παραπάνω, και ότι παράγει ***ακριβώς*** την έξοδο που περιγράφεται.

Ο μεταγλωττισμός των αρχείων σας θα γίνεται με μία εντολή της μορφής:
    ```
    javac -cp ".:lib/json.jar" *.java
    ```

Αντίστοιχα, η εκτέλεση του προγράμματός σας θα πρέπει να γίνεται με την εντολή:
    ```
    java -cp ".:lib/json.jar" Schulze example_elections.json
    ```

Για να ελέγξετε το πρόγραμμά σας μπορείτε να χρησιμοποιήσετε τα αρχεία:

* [example_elections.json](https://github.com/dmst-algorithms-course/assigmnent-3/blob/master/example_elections.json)

* [schulze_1.json](https://github.com/dmst-algorithms-course/assigmnent-3/blob/master/schulze_1.json)

