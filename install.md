# Uso direto
### A partir do arquivo .zip

Faça download do arquivo zipado `capt2-5.zip`. Extraia seu conteúdo para uma pasta apropriada no seu computador. Altere as permissões de execução para o executável. Feito isso, o aplicativo já pode ser usado.

# Dependências
### ambiente Ubuntu 24.04

No caso do Capt, as dependências não são instaladas automaticamente, porque o programa não é um pacote, nem está incluído nos repositórios oficiais de nenhuma distribuição linux. Então o usuário precisa instalar essas dependências *manualmente* antes de começar a usar o aplicativo.

É bem possível que todas essas bibliotecas já estejam instaladas na sua distribuição. Porém, se o Capt não rodar na primeira tentativa, pode ser pela falta de alguma delas.

### Para instalar bibliotecas necessárias

`sudo apt update`

`sudo apt install libqt5widgets5t64 libqt5gui5t64 libqt5core5t64 libstdc++6 libgcc-s1 libc6 libc6 libgl1 libpng16-16t64 zlib1g libharfbuzz0b libmd4c0 libdouble-conversion3 libicu74 libicu74 libpcre2-16-0 libzstd1 libglib2.0-0t64 libglvnd0 libglx0 libfreetype6 libgraphite2-3 libicu74 libpcre2-8-0 libx11-6 libbz2-1.0 libbrotli1 libxcb1 libbrotli1 libxau6 libxdmcp6 libbsd0 libmd0`
