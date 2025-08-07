USE LibraryDB;
SELECT * FROM Books;
SELECT Title, Genre FROM Books;
SELECT * FROM Authors
WHERE Country = 'India';
SELECT * FROM Books
WHERE PublishedYear BETWEEN 2000 AND 2010;
SELECT * FROM Books
WHERE Genre LIKE '%Fiction%';
SELECT * FROM Members
WHERE MembershipDate > '2022-01-01';
SELECT * FROM Members
WHERE Name LIKE 'A%';
SELECT * FROM Borrow
ORDER BY BorrowDate DESC
LIMIT 2;
SELECT B.Title, A.Name AS Author
FROM Books B
JOIN Authors A ON B.AuthorID = A.AuthorID;
SELECT * FROM Borrow
WHERE ReturnDate IS NULL;
SELECT * FROM Staff
ORDER BY Role DESC;
SELECT DISTINCT Genre FROM Books;
SELECT * FROM Staff
WHERE Role = 'Librarian';
SELECT * FROM Staff
WHERE Role IN ('Librarian', 'Assistant');
SELECT Name AS MemberName, Email AS EmailID
FROM Members;
SELECT * FROM Members
WHERE Email LIKE '%@gmail.com';
