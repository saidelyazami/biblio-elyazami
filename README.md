# biblio-elyazami

TP XML — Gestion d'une bibliothèque (Formation ING HTECH, 01-11-2026).

## Fichiers

| Fichier | Rôle |
|---|---|
| `biblio.xml` | Données : étudiants et livres empruntés |
| `biblio.dtd` | DTD de validation de `biblio.xml` |
| `biblio1.xsl` | Feuille XSLT : pour chaque étudiant, liste des livres non rendus + compteurs (empruntés / rendus / non rendus) |
| `test1.html` | Résultat HTML de la transformation XSLT |

## Exécution

```bash
# Validation DTD
xmllint --noout --valid biblio.xml

# Transformation XSLT (XSLT 2.0, ex. Saxon)
java -jar saxon-he.jar -s:biblio.xml -xsl:biblio1.xsl -o:test1.html
```
