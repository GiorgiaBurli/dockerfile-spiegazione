# 🐳 Dockerfile - Spiegazione completa

Questo repository contiene la spiegazione dettagliata di cos'è un `Dockerfile`, a cosa serve e come funziona riga per riga.

---

## 📦 Cos'è un Dockerfile?

Un **Dockerfile** è un file di testo che contiene una lista di istruzioni che Docker usa per costruire un'immagine personalizzata.

È come una **ricetta** che Docker legge per costruire un contenitore pronto all'uso.

---

## 📄 Esempio di Dockerfile usato:

```Dockerfile
# Usa un'immagine base di Node.js
FROM node:14

# Imposta la cartella di lavoro
WORKDIR /usr/src/app

# Copia il file package.json e installa le dipendenze
COPY package*.json ./
RUN npm install

# Copia il resto dell'applicazione
COPY . .

# Espone la porta su cui l'app ascolta
EXPOSE 3000

# Comando per avviare l'app
CMD ["npm", "start"]
