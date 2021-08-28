---
description: esta seção descreve as funções de manipulação de cadeia de caracteres do Windows Shell. Os elementos de programação explicados nesta documentação são exportados por Shlwapi.dll e definidos em Shlwapi. h e shlwapi. lib.
title: Funções de manipulação de cadeia de caracteres do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d11ad956b6eab11212243232dfaf8ef341d05544
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473312"
---
# <a name="shell-string-handling-functions"></a>Funções de manipulação de cadeia de caracteres do Shell

esta seção descreve as funções de manipulação de cadeia de caracteres do Windows Shell. Os elementos de programação explicados nesta documentação são exportados por Shlwapi.dll e definidos em Shlwapi. h e shlwapi. lib.

## <a name="in-this-section"></a>Nesta seção




| Tópico | Descrição | 
|-------|-------------|
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a><br /> | Executa uma comparação entre dois caracteres. A comparação não diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a><br /> | Recupera uma cadeia de caracteres usada com sites ao especificar preferências de idioma.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a><br /> | Executa uma comparação que diferencia maiúsculas de minúsculas de um número especificado de caracteres a partir do início de duas cadeias localizadas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a><br /> | Executa uma comparação que não diferencia maiúsculas de minúsculas de um número especificado de caracteres a partir do início de duas cadeias localizadas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a><br /> | Compara um número especificado de caracteres a partir do início de duas cadeias localizadas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a><br /> | Determina se um caractere representa um espaço.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a><br /> | Extrai um recurso de texto especificado quando esse recurso é fornecido na forma de uma cadeia de caracteres indireta (uma cadeia de caracteres que começa com o símbolo ' @ ').<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a><br /> | Faz uma cópia de uma cadeia de caracteres na memória alocada recentemente.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a><br /> | Acrescenta uma cadeia de caracteres a outra. <br /><blockquote>[!Note]<br />Não use. Consulte comentários para funções alternativas.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a><br /> | Copia e anexa caracteres de uma cadeia de caracteres ao final de outra. <br /><blockquote>[!Note]<br />Não use. Consulte comentários para funções alternativas.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a><br /> | Concatena duas cadeias de caracteres Unicode. Usado quando são necessárias concatenações repetidas para o mesmo buffer.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a><br /> | Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere que corresponde ao caractere especificado. A comparação diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a><br /> | Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere que corresponde ao caractere especificado. A comparação não diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a><br /> | Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere especificado. A comparação não diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a><br /> | Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere especificado. A comparação diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a><br /> | Compara duas cadeias de caracteres para determinar se elas são iguais. A comparação diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a><br /> | Compara Cadeias de caracteres usando regras de agrupamento de tempo de execução C (ASCII). A comparação diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a><br /> | Compara duas cadeias de caracteres para determinar se elas são iguais. A comparação não diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a><br /> | Compara duas cadeias de caracteres usando regras de agrupamento de tempo de execução C (ASCII). A comparação não diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a><br /> | Compara duas cadeias de caracteres Unicode. Os dígitos nas cadeias de caracteres são considerados como conteúdo numérico em vez de texto. Esse teste não diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a><br /> | Compara um número especificado de caracteres desde o início de duas cadeias para determinar se elas são iguais. A comparação diferencia maiúsculas de minúsculas. A macro <strong>StrNCmp</strong> difere dessa função somente em nome.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a><br /> | Compara um número especificado de caracteres desde o início de duas cadeias usando regras de agrupamento em tempo de execução C (ASCII). A comparação diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a><br /> | Compara um número especificado de caracteres desde o início de duas cadeias para determinar se elas são iguais. A comparação não diferencia maiúsculas de minúsculas. A macro <strong>StrNCmpI</strong> difere dessa função somente em nome.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a><br /> | Compara um número especificado de caracteres desde o início de duas cadeias usando regras de agrupamento em tempo de execução C (ASCII). A comparação não diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a><br /> | Copia uma cadeia de caracteres para outra. <br /><blockquote>[!Note]<br />Não use. Consulte comentários para funções alternativas.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpy</strong></a><br /> | Copia um número especificado de caracteres do início de uma cadeia de caracteres para outra.<br /><blockquote>[!Note]<br />Não use essa função ou a macro <strong>StrNCpy</strong> . Consulte comentários para funções alternativas.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a><br /> | Pesquisa uma cadeia de caracteres para a primeira ocorrência de qualquer um dos grupos de caracteres. O método de pesquisa diferencia maiúsculas de minúsculas e o caractere <strong>nulo</strong> de terminação é incluído na correspondência do padrão de pesquisa.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a><br /> | Pesquisa uma cadeia de caracteres para a primeira ocorrência de qualquer um dos grupos de caracteres. O método Search não diferencia maiúsculas de minúsculas e o caractere <strong>nulo</strong> de terminação é incluído na correspondência do padrão de pesquisa.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a><br /> | Duplica uma cadeia de caracteres.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a><br /> | Converte um valor numérico em uma cadeia de caracteres que representa o número expresso como um valor de tamanho em bytes, kilobytes, megabytes ou gigabytes, dependendo do tamanho.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a><br /> | Converte um valor numérico em uma cadeia de caracteres que representa o número expresso como um valor de tamanho em bytes, kilobytes, megabytes ou gigabytes, dependendo do tamanho. Difere de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> em um tipo de parâmetro.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a><br /> | Converte um valor numérico em uma cadeia de caracteres que representa o número em bytes, kilobytes, megabytes ou gigabytes, dependendo do tamanho. Estende <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> oferecendo a opção de arredondar para o dígito exibido mais próximo ou para descartar dígitos não exibidos.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a><br /> | Converte um valor numérico em uma cadeia de caracteres que representa o número expresso como um valor de tamanho em bytes, kilobytes, megabytes ou gigabytes, dependendo do tamanho. Difere de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> em um tipo de parâmetro.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a><br /> | Converte um valor numérico em uma cadeia de caracteres que representa o número expresso como um valor de tamanho em quilobytes.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a><br /> | Converte um intervalo de tempo, especificado em milissegundos, em uma cadeia de caracteres.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a><br /> | Compara um número especificado de caracteres desde o início de duas cadeias para determinar se elas são iguais.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a><br /> | Anexa um número especificado de caracteres desde o início de uma cadeia de caracteres até o fim de outro. <br /><blockquote>[!Note]<br />Não use essa função ou a macro <strong>StrCatN</strong> . Consulte comentários para funções alternativas.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a><br /> | Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere contido em um buffer especificado. Essa pesquisa não inclui o caractere nulo de terminação.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a><br /> | Pesquisa uma cadeia de caracteres para a última ocorrência de um caractere especificado. A comparação diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a><br /> | Pesquisa uma cadeia de caracteres para a última ocorrência de um caractere especificado. A comparação não diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a><br /> | Aceita uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> retornada por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> que contém ou aponta para uma cadeia de caracteres e retorna essa cadeia de caracteres como um <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a><br /> | Converte uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> retornada por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> em uma cadeia de caracteres e coloca o resultado em um buffer.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a><br /> | Usa uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> retornada por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> e retorna um ponteiro para uma cadeia de caracteres alocada que contém o nome de exibição.<br /> | 
| <a href="strrettostrn.md"><strong>StrRetToStrN</strong></a><br /> | Usa uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> retornada por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a>, converte-a em uma cadeia de caracteres e coloca o resultado em um buffer.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a><br /> | Pesquisa a última ocorrência de uma subcadeia de caracteres especificada em uma cadeia de caracteres. A comparação não diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a><br /> | Obtém o comprimento de uma subcadeia de caracteres dentro de uma cadeia de caracteres que consiste inteiramente em caracteres contidos em um buffer especificado.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a><br /> | Localiza a primeira ocorrência de uma subcadeia de caracteres dentro de uma cadeia de caracteres. A comparação diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a><br /> | Localiza a primeira ocorrência de uma subcadeia de caracteres dentro de uma cadeia de caracteres. A comparação não diferencia maiúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a><br /> | Converte uma cadeia de caracteres que representa um valor decimal em um inteiro. A macro <strong>StrToLong</strong> é idêntica a essa função.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a><br /> | Converte uma cadeia de caracteres que representa um valor decimal ou hexadecimal em um inteiro de 64 bits.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a><br /> | Converte uma cadeia de caracteres que representa um número decimal ou hexadecimal em um número inteiro.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>Prertrim</strong></a><br /> | Remove os caracteres especificados à esquerda e à direita de uma cadeia de caracteres.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a><br /> | Usa uma lista de argumentos de comprimento variável e retorna os valores dos argumentos como uma cadeia de caracteres formatada no estilo <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>. <br /><blockquote>[!Note]<br />Não use essa função. Consulte comentários para funções alternativas.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a><br /> | Usa uma lista de argumentos e retorna os valores dos argumentos como uma cadeia de caracteres formatada no estilo <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>. <br /><blockquote>[!Note]<br />Não use essa função. Consulte comentários para funções alternativas.</blockquote><br /> | 




 

 

 
