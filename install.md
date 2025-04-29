# Uso direto
### A partir do arquivo .zip

Faça download do arquivo zipado `capt2-5.zip`. Extraia seu conteúdo para uma pasta apropriada no seu computador. Altere as permissões de execução para o executável. Feito isso, o aplicativo já pode ser usado.

# Dependências
### ambiente Ubuntu 24.04

No caso do Capt, as dependências não são instaladas automaticamente, porque o programa não é um pacote, nem está incluído nos repositórios oficiais de nenhuma distribuição linux. Então o usuário precisa instalar essas dependências *manualmente* antes de começar a usar o aplicativo.

É bem possível que todas essas bibliotecas já estejam instaladas na sua distribuição. Porém, se o Capt não rodar na primeira tentativa, pode ser pela falta de alguma delas.

# Comandos
### Para instalar bibliotecas necessárias

`sudo apt update`

`sudo apt install libqt5widgets5t64 libqt5gui5t64 libqt5core5t64 libstdc++6 libgcc-s1 libc6 libc6 libgl1 libpng16-16t64 zlib1g libharfbuzz0b libmd4c0 libdouble-conversion3 libicu74 libicu74 libpcre2-16-0 libzstd1 libglib2.0-0t64 libglvnd0 libglx0 libfreetype6 libgraphite2-3 libicu74 libpcre2-8-0 libx11-6 libbz2-1.0 libbrotli1 libxcb1 libbrotli1 libxau6 libxdmcp6 libbsd0 libmd0`

### Para instalar temas
`sudo apt update`

`sudo apt install kde-style-qtcurve-qt5 qt5-style-kvantum qt5-style-kvantum-l10n qt5-style-kvantum-themes qt5-style-plugin-plastique qt5-style-plugin-motif qt5-style-plugin-cleanlooks`

### Para o primeiro uso

No navegador, basta clicar com o botão direito do mouse, selecionar propriedades, abrir a aba permissões e marcar o item `executar como programa`. Então é possível clicar duas vezes ou clicar com o botão direito e selecionar `executar` no menu.

Ou no terminal, posicionar-se na pasta do aplicativo e executar o comando de permissões:
`cd /pasta/do/capt`
`sudo chmod +x capt`
`./capt`

De outras vezes, basta:
`cd /pasta/do/capt`
`./capt`
 
Observação: é importante manter a pasta `xpm` (a pasta dos ícones) na mesma pasta do executável; sem ela, os ícones não aparecem na interface.

# Integração
### Para integrar ao sistema

É possível integrar o Capt ao sistema. Para isto, basta copiar a pasta do aplicativo para a pasta de sistema `/opt` e criar um link simbólico para o executável na pasta de aplicativos de sistema `/usr/bin`. Algumas dessas operações exigem permissões de administrador.

Para isso, no terminal, use os comandos a seguir:
`cd /pasta/do/capt`
`sudo cp -r Capt2.5 /opt/Capt2.5`
`sudo ln -s /opt/Capt2.5/capt /usr/bin/capt`
`cd /opt/Capt2.5`
`capt`

Observe que, para abrir o programa a partir desta alteração, não é mais necessário usar o `./` antes do comando. Porém, chamar o programa de outra pasta que não a do aplicativo, pode causar dificuldade para o programa encontrar os ícones. Para evitar isso, o programa deve ser chamado sempre dentro da pasta onde também está a pasta `xpm` dos ícones:
`cd /opt/Capt2.5`
`capt`

### Para integrar ao menu do ambiente gráfico

Integrar o programa ao desktop (Ubuntu 24.04/Gnome) evita o perrengue de não abrir os ícones da interface. Para integrar ao desktop, crie um arquivo de texto puro com o nome `capt.desktop` com seguinte conteúdo:

```
[Desktop Entry]
Name=Capt 2.5
Comment=Coleta Assistida de Padrões de Texto
Exec=capt
Path=/opt/Capt2.5
Icon=/opt/Capt2.5/xpm/capt_mainwindow.png
Terminal=false
Type=Application
StartupNotify=true
Categories=KDE;Qt;Science;
Keywords=editor;notes;note-taking;
```

Salve o arquivo em `~/.local/share/applications/capt.desktop`, depois faça uma cópia dele com o seguinte comando:
`sudo cp ~/.local/share/applications/capt.desktop /usr/share/applications`

Pronto, agora é possível ver do que o **Capt 2.5** capaz!
