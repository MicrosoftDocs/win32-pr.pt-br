---
description: Esta seção descreve as funções de Windows de tratamento de caminho do Shell. Os elementos de programação explicados nesta documentação são exportados por Shlwapi.dll e definidos em Shlwapi.h e Shlwapi.lib.
title: Funções de manipulação de caminho do shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 90937e4aa3c93c14957ec0db7f081c1cb598989e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481962"
---
# <a name="shell-path-handling-functions"></a>Funções de manipulação de caminho do shell

Esta seção descreve as funções de Windows de tratamento de caminho do Shell. Os elementos de programação explicados nesta documentação são exportados por Shlwapi.dll e definidos em Shlwapi.h e Shlwapi.lib.

## <a name="in-this-section"></a>Nesta seção




| Tópico | Descrição | 
|-------|-------------|
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>Pathaddbackslash</strong></a><br /> | Adiciona uma faixa invertida ao final de uma cadeia de caracteres para criar a sintaxe correta para um caminho. Se o caminho de origem já tiver uma faixa invertida à frente, nenhuma faixa invertida será adicionada. <br /><blockquote>[!Note]<br />O uso indevido dessa função pode levar a um estouro de buffer. Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> mais segura em seu lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>Pathaddextension</strong></a><br /> | Adiciona uma extensão de nome de arquivo a uma cadeia de caracteres de caminho.<br /><blockquote>[!Note]<br />O uso indevido dessa função pode levar a um estouro de buffer. Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> mais segura em seu lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>Pathappend</strong></a><br /> | Anexa um caminho ao final de outro. <br /><blockquote>[!Note]<br />O uso indevido dessa função pode levar a um estouro de buffer. Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> mais segura em seu lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>Pathbuildroot</strong></a><br /> | Cria um caminho raiz de um determinado número de unidade.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>Pathcanonicalize</strong></a><br /> | Simplifica um caminho removendo elementos de navegação como "." e ".." para produzir um caminho direto e bem formado.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>Pathcombine</strong></a><br /> | Concatena duas cadeias de caracteres que representam caminhos formados corretamente em um caminho; também concatena quaisquer elementos de caminho relativo. <br /><blockquote>[!Note]<br />O uso indevido dessa função pode levar a um estouro de buffer. Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> mais segura em seu lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>Pathcommonprefix</strong></a><br /> | Compara dois caminhos para determinar se eles compartilham um prefixo comum. Um prefixo é um destes tipos: "C: \\ ", ".", "..", ".. \\ ".<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>Pathcompactpath</strong></a><br /> | Trunca um caminho de arquivo para se ajustar dentro de uma determinada largura de pixel substituindo componentes de caminho por reellipses.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>Pathcompactpathex</strong></a><br /> | Trunca um caminho para se ajustar a um determinado número de caracteres substituindo componentes de caminho por reellipses.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a><br /> | Converte uma URL de arquivo em um caminho MS-DOS da Microsoft.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a><br /> | Cria um caminho de uma URL de arquivo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>Pathfileexists</strong></a><br /> | Determina se um caminho para um objeto do sistema de arquivos, como um arquivo ou pasta, é válido.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>Pathfindextension</strong></a><br /> | Pesquisa um caminho para uma extensão.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>Pathfindfilename</strong></a><br /> | Pesquisa um caminho para um nome de arquivo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a><br /> | Analisado um caminho e retorna a parte desse caminho que segue a primeira faixa invertida.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a><br /> | Pesquisa um arquivo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a><br /> | Determina se um determinado nome de arquivo tem uma de uma lista de sufixos.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a><br /> | Localiza os argumentos de linha de comando dentro de um determinado caminho.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a><br /> | Determina o tipo de caractere em relação a um caminho.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>Pathgetdrivenumber</strong></a><br /> | Pesquisa um caminho para uma letra da unidade dentro do intervalo de 'A' a 'Z' e retorna o número da unidade correspondente.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a><br /> | Determina se o tipo de conteúdo registrado de um arquivo corresponde ao tipo de conteúdo especificado. Essa função obtém o tipo de conteúdo para o tipo de arquivo especificado e compara essa cadeia de caracteres com <em>o pszContentType</em>. A comparação não diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>Pathisdirectory</strong></a><br /> | Verifica se um caminho é um diretório válido.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a><br /> | Determina se um caminho especificado é um diretório vazio.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>Pathisfilespec</strong></a><br /> | Pesquisa um caminho para qualquer caractere delimitador de caminho (por exemplo, ':' ou ' \' ). Se não houver nenhum caractere delimitador de caminho presente, o caminho será considerado um caminho de Especificação de Arquivo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a><br /> | Determina se um arquivo é um arquivo HTML. A determinação é feita com base no tipo de conteúdo registrado para a extensão do arquivo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a><br /> | Determina se um nome de arquivo está em formato longo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a><br /> | Determina se uma cadeia de caracteres de caminho representa um recurso de rede.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>Pathisprefix</strong></a><br /> | Pesquisa um caminho para determinar se ele contém um prefixo válido do tipo passado por <em>pszPrefix.</em> Um prefixo é um destes tipos: "C: \\ ", ".", "..", ".. \\ ".<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a><br /> | Pesquisa um caminho e determina se ele é relativo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>Pathisroot</strong></a><br /> | Determina se uma cadeia de caracteres de caminho se refere à raiz de um volume.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>Pathissameroot</strong></a><br /> | Compara dois caminhos para determinar se eles têm um componente raiz comum.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a><br /> | Determina se uma pasta existente contém os atributos que a fazem uma pasta do sistema. Como alternativa, essa função indica se determinados atributos qualificam uma pasta para ser uma pasta do sistema.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>Pathisunc</strong></a><br /> | Determina se uma cadeia de caracteres de caminho é um caminho UNC válido, em vez de um caminho baseado em uma letra da unidade.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>Pathisuncserver</strong></a><br /> | Determina se uma cadeia de caracteres é um UNC válido apenas para um caminho de servidor.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>Pathisuncservershare</strong></a><br /> | Determina se uma cadeia de caracteres é um caminho de compartilhamento UNC válido, \\ <em>compartilhamento de</em> \<em> servidor </em> .<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a><br /> | Testa uma determinada cadeia de caracteres para determinar se ela está em conformidade com um formato de URL válido.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>Pathmakepretty</strong></a><br /> | Converte um caminho em letras maiúsculas em todos os caracteres minúsculos para dar ao caminho uma aparência consistente.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a><br /> | Dá a uma pasta existente os atributos adequados para se tornarem uma pasta do sistema.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a><br /> | Pesquisa uma cadeia de caracteres usando um tipo de correspondência curinga do MS-DOS.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a><br /> | Corresponde a um nome de arquivo de um caminho em relação a um ou mais padrões de nome de arquivo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a><br /> | Analisa uma cadeia de caracteres de local de arquivo que contém um local de arquivo e um índice de ícone e retorna valores separados.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a><br /> | Pesquisa um caminho em busca de espaços. Se forem encontrados espaços, o caminho inteiro será colocado entre aspas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a><br /> | Cria um caminho relativo de um arquivo ou pasta para outro.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a><br /> | Remove todos os argumentos de um determinado caminho.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a><br /> | Remove a barra invertida à direita de um determinado caminho.<br /><blockquote>[!Note]<br />Esta função é preterida. Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> em seu lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a><br /> | Remove todos os espaços à esquerda e à direita de uma cadeia de caracteres.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a><br /> | Remove a extensão de nome de arquivo de um caminho, se houver uma. <br /><blockquote>[!Note]<br />Esta função é preterida. Recomendamos o uso do <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> em seu lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a><br /> | Remove o nome de arquivo à direita e a barra invertida de um caminho, se estiverem presentes.<br /><blockquote>[!Note]<br />Esta função é preterida. Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> em seu lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a><br /> | Substitui a extensão de um nome de arquivo por uma nova extensão. Se o nome do arquivo não contiver uma extensão, a extensão será anexada ao final da cadeia de caracteres.<br /><blockquote>[!Note]<br />O uso indevido dessa função pode levar a uma saturação do buffer. Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> mais segura em seu lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a><br /> | Determina se um determinado caminho está formatado corretamente e totalmente qualificado.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a><br /> | Define o texto de um controle filho em uma janela ou caixa de diálogo, usando <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> para garantir que o caminho caiba no controle.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a><br /> | Recupera um ponteiro para o primeiro caractere em um caminho após a letra da unidade ou o servidor UNC/elementos do caminho de compartilhamento.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a><br /> | Remove a parte do caminho de um caminho e arquivo totalmente qualificado.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a><br /> | Remove todos os elementos de arquivo e diretório em um caminho, exceto as informações de raiz.<br /><blockquote>[!Note]<br />O uso indevido dessa função pode levar a uma saturação do buffer. Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> mais segura em seu lugar.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a><br /> | Remove a decoração de uma cadeia de caracteres de caminho.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a><br /> | Substitui determinados nomes de pasta em um caminho totalmente qualificado com sua cadeia de caracteres de ambiente associada.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a><br /> | Remove os atributos de uma pasta que o tornam uma pasta do sistema. Essa pasta deve realmente existir no sistema de arquivos.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a><br /> | Remove as aspas do início e do fim de um caminho.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a><br /> | Verifica um contexto de associação para ver se é seguro associar a um objeto de componente específico.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a><br /> | Determina um esquema para uma cadeia de caracteres de URL especificada e retorna uma cadeia de caracteres com um prefixo apropriado.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a><br /> | Converte uma cadeia de caracteres de URL em forma canônica.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a><br /> | Quando fornecido com uma URL relativa e sua base, o retorna uma URL na forma canônica.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a><br /> | Faz uma comparação que diferencia maiúsculas de minúsculas de duas cadeias de caracteres de URL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a><br /> | Converte um caminho do MS-DOS em uma URL canônica.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a><br /> | Converte caracteres ou pares substitutos em uma URL que pode ser alterada durante o transporte pela Internet (caracteres "não seguros") em suas sequências de escape correspondentes. Os pares substitutos são caracteres entre U + 10000 a U + 10FFFF (em UTF-32) ou entre DC00 e DFFF (em UTF-16). <br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a><br /> | Uma macro que converte caracteres de espaço em sua sequência de escape correspondente.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a><br /> | Recupera o local de uma URL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a><br /> | Aceita uma cadeia de caracteres de URL e retorna uma parte especificada dessa URL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a><br /> | Aplica hash a uma cadeia de caracteres de URL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a><br /> | Testa se uma URL é um tipo especificado.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a><br /> | Testa uma URL para determinar se é uma URL de arquivo.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a><br /> | Retorna se uma URL é uma URL que os navegadores normalmente não incluem no histórico de navegação.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a><br /> | Retorna se uma URL é opaca.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a><br /> | Converte as sequências de escape de volta em caracteres comuns.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a><br /> | Converte as sequências de escape de volta em caracteres comuns e substitui a cadeia de caracteres original.<br /> | 




 

 

 




