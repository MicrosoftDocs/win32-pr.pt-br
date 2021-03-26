---
description: Esta seção descreve as funções de manipulação de cadeia de caracteres do shell do Windows. Os elementos de programação explicados nesta documentação são exportados por Shlwapi.dll e definidos em Shlwapi. h e shlwapi. lib.
title: Funções de manipulação de cadeia de caracteres do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c2e47785db10ba7dc4bbe54e78e3a06be1b152a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922565"
---
# <a name="shell-string-handling-functions"></a>Funções de manipulação de cadeia de caracteres do Shell

Esta seção descreve as funções de manipulação de cadeia de caracteres do shell do Windows. Os elementos de programação explicados nesta documentação são exportados por Shlwapi.dll e definidos em Shlwapi. h e shlwapi. lib.

## <a name="in-this-section"></a>Nesta seção



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a><br/></td>
<td>Executa uma comparação entre dois caracteres. A comparação não diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a><br/></td>
<td>Recupera uma cadeia de caracteres usada com sites ao especificar preferências de idioma.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a><br/></td>
<td>Executa uma comparação que diferencia maiúsculas de minúsculas de um número especificado de caracteres a partir do início de duas cadeias localizadas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a><br/></td>
<td>Executa uma comparação que não diferencia maiúsculas de minúsculas de um número especificado de caracteres a partir do início de duas cadeias localizadas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a><br/></td>
<td>Compara um número especificado de caracteres a partir do início de duas cadeias localizadas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a><br/></td>
<td>Determina se um caractere representa um espaço.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a><br/></td>
<td>Extrai um recurso de texto especificado quando esse recurso é fornecido na forma de uma cadeia de caracteres indireta (uma cadeia de caracteres que começa com o símbolo ' @ ').<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a><br/></td>
<td>Faz uma cópia de uma cadeia de caracteres na memória alocada recentemente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a><br/></td>
<td>Acrescenta uma cadeia de caracteres a outra. <br/>
<blockquote>
[!Note]<br />
Não use. Consulte comentários para funções alternativas.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a><br/></td>
<td>Copia e anexa caracteres de uma cadeia de caracteres ao final de outra. <br/>
<blockquote>
[!Note]<br />
Não use. Consulte comentários para funções alternativas.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a><br/></td>
<td>Concatena duas cadeias de caracteres Unicode. Usado quando são necessárias concatenações repetidas para o mesmo buffer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a><br/></td>
<td>Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere que corresponde ao caractere especificado. A comparação diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a><br/></td>
<td>Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere que corresponde ao caractere especificado. A comparação não diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a><br/></td>
<td>Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere especificado. A comparação não diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a><br/></td>
<td>Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere especificado. A comparação diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a><br/></td>
<td>Compara duas cadeias de caracteres para determinar se elas são iguais. A comparação diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a><br/></td>
<td>Compara Cadeias de caracteres usando regras de agrupamento de tempo de execução C (ASCII). A comparação diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a><br/></td>
<td>Compara duas cadeias de caracteres para determinar se elas são iguais. A comparação não diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a><br/></td>
<td>Compara duas cadeias de caracteres usando regras de agrupamento de tempo de execução C (ASCII). A comparação não diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a><br/></td>
<td>Compara duas cadeias de caracteres Unicode. Os dígitos nas cadeias de caracteres são considerados como conteúdo numérico em vez de texto. Esse teste não diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a><br/></td>
<td>Compara um número especificado de caracteres desde o início de duas cadeias para determinar se elas são iguais. A comparação diferencia maiúsculas de minúsculas. A macro <strong>StrNCmp</strong> difere dessa função somente em nome.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a><br/></td>
<td>Compara um número especificado de caracteres desde o início de duas cadeias usando regras de agrupamento em tempo de execução C (ASCII). A comparação diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a><br/></td>
<td>Compara um número especificado de caracteres desde o início de duas cadeias para determinar se elas são iguais. A comparação não diferencia maiúsculas de minúsculas. A macro <strong>StrNCmpI</strong> difere dessa função somente em nome.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a><br/></td>
<td>Compara um número especificado de caracteres desde o início de duas cadeias usando regras de agrupamento em tempo de execução C (ASCII). A comparação não diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a><br/></td>
<td>Copia uma cadeia de caracteres para outra. <br/>
<blockquote>
[!Note]<br />
Não use. Consulte comentários para funções alternativas.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpy</strong></a><br/></td>
<td>Copia um número especificado de caracteres do início de uma cadeia de caracteres para outra.<br/>
<blockquote>
[!Note]<br />
Não use essa função ou a macro <strong>StrNCpy</strong> . Consulte comentários para funções alternativas.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a><br/></td>
<td>Pesquisa uma cadeia de caracteres para a primeira ocorrência de qualquer um dos grupos de caracteres. O método de pesquisa diferencia maiúsculas de minúsculas e o caractere <strong>nulo</strong> de terminação é incluído na correspondência do padrão de pesquisa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a><br/></td>
<td>Pesquisa uma cadeia de caracteres para a primeira ocorrência de qualquer um dos grupos de caracteres. O método Search não diferencia maiúsculas de minúsculas e o caractere <strong>nulo</strong> de terminação é incluído na correspondência do padrão de pesquisa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a><br/></td>
<td>Duplica uma cadeia de caracteres.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a><br/></td>
<td>Converte um valor numérico em uma cadeia de caracteres que representa o número expresso como um valor de tamanho em bytes, kilobytes, megabytes ou gigabytes, dependendo do tamanho.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a><br/></td>
<td>Converte um valor numérico em uma cadeia de caracteres que representa o número expresso como um valor de tamanho em bytes, kilobytes, megabytes ou gigabytes, dependendo do tamanho. Difere de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> em um tipo de parâmetro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a><br/></td>
<td>Converte um valor numérico em uma cadeia de caracteres que representa o número em bytes, kilobytes, megabytes ou gigabytes, dependendo do tamanho. Estende <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> oferecendo a opção de arredondar para o dígito exibido mais próximo ou para descartar dígitos não exibidos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a><br/></td>
<td>Converte um valor numérico em uma cadeia de caracteres que representa o número expresso como um valor de tamanho em bytes, kilobytes, megabytes ou gigabytes, dependendo do tamanho. Difere de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> em um tipo de parâmetro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a><br/></td>
<td>Converte um valor numérico em uma cadeia de caracteres que representa o número expresso como um valor de tamanho em quilobytes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a><br/></td>
<td>Converte um intervalo de tempo, especificado em milissegundos, em uma cadeia de caracteres.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a><br/></td>
<td>Compara um número especificado de caracteres desde o início de duas cadeias para determinar se elas são iguais.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a><br/></td>
<td>Anexa um número especificado de caracteres desde o início de uma cadeia de caracteres até o fim de outro. <br/>
<blockquote>
[!Note]<br />
Não use essa função ou a macro <strong>StrCatN</strong> . Consulte comentários para funções alternativas.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a><br/></td>
<td>Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere contido em um buffer especificado. Essa pesquisa não inclui o caractere nulo de terminação.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a><br/></td>
<td>Pesquisa uma cadeia de caracteres para a última ocorrência de um caractere especificado. A comparação diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a><br/></td>
<td>Pesquisa uma cadeia de caracteres para a última ocorrência de um caractere especificado. A comparação não diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a><br/></td>
<td>Aceita uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> retornada por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> que contém ou aponta para uma cadeia de caracteres e retorna essa cadeia de caracteres como um <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a><br/></td>
<td>Converte uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> retornada por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> em uma cadeia de caracteres e coloca o resultado em um buffer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a><br/></td>
<td>Usa uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> retornada por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> e retorna um ponteiro para uma cadeia de caracteres alocada que contém o nome de exibição.<br/></td>
</tr>
<tr class="even">
<td><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a><br/></td>
<td>Usa uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> retornada por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a>, converte-a em uma cadeia de caracteres e coloca o resultado em um buffer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a><br/></td>
<td>Pesquisa a última ocorrência de uma subcadeia de caracteres especificada em uma cadeia de caracteres. A comparação não diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a><br/></td>
<td>Obtém o comprimento de uma subcadeia de caracteres dentro de uma cadeia de caracteres que consiste inteiramente em caracteres contidos em um buffer especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a><br/></td>
<td>Localiza a primeira ocorrência de uma subcadeia de caracteres dentro de uma cadeia de caracteres. A comparação diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a><br/></td>
<td>Localiza a primeira ocorrência de uma subcadeia de caracteres dentro de uma cadeia de caracteres. A comparação não diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a><br/></td>
<td>Converte uma cadeia de caracteres que representa um valor decimal em um inteiro. A macro <strong>StrToLong</strong> é idêntica a essa função.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a><br/></td>
<td>Converte uma cadeia de caracteres que representa um valor decimal ou hexadecimal em um inteiro de 64 bits.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a><br/></td>
<td>Converte uma cadeia de caracteres que representa um número decimal ou hexadecimal em um número inteiro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>Prertrim</strong></a><br/></td>
<td>Remove os caracteres especificados à esquerda e à direita de uma cadeia de caracteres.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a><br/></td>
<td>Usa uma lista de argumentos de comprimento variável e retorna os valores dos argumentos como uma cadeia de caracteres formatada no estilo <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>. <br/>
<blockquote>
[!Note]<br />
Não use essa função. Consulte comentários para funções alternativas.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a><br/></td>
<td>Usa uma lista de argumentos e retorna os valores dos argumentos como uma cadeia de caracteres formatada no estilo <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>. <br/>
<blockquote>
[!Note]<br />
Não use essa função. Consulte comentários para funções alternativas.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
