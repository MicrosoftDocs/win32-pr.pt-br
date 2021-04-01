---
title: Cadeias de caracteres
description: Esta seção discute as funções de cadeia de caracteres.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- recursos, cadeias de caracteres
- cadeias de caracteres
- funções de cadeia de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3231006de2dfe6ed611b58e5b511819a40c21e8b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103642299"
---
# <a name="strings"></a>Cadeias de caracteres

Esta seção descreve as funções de cadeia de caracteres e explica como usá-las em seus aplicativos.

### <a name="in-this-section"></a>Nesta seção



| Nome                                     | Descrição                                             |
|------------------------------------------|---------------------------------------------------------|
| [Sobre cadeias de caracteres](about-strings.md)       | Discute as funções de cadeia de caracteres.<br/>              |
| [Sobre o strsafe. h](strsafe-ovw.md)       | Discute as funções de cadeia de caracteres no strsafe. h.<br/> |
| [Referência de cadeia de caracteres](string-reference.md) | Contém a referência de API.<br/>                  |



 

### <a name="string-functions"></a>Funções de Cadeia de Caracteres



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></td>
<td>Converte uma cadeia de caracteres ou um único caractere em minúsculas. Se o operando for uma cadeia de caracteres, a função converterá os caracteres em vigor. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></td>
<td>Converte caracteres maiúsculos em um buffer para caracteres minúsculos. A função converte os caracteres em vigor. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></td>
<td>Recupera um ponteiro para o próximo caractere em uma cadeia de caracteres. Essa função pode lidar com cadeias de caracteres que consistem em caractere de um ou vários bytes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></td>
<td>Recupera o ponteiro para o próximo caractere em uma cadeia de caracteres. Essa função pode lidar com cadeias de caracteres que consistem em caractere de um ou vários bytes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></td>
<td>Recupera um ponteiro para o caractere anterior em uma cadeia de caracteres. Essa função pode lidar com cadeias de caracteres que consistem em caractere de um ou vários bytes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></td>
<td>Recupera o ponteiro para o caractere anterior em uma cadeia de caracteres. Essa função pode lidar com cadeias de caracteres que consistem em caractere de um ou vários bytes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></td>
<td>Traduz uma cadeia de caracteres no conjunto de caracteres definido pelo OEM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></td>
<td>Converte um número especificado de caracteres em uma cadeia de caracteres no conjunto de caracteres definido pelo OEM.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></td>
<td>Converte uma cadeia de caracteres ou um único caractere em maiúsculas. Se o operando for uma cadeia de caracteres, a função converterá os caracteres em vigor. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></td>
<td>Converte caracteres minúsculos em um buffer em caracteres maiúsculos. A função converte os caracteres em vigor. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></td>
<td>Compara duas cadeias de caracteres, usando a localidade especificada.
<blockquote>
[!Note]<br />
Para compatibilidade com Unicode, use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> ou a versão Unicode de <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></td>
<td>Compara duas cadeias de caracteres Unicode (caractere largo), usando a localidade especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></td>
<td>Mapeia uma cadeia de caracteres para outra, executando uma opção de transformação especificada. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></td>
<td>Recupera informações de tipo de caractere para os caracteres na cadeia de caracteres de origem especificada. Para cada caractere na cadeia de caracteres, a função define um ou mais bits no elemento de 16 bits correspondente da matriz de saída. Cada bit identifica um determinado tipo de caractere, como se o caractere é uma letra, um dígito ou nenhum deles.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></td>
<td>Recupera informações de tipo de caractere para os caracteres na cadeia de caracteres de origem especificada. Para cada caractere na cadeia de caracteres, a função define um ou mais bits no elemento de 16 bits correspondente da matriz de saída. Cada bit identifica um determinado tipo de caractere, como se o caractere é uma letra, um dígito ou nenhum deles. <br/> Ao contrário de seus parentes <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> e <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, o <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> exibe o comportamento padrão por meio do uso da opção <strong> # definir Unicode</strong> . É a função recomendada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></td>
<td>Recupera informações de tipo de caractere para os caracteres na cadeia de caracteres de origem especificada. Para cada caractere na cadeia de caracteres, a função define um ou mais bits no elemento de 16 bits correspondente da matriz de saída. Cada bit identifica um determinado tipo de caractere, como se o caractere é uma letra, um dígito ou nenhum deles.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></td>
<td>Determina se um caractere é um caractere alfabético. Essa determinação se baseia na semântica do idioma selecionado pelo usuário durante a instalação ou por meio do painel de controle. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></td>
<td>Determina se um caractere é um caractere alfabético ou numérico. Essa determinação se baseia na semântica do idioma selecionado pelo usuário durante a instalação ou por meio do painel de controle. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></td>
<td>Determina se um caractere é minúsculo. Essa determinação se baseia na semântica do idioma selecionado pelo usuário durante a instalação ou por meio do painel de controle. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></td>
<td>Determina se um caractere é maiúsculo. Essa determinação se baseia na semântica do idioma selecionado pelo usuário durante a instalação ou por meio do painel de controle. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>Cadeia de caracteres LoadString</strong></a></td>
<td>Carrega um recurso de cadeia de caracteres do arquivo executável associado a um módulo especificado, copia a cadeia de caracteres em um buffer e anexa um caractere nulo de terminação.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></td>
<td>Acrescenta uma cadeia de caracteres a outra.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a></td>
<td>Compara duas cadeias de caracteres. A comparação diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a></td>
<td>Compara duas cadeias de caracteres. A comparação não diferencia maiúsculas de minúsculas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></td>
<td>Copia uma cadeia de caracteres em um buffer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></td>
<td>Copia um número especificado de caracteres de uma cadeia de caracteres de origem em um buffer. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></td>
<td>Determina o comprimento da cadeia de caracteres especificada (não incluindo o caractere nulo de terminação).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></td>
<td>Traduz uma cadeia de caracteres do conjunto de caracteres definido pelo OEM em uma cadeia de caracteres ANSI ou de caractere largo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></td>
<td>Converte um número especificado de caracteres em uma cadeia de caractere do conjunto de caracteres definido pelo OEM em uma cadeia de caracteres ANSI ou de caractere largo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></td>
<td>Grava dados formatados no buffer especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></td>
<td>Grava dados formatados no buffer especificado usando um ponteiro para uma lista de argumentos.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="strsafe-functions"></a>Funções strsafe



| Nome                                             | Descrição                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | Concatena uma cadeia de caracteres a outra cadeia de caracteres.<br/>                                            |
| [**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | Concatena uma cadeia de caracteres a outra cadeia de caracteres.<br/>                                            |
| [**StringCbCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | Concatena o número especificado de bytes de uma cadeia de caracteres para outra cadeia de caracteres.<br/>         |
| [**StringCbCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | Concatena o número especificado de bytes de uma cadeia de caracteres para outra cadeia de caracteres.<br/>         |
| [**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | Copia uma cadeia de caracteres para outra.<br/>                                                         |
| [**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | Copia uma cadeia de caracteres para outra.<br/>                                                         |
| [**StringCbCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | Copia o número especificado de bytes de uma cadeia de caracteres para outra.<br/>                      |
| [**StringCbCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | Copia o número especificado de bytes de uma cadeia de caracteres para outra.<br/>                      |
| [**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | Obtém uma linha de texto de stdin, até e incluindo o caractere de nova linha (' \\ n').<br/>  |
| [**StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | Obtém uma linha de texto de stdin, até e incluindo o caractere de nova linha (' \\ n').<br/>  |
| [**StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | Determina se uma cadeia de caracteres excede o comprimento especificado, em bytes.<br/>                   |
| [**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | Grava dados formatados na cadeia de caracteres especificada.<br/>                                        |
| [**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | Grava dados formatados na cadeia de caracteres especificada.<br/>                                        |
| [**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | Grava dados formatados na cadeia de caracteres especificada usando um ponteiro para uma lista de argumentos.<br/> |
| [**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | Grava dados formatados na cadeia de caracteres especificada usando um ponteiro para uma lista de argumentos.<br/> |
| [**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | Concatena uma cadeia de caracteres a outra cadeia de caracteres.<br/>                                            |
| [**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | Concatena uma cadeia de caracteres a outra cadeia de caracteres.<br/>                                            |
| [**StringCchCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | Concatena o número especificado de caracteres de uma cadeia de caracteres para outra.<br/>    |
| [**StringCchCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | Concatena o número especificado de caracteres de uma cadeia de caracteres para outra.<br/>    |
| [**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | Copia uma cadeia de caracteres para outra.<br/>                                                         |
| [**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | Copia uma cadeia de caracteres para outra.<br/>                                                         |
| [**StringCchCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | Copia o número especificado de caracteres de uma cadeia para outra.<br/>                 |
| [**StringCchCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | Copia o número especificado de caracteres de uma cadeia para outra.<br/>                 |
| [**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | Obtém uma linha de texto de stdin, até e incluindo o caractere de nova linha (' \\ n').<br/>  |
| [**StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | Obtém uma linha de texto de stdin, até e incluindo o caractere de nova linha (' \\ n').<br/>  |
| [**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | Determina se uma cadeia de caracteres excede o comprimento especificado, em caracteres.<br/>              |
| [**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | Grava dados formatados na cadeia de caracteres especificada.<br/>                                        |
| [**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | Grava dados formatados na cadeia de caracteres especificada.<br/>                                        |
| [**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | Grava dados formatados na cadeia de caracteres especificada usando um ponteiro para uma lista de argumentos.<br/> |
| [**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | Grava dados formatados na cadeia de caracteres especificada usando um ponteiro para uma lista de argumentos.<br/> |



 

 

