---
description: A biblioteca DbgHelp usa o caminho de pesquisa de símbolo para localizar símbolos de depuração (arquivos. PDB e. dbg). O caminho de pesquisa pode ser composto por um ou mais elementos de caminho separados por ponto e vírgula.
ms.assetid: 3527f589-285b-4cdf-b024-17920971a904
title: Caminhos de símbolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 977772e45c345e1e990dc038fccd852d17d279dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920275"
---
# <a name="symbol-paths"></a>Caminhos de símbolo

A biblioteca DbgHelp usa o caminho de pesquisa de símbolo para localizar símbolos de depuração (arquivos. PDB e. dbg). O caminho de pesquisa pode ser composto por um ou mais elementos de caminho separados por ponto e vírgula.

## <a name="specifying-search-paths"></a>Especificando caminhos de pesquisa

Para especificar onde o manipulador de símbolo pesquisará os diretórios de disco para arquivos de símbolo, chame a função [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) . Como alternativa, você pode especificar um caminho de pesquisa de símbolo no parâmetro *UserSearchPath* da função [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .

O parâmetro *UserSearchPath* em [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) e o parâmetro *SearchPath* em [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) usam um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um caminho ou uma série de caminhos separados por um ponto-e-vírgula. O manipulador de símbolo usa esses caminhos para pesquisar arquivos de símbolo. Se esse parâmetro for **nulo**, o manipulador de símbolo pesquisará o diretório que contém o módulo para o qual os símbolos estão sendo pesquisados. Caso contrário, se esse parâmetro for especificado como um valor não **nulo** , o manipulador de símbolo primeiro pesquisará os caminhos definidos pelo aplicativo antes de Pesquisar o diretório do módulo. Se você definir o \_ caminho do símbolo do NT \_ \_ ou a \_ \_ \_ \_ variável de ambiente do caminho do símbolo do NT Alt, o manipulador de símbolos pesquisará os arquivos de símbolo na seguinte ordem:

1. A \_ \_ variável de ambiente do caminho do símbolo NT \_ .
2. A \_ \_ variável de ambiente do caminho do símbolo Alt do NT \_ \_ .
3. O diretório que contém o módulo correspondente.

Para recuperar os caminhos de pesquisa, chame a função [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) .

O caminho de pesquisa para arquivos do banco de dados do programa (. pdb) é diferente do caminho para arquivos de depuração (. dbg). O algoritmo é determinado pela funcionalidade da biblioteca de símbolos. Por padrão, o Microsoft Visual C/C++ cria símbolos de formato da Microsoft, os retira da imagem e os coloca em um arquivo. pdb separado. Normalmente, o arquivo. pdb estará localizado no diretório que contém a imagem executável. O Visual C/C++ incorpora o caminho absoluto para o arquivo. pdb na imagem executável. Se o manipulador de símbolo não encontrar o arquivo. pdb nesse local ou se o arquivo. pdb foi movido para outro diretório, o manipulador de símbolo localizará o arquivo. pdb usando o caminho de pesquisa descrito para os arquivos. dbg.

## <a name="path-element-types"></a>Tipos de elemento Path

Há três tipos de elementos Path.

### <a name="standard-path-element"></a>Elemento de caminho padrão

Um elemento Path padrão é pesquisado procurando na raiz do diretório especificado pelo elemento Path. O manipulador de símbolo também procura em um subdiretório de "Symbols" que corresponde à extensão de arquivo do módulo que os símbolos estão sendo procurados. Normalmente, é "dll", "exe" ou "sys". Por fim, ele procura em um subdiretório chamado "Symbols" com um diretório com o mesmo nome da extensão. Por exemplo, se o elemento de caminho do símbolo for "c: \\ Mysymbols" e o arquivo para o qual os símbolos estão sendo pesquisados for "boo.dll", os seguintes diretórios serão pesquisados.

- c: \\ Mysymbols  
- c: \\ Mysymbols \\ dll  
- DLL de \\ símbolos c: Mysymbols \\ \\  

O manipulador de símbolo usa essa lógica para pesquisar qualquer elemento de caminho que não atenda aos critérios para ser um *servidor de símbolos* ou *cache* (descrito abaixo).

### <a name="symbol-server-path-element"></a>Elemento de caminho do servidor Symbol

Um elemento de caminho de *servidor de símbolos* usa uma tecnologia especial que pode localizar um símbolo que seja uma correspondência exata para o módulo em questão. Consulte [usando symsrv](using-symsrv.md) para obter mais detalhes.

O manipulador de símbolos trata um elemento Path como um servidor de símbolos se ele começa com o texto "SRV \* ".

> [!Note]  
> Se o texto "SRV \* " não for especificado, mas o elemento de caminho real for um armazenamento de servidor de símbolos, o manipulador de símbolo atuará como se "SRV \* " fosse especificado. O manipulador de símbolos faz essa determinação pesquisando a existência de um arquivo chamado "pingme.txt" no diretório raiz do caminho especificado.

 

### <a name="cache-path-element"></a>Elemento de caminho de cache

Um elemento de caminho de *cache* é uma variação em um elemento de caminho de servidor de símbolo.

Esse diretório é pesquisado como qualquer outro servidor de símbolos. No entanto, se o símbolo não for encontrado aqui e for encontrado em um elemento Path mais distante da cadeia do caminho do símbolo, o símbolo será copiado e armazenado no servidor de símbolos especificado neste elemento.

O manipulador de símbolo trata um elemento Path como um elemento de cache se ele começa com o texto "cache \* ". Para especificar um cache em "c: \\ myCache", use um elemento de caminho de símbolo de "cache \* c: \\ myCache".

## <a name="example-search-path"></a>Exemplo de caminho de pesquisa

Para ver como isso funciona, defina este caminho de pesquisa.

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

A seguir está uma lista da saída detalhada do manipulador de símbolos ao procurar o ntdll. pdb, usando o caminho de pesquisa listado acima.

```
DBGHELP: .\ntdll.pdb - file not found
DBGHELP: .\dll\ntdll.pdb - file not found
DBGHELP: .\symbols\dll\ntdll.pdb - file not found
SYMSRV: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb not found
SYMSRV: ntdll.pdb from \\symbols\symbols: 10497024 bytes - copied
DBGHELP: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb already cached
DBGHELP: ntdll - private symbols & lines
c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb
```

As três primeiras linhas da saída mostram o manipulador de símbolo que processa o primeiro elemento Path de `.` . Este é um elemento de caminho padrão.

A quarta linha mostra o manipulador de símbolo usando o servidor de símbolos para procurar o arquivo no segundo elemento Path, `cache*c:\myCache` que é um elemento de caminho de cache.

A quinta linha mostra que o arquivo está localizado no terceiro elemento Path de `srv*\\symbols\symbols` , que é um elemento Path do servidor Symbol.

A sexta linha mostra que o arquivo é copiado para o cache.

As duas últimas linhas em que o arquivo é aberto do cache.
