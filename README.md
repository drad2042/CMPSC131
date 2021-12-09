# CMPSC131

Booklist.txt includes a line for each book in the library in the following form:

<book name>#<number of copies>#<restricted>

Where <book name> indicates the name of the book, <number of copies indicates> how many copies the library has and <restricted> is a TRUE/FALSE value indicating if the book has borrowing restrictions.

For example if booklist.txt contains

Introduction to python#3#TRUE

Eye of the world#1#FALSE

it means 

The library has 3 copies of Introduction to python and it has borrowing restrictions. It also has one copy of Eye of the world and there are no borrowing restrictions for that book. Borrowing restrictions for a book means the book can be borrowed for at most 7 days. Books with no borrowing restrictions can be borrowed for upto 28 days.

 

Next we are given a log of the library's working in the form of librarylog.txt . Each line of text of the log is of one of the following types:

1) Borrow notation

B#<day>#<Student Name>#<Book name>#<days borrowed for>

2) Return notation

R#<day>#<Student Name>#<Book name>

3) Book addition

A#<day>#<Book name>

4) Fine pay notation

P#<day>#<student name>#<amount>

 

For example a librarylog.txt which has

B#1#adam#harry potter#6

R#10#adam#harry potter

A#11#Introduction to programming

P#15#adam#5

 

indicates adam borrowed harry potter on day 1 for 6 days. Adam then returned harry potter on day 10 (he was thus 3 days late). On day 11 a copy of introduction to programming was added to the library. Finally on day 15 adam paid 5 dollors towards the owed library fine dues.

The final line of librarylog.txt will include a single number which indicates the current day.

The rules of the library are :

Restricted books can be borrowed for at most 7 days. Non restricted books can be borrowed for 28 days.

Books returned late are fined 5 a day for each day late for restricted books, 1 per day late for non restricted books. 

Any library user can have at most 3 books borrowed at a time.

A library user can only borrow if they have no pending fines.

New books to the library can be added as per the log, these are in addition to the original list of books in booklist. (The added book can already exist in which case its an additional copy or can be a new book)

A book can only be borrowed if there is an unborrowed copy in the library.

 

You program should process booklist and librarylog

And be able to answer the following questions.

1) Can a student borrow a book on a particular day for a certain number of days (this depends on how many copies remain in the library, if the person has any pending fines or too many borrowed books and consider book restriction conditions)

2) What are the most borrowed/popular books in the library (How many days were they borrowed vs not borrowed) .

3) Which books have the highest borrow ratio. You have to consider how many copies are there for this also . For example if a book has 10 copies from day 1 and 1 copy was always borrowed but another book has only 2 copies and 1 copy was borrowed half the number of days. The 2nd book has more borrow ratio. Basically for how much of the books were available vs how much they got borrowed.

4) Be able to produce sorted lists of most borrowed books/ books with highest usage ratio.

5) What are the pending fines at the end of the log/at a specific day in the log.
