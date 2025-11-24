# 🌐 The Verdú Method  
### Native Cross-Database Queries in Firebird 2.5 Using `EXECUTE STATEMENT ON EXTERNAL`

> *"Una técnica que conecta España con China… sin APIs, sin replicación, solo con SQL puro."*

This repository documents a groundbreaking technique discovered by **Salvador Verdú** in **2023**, enabling **real-time queries across multiple Firebird 2.5 databases** —even across continents— using only native SQL features.

✅ No external libraries  
✅ No UDFs, no ETL, no scripts  
✅ Works with remote databases over TCP/IP  
✅ Full error handling and scalability  

---

## 🔍 ¿Qué es el *Método Verdú*?

Es una técnica que aprovecha una funcionalidad **no documentada pero operativa en Firebird 2.5**:
```sql
EXECUTE STATEMENT 'SELECT ...' 
  ON EXTERNAL '114.22.xxx.xxx:C:\ruta\base.fdb'
  AS USER 'SYSDBA' PASSWORD 'masterkey'
  INTO :var1, :var2;

🚀 [Demostración en vivo](https://olbeup.github.io/verdu-method) · 
📄 [Ejemplos completos](https://github.com/olbeup/verdu-method/tree/main/) · 
🐛 [Reporta un issue](https://github.com/olbeup/verdu-method/issues/new) · 
⭐ ¡Deja tu star si te salva la vida con Firebird!
