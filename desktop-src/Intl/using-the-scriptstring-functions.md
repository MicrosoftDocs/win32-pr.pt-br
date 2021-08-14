---
description: Para um aplicativo lidando com texto não formatado, o Uniscribe fornece as funções de ScriptString \* .
ms.assetid: bfbba5df-ce06-4012-a7b1-55d8ea580942
title: Usando as funções ScriptString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6685af7dad2c9e1b8d0cf460d526155f967a9105e1b107047afb99c18a5124f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389402"
---
# <a name="using-the-scriptstring-functions"></a>Usando as funções ScriptString

Para um aplicativo lidando com texto não formatado, o Uniscribe fornece as funções **ScriptString \** _. Essas funções são semelhantes a [_ *ExtTextOut* *](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)e [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent), mas fornecem suporte completo a scripts complexos, incluindo o posicionamento do cursor. Essas funções são semelhantes às outras funções do Uniscribe, mas são adaptadas aos requisitos mais simples de processamento de texto sem formatação.

A tabela a seguir detalha as funções **ScriptString \*** e quaisquer contrapartes nas outras funções de Uniscribe.



<table>
<thead>
<tr class="header">
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></td>
<td>Analisa o texto sem formatação. Essa função corresponde às seguintes funções:<br/> <dl><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></td>
<td>Recupera a coordenada x para uma posição de caractere. Essa função corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></td>
<td>Libera uma estrutura de <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></td>
<td>Converte larguras visuais em larguras lógicas. Essa função corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></td>
<td>Mapas posições de glifo de caractere de forma semelhante a <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, somente para uso herdado. Essa função não funciona bem com scripts que geram mais de um glifo por ponto de código.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></td>
<td>Exibe texto sem formatação. Essa função corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></td>
<td>Retorna um ponteiro para o comprimento de uma cadeia de caracteres de texto sem formatação recortada.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></td>
<td>Retorna um ponteiro para o buffer de atributos lógicos para uma cadeia de caracteres de texto sem formatação analisada.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></td>
<td>Retorna um ponteiro para o tamanho (largura e altura) de uma cadeia de caracteres de texto sem formatação analisada.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></td>
<td>Identifica sequências de ponto de código não válidas no script especificado. Essa função é diferente de <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>, que identifica pontos de código que não estão presentes em uma fonte.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></td>
<td>Converte uma coordenada x em uma posição de caractere. Essa função corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>.</td>
</tr>
</tbody>
</table>

Para exibir apenas texto sem formatação sem modificações, um aplicativo deve chamar [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)e, em seguida, [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree). As outras funções são usadas para modificar o texto sem formatação antes da exibição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
