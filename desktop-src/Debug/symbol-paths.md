---
description: A biblioteca DbgHelp usa o caminho de pesquisa de símbolos para localizar símbolos de depuração (arquivos .pdb e .dbg). O caminho de pesquisa pode ser feito de um ou mais elementos de caminho separados por ponto e vírgula.
ms.assetid: 3527f589-285b-4cdf-b024-17920971a904
title: Caminhos de símbolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddf01dfbb5aedfcdd2d96cdfd5d4fdd10e6d3f71b5c69024917ddac534d3824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405896"
---
# <a name="symbol-paths"></a>Caminhos de símbolo

A biblioteca DbgHelp usa o caminho de pesquisa de símbolos para localizar símbolos de depuração (arquivos .pdb e .dbg). O caminho de pesquisa pode ser feito de um ou mais elementos de caminho separados por ponto e vírgula.

## <a name="specifying-search-paths"></a>Especificando caminhos de pesquisa

Para especificar onde o manipulador de símbolos pesquisa os diretórios de disco para arquivos de símbolo, chame a [**função SymSetSearchPath.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) Como alternativa, você pode especificar um caminho de pesquisa de símbolo no *parâmetro UserSearchPath* da [**função SymInitialize.**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)

O *parâmetro UserSearchPath* em [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) e o parâmetro *SearchPath* em [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) levam um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um caminho ou uma série de caminhos separados por ponto e vírgula. O manipulador de símbolos usa esses caminhos para pesquisar arquivos de símbolo. Se esse parâmetro for **NULL,** o manipulador de símbolos pesquisa o diretório que contém o módulo para o qual os símbolos estão sendo pesquisados. Caso contrário, se esse parâmetro for especificado como um valor não **NULL,** o manipulador de símbolos primeiro pesquisa os caminhos definidos pelo aplicativo antes de pesquisar o diretório do módulo. Se você definir a variável de ambiente CAMINHO DO SÍMBOLO NT ou CAMINHO DO SÍMBOLO \_ ALT NT, o manipulador de símbolos procurará arquivos \_ de símbolo na seguinte \_ \_ \_ \_ \_ ordem:

1. A \_ variável de ambiente PATH do SÍMBOLO NT. \_ \_
2. A \_ variável de ambiente PATH de SÍMBOLO ALT NT. \_ \_ \_
3. O diretório que contém o módulo correspondente.

Para recuperar os caminhos de pesquisa, chame a [**função SymGetSearchPath.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath)

O caminho de pesquisa para arquivos de banco de dados do programa (.pdb) é diferente do caminho para arquivos de depuração (.dbg). O algoritmo é determinado pela funcionalidade da biblioteca de símbolos. Por padrão, o Microsoft Visual C/C++ cria símbolos de formato da Microsoft, os retira da imagem e os coloca em um arquivo .pdb separado. Normalmente, o arquivo .pdb estará localizado no diretório que contém a imagem executável. O Visual C/C++ incorpora o caminho absoluto para o arquivo .pdb na imagem executável. Se o manipulador de símbolos não puder localizar o arquivo .pdb nesse local ou se o arquivo .pdb tiver sido movido para outro diretório, o manipulador de símbolos localizará o arquivo .pdb usando o caminho de pesquisa descrito para arquivos .dbg.

## <a name="path-element-types"></a>Tipos de elemento Path

Há três tipos de elementos de caminho.

### <a name="standard-path-element"></a>Elemento Path Standard

Um elemento de caminho padrão é pesquisado observando a raiz do diretório especificado pelo elemento path. O manipulador de símbolos também procura um subdiretório de "símbolos" que corresponde à extensão de arquivo do módulo que os símbolos estão sendo procurados. Normalmente, isso é "dll", "exe" ou "sys". Por fim, ele procura em um subdiretório chamado "símbolos" com um diretório com o mesmo nome que a extensão. Por exemplo, se o elemento de caminho do símbolo for "c: mySymbols" e o arquivo que os símbolos estão sendo pesquisados for "boo.dll", os diretórios a seguir serão \\ pesquisados.

- c: \\ mySymbols  
- c: \\ mySymbols \\ dll  
- c: \\ dll de \\ símbolos de mySymbols \\  

O manipulador de símbolos usa essa lógica para pesquisar qualquer elemento de caminho que não atender aos critérios para ser um servidor de símbolos *ou* *cache* (descrito abaixo).

### <a name="symbol-server-path-element"></a>Elemento Symbol Server Path

Um *elemento de caminho do* servidor de símbolos usa uma tecnologia especial que pode localizar um símbolo que é uma combinação exata para o módulo em questão. Consulte [Usando SymSrv](using-symsrv.md) para obter mais detalhes.

O manipulador de símbolos tratará um elemento path como um servidor de símbolos se ele começar com o texto " srv \* ".

> [!Note]  
> Se o texto "srv" não for especificado, mas o elemento de caminho real for um armazenamento de servidores de símbolos, o manipulador de símbolos atuará como se \* "srv" tivesse \* sido especificado. O manipulador de símbolos faz essa determinação pesquisando a existência de um arquivo chamado "pingme.txt" no diretório raiz do caminho especificado.

 

### <a name="cache-path-element"></a>Elemento Cache Path

Um *elemento de* caminho de cache é uma variação em um elemento de caminho do servidor de símbolos.

Esse diretório é pesquisado como qualquer outro servidor de símbolos. No entanto, se o símbolo não for encontrado aqui e for encontrado em um elemento de caminho mais adiante na cadeia do caminho do símbolo, o símbolo será copiado e armazenado no servidor de símbolos especificado neste elemento.

O manipulador de símbolos tratará um elemento path como um elemento de cache se ele começar com o texto " cache \* ". Para especificar um cache em "c: myCache", use um elemento de caminho de símbolo \\ de "cache \* c: \\ myCache".

## <a name="example-search-path"></a>Caminho de pesquisa de exemplo

Para ver como isso funciona, de definir esse caminho de pesquisa.

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

Veja a seguir uma listagem da saída detalhada do manipulador de símbolos ao pesquisar ntdll.pdb, usando o caminho de pesquisa listado acima.

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

As três primeiras linhas de saída mostram o manipulador de símbolos processando o primeiro elemento de caminho de `.` . Esse é um elemento de caminho padrão.

A quarta linha mostra o manipulador de símbolos usando o servidor de símbolos para procurar o arquivo no segundo elemento de caminho do qual `cache*c:\myCache` é um elemento de caminho de cache.

A quinta linha mostra que o arquivo é encontrado no terceiro elemento de caminho de `srv*\\symbols\symbols` , que é um elemento de caminho do servidor de símbolos.

A sexta linha mostra que o arquivo é copiado para o cache.

As duas últimas linhas que o arquivo é aberto do cache.
