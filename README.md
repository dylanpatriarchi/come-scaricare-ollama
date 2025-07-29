# Come Scaricare Ollama

**Ultimo aggiornamento:** 29 Luglio 2025

[Ollama](https://ollama.ai/) è un framework open-source per eseguire modelli di linguaggio localmente sul tuo computer. Questo README ti guiderà attraverso il processo di installazione su Linux, macOS e Windows.

## 📋 Prerequisiti

- **RAM:** Almeno 8GB (16GB consigliati)
- **Spazio su disco:** Almeno 10GB di spazio libero
- **Sistema operativo:** Linux, macOS 10.15+ o Windows 10/11

## 🐧 Linux

### Ubuntu/Debian
```bash
curl -fsSL https://ollama.ai/install.sh | sh
```

### Arch Linux
```bash
yay -S ollama-bin
# oppure
paru -S ollama-bin
```

### Fedora/RHEL/CentOS
```bash
curl -fsSL https://ollama.ai/install.sh | sh
```

### AppImage (Distribuzioni generiche)
1. Vai su [ollama.ai/download](https://ollama.ai/download)
2. Scarica il file `.AppImage` per Linux
3. Rendi eseguibile il file:
```bash
chmod +x ollama-linux-amd64.AppImage
```
4. Esegui:
```bash
./ollama-linux-amd64.AppImage
```

## 🍎 macOS

### Metodo 1: Installer ufficiale (Consigliato)
1. Vai su [ollama.ai/download](https://ollama.ai/download)
2. Scarica l'installer per macOS
3. Apri il file `.dmg` scaricato
4. Trascina l'app Ollama nella cartella Applicazioni
5. Avvia Ollama dall'applicazione

### Metodo 2: Homebrew
```bash
brew install ollama
```

### Metodo 3: Script di installazione
```bash
curl -fsSL https://ollama.ai/install.sh | sh
```

## 🪟 Windows

### Metodo 1: Installer ufficiale (Consigliato)
1. Vai su [ollama.ai/download](https://ollama.ai/download)
2. Scarica l'installer per Windows
3. Esegui il file `.exe` scaricato
4. Segui le istruzioni dell'installer
5. Ollama si avvierà automaticamente

### Metodo 2: Winget
```powershell
winget install Ollama.Ollama
```

### Metodo 3: Chocolatey
```powershell
choco install ollama
```

### Metodo 4: Scoop
```powershell
scoop install ollama
```

## 🚀 Verifica dell'Installazione

Dopo l'installazione, verifica che tutto funzioni:

```bash
ollama --version
```

## 📦 Scaricare il Primo Modello

Una volta installato Ollama, puoi scaricare il tuo primo modello:

```bash
# Modello base (consigliato per iniziare)
ollama pull llama3.2

# Modello più piccolo per test rapidi
ollama pull llama3.2:1b

# Modello più potente (richiede più RAM)
ollama pull llama3.2:70b
```

## 💬 Primo Test

Testa l'installazione con un semplice comando:

```bash
ollama run llama3.2 "Ciao! Come stai?"
```

## 🔧 Risoluzione Problemi

### Linux
- **Errore di permessi:** Assicurati che l'utente sia nel gruppo `docker` o esegui con `sudo`
- **Porta occupata:** Ollama usa la porta 11434, verifica che sia libera

### macOS
- **Errore di sicurezza:** Vai su Preferenze di Sistema > Sicurezza e Privacy per permettere l'esecuzione
- **Problemi con Homebrew:** Prova `brew update && brew upgrade ollama`

### Windows
- **WSL2 richiesto:** Assicurati che WSL2 sia installato e configurato
- **Antivirus:** Aggiungi Ollama alle eccezioni del tuo antivirus
- **Firewall:** Permetti a Ollama di comunicare attraverso il firewall

## 🌐 Interfaccia Web

Ollama include un'interfaccia web integrata. Dopo aver avviato Ollama, apri il browser e vai su:
```
http://localhost:11434
```

## 📚 Risorse Utili

- [Documentazione ufficiale](https://github.com/ollama/ollama/tree/main/docs)
- [Modelli disponibili](https://ollama.ai/library)
- [GitHub repository](https://github.com/ollama/ollama)
- [Community Discord](https://discord.gg/ollama)

## 🔄 Aggiornamenti

Per aggiornare Ollama:

```bash
# Linux/macOS
curl -fsSL https://ollama.ai/install.sh | sh

# Windows
# Scarica e installa la nuova versione dal sito ufficiale
```

## 📝 Note

- Ollama funziona offline una volta scaricati i modelli
- I modelli vengono scaricati automaticamente la prima volta che li usi
- La dimensione dei modelli varia da 1GB a oltre 40GB
- Assicurati di avere una connessione internet stabile per il download iniziale

---

**Hai bisogno di aiuto?** Apri una issue su GitHub o unisciti alla community Discord! 