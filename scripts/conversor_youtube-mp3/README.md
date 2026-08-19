## YouTube para MP3

Script em Bash que baixa o áudio de um vídeo do YouTube e o converte para MP3.

### Requisitos

* Bash
* yt-dlp nightly
* Deno
* FFmpeg
* Internet

### Instalar FFmpeg e curl

```bash
sudo apt update
sudo apt install ffmpeg curl
```

### Instalar yt-dlp nightly

```bash
mkdir -p "$HOME/.local/bin"

curl -L "https://github.com/yt-dlp/yt-dlp-nightly-builds/releases/latest/download/yt-dlp" \
-o "$HOME/.local/bin/yt-dlp"

chmod +x "$HOME/.local/bin/yt-dlp"
export PATH="$HOME/.local/bin:$PATH"
```

### Instalar Deno

```bash
curl -fsSL https://deno.land/install.sh | sh
exec zsh
```

### Dar permissão ao script

```bash
chmod +x youtube-para-mp3.sh
```

### Como usar

```bash
./youtube-para-mp3.sh "URL_DO_VIDEO"
```

Exemplo:

```bash
./youtube-para-mp3.sh "https://www.youtube.com/watch?v=ID_DO_VIDEO"
```

Os arquivos serão salvos na pasta:

```text
musicas/
```

> Use somente em vídeos próprios, autorizados ou cuja licença permita o download.
