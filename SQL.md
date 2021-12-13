
# Tables
## Doctorants table
```sql
CREATE table Doctorant (
    id_doctorant serial,
    date_debut_de_these date,
    date_de_soutenance date,
    PRIMARY KEY (id_doctorant),
    CONSTRAINT fk_personnel
       FOREIGN KEY(id_doctorant)
           REFERENCES personnel(id_personnel)
);
```
## President table
```sql
CREATE TABLE President(ID_President INT PRIMARY KEY,  
                        Constraint fk_president 
                            FOREIGN KEY (ID_president) 
                                REFERENCES scientifique(id_scientifique) ON DELETE CASCADE
);

```
