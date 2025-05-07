# SQL-Bewerbung
-- Wer bin ich?
CREATE TABLE ueber_mich (
id INT PRIMARY KEY AUTO_INCREMENT,
vorname VARCHAR(50),
nachname VARCHAR(50),
alter INT,
email VARCHAR(200),
anschrift TEXT,
geburtsdatum DATE,
telefonnummer VARCHAR(20)
);
INSERT INTO ueber_mich (vorname, nachname, alter, email, anschrift, geburtsdatum,
telefonnummer)
VALUES (
'Maher', 'Ghazzawi', 23, 'maherghazzawi2@gmail.com',
'Hospitalstraße 21, 35216 Biedenkopf', '2001-11-12', '+49 1520 3228 755'
);
-- Was kann ich?
CREATE TABLE faehigkeiten (
id INT PRIMARY KEY AUTO_INCREMENT,
programmiersprache VARCHAR(50),
projekt_beschreibung TEXT,
github_link TEXT,
erklaerung_code TEXT);

INSERT INTO faehigkeiten (programmiersprache, projekt_beschreibung, github_link,
erklaerung_code)
VALUES (
'Python',
'Ein Tool zur Verschlüsselung und Entschlüsselung von Nachrichten.',
'https://github.com/MaherGhazzawi/Caeser-Code/blob/main/README.md?plain=1',
'Im Link erkläre ich, wie mein Python-Code mit dem
Caesar-Verschlüsselungsverfahren funktioniert.'
);
-- Verbindung herstellen: Ich und meine Skills
SELECT * FROM ueber_mich
CROSS JOIN faehigkeiten;
