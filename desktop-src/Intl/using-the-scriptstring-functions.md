---
description: Para um aplicativo lidando com texto não formatado, o Uniscribe fornece as funções de ScriptString \* .
ms.assetid: bfbba5df-ce06-4012-a7b1-55d8ea580942
title: Usando as funções ScriptString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a2df5e7515bd605ad48cc7a246941e9b6f08f2
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008558"
---
# <a name="using-the-scriptstring-functions"></a><span data-ttu-id="e6cd6-103">Usando as funções ScriptString</span><span class="sxs-lookup"><span data-stu-id="e6cd6-103">Using the ScriptString Functions</span></span>

<span data-ttu-id="e6cd6-104">Para um aplicativo lidando com texto não formatado, o Uniscribe fornece as funções de **ScriptString \*** .</span><span class="sxs-lookup"><span data-stu-id="e6cd6-104">For an application dealing with unformatted text, Uniscribe provides the **ScriptString\*** functions.</span></span> <span data-ttu-id="e6cd6-105">Essas funções são semelhantes a [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)e [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent), mas fornecem suporte completo a scripts complexos, incluindo o posicionamento do cursor.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-105">These functions are similar to [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext), and [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent), but they provide full complex script support, including caret placement.</span></span> <span data-ttu-id="e6cd6-106">Essas funções são semelhantes às outras funções do Uniscribe, mas são adaptadas aos requisitos mais simples de processamento de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-106">These functions are similar to the other Uniscribe functions, but are tailored to the simpler requirements of plain text processing.</span></span>

<span data-ttu-id="e6cd6-107">A tabela a seguir detalha as funções **ScriptString \*** e quaisquer contrapartes nas outras funções de Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-107">The following table details the **ScriptString\*** functions and any counterparts in the other Uniscribe functions.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e6cd6-108">Função</span><span class="sxs-lookup"><span data-stu-id="e6cd6-108">Function</span></span></th>
<th><span data-ttu-id="e6cd6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6cd6-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6cd6-110"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-110"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></span></span></td>
<td><span data-ttu-id="e6cd6-111">Analisa o texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-111">Analyzes plain text.</span></span> <span data-ttu-id="e6cd6-112">Essa função corresponde às seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="e6cd6-112">This function corresponds to the following functions:</span></span><br/> <dl><span data-ttu-id="e6cd6-113"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-113"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a></span></span><br /><span data-ttu-id="e6cd6-114">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-114">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a></span></span><br /><span data-ttu-id="e6cd6-115">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-115">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a></span></span><br /><span data-ttu-id="e6cd6-116">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-116">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a></span></span><br /><span data-ttu-id="e6cd6-117">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-117">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a></span></span><br /><span data-ttu-id="e6cd6-118">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-118">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a></span></span><br /><span data-ttu-id="e6cd6-119">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-119">
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6cd6-120"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-120"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></span></span></td>
<td><span data-ttu-id="e6cd6-121">Recupera a coordenada x para uma posição de caractere.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-121">Retrieves the x coordinate for a character position.</span></span> <span data-ttu-id="e6cd6-122">Essa função corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-122">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6cd6-123"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-123"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></span></span></td>
<td><span data-ttu-id="e6cd6-124">Libera uma estrutura de <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e6cd6-124">Frees a <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6cd6-125"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-125"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></span></span></td>
<td><span data-ttu-id="e6cd6-126">Converte larguras visuais em larguras lógicas.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-126">Converts visual widths to logical widths.</span></span> <span data-ttu-id="e6cd6-127">Essa função corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-127">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6cd6-128"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-128"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></span></span></td>
<td><span data-ttu-id="e6cd6-129">Mapeia posições de glifos de caracteres de forma semelhante a <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, apenas para uso herdado.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-129">Maps character glyph positions in a similar way to <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, for legacy use only.</span></span> <span data-ttu-id="e6cd6-130">Essa função não funciona bem com scripts que geram mais de um glifo por ponto de código.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-130">This function does not work well with scripts that generate more than one glyph per code point.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6cd6-131"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-131"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></span></span></td>
<td><span data-ttu-id="e6cd6-132">Exibe texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-132">Displays plain text.</span></span> <span data-ttu-id="e6cd6-133">Essa função corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-133">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6cd6-134"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-134"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></span></span></td>
<td><span data-ttu-id="e6cd6-135">Retorna um ponteiro para o comprimento de uma cadeia de caracteres de texto sem formatação recortada.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-135">Returns a pointer to the length of a clipped plain text string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6cd6-136"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-136"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></span></span></td>
<td><span data-ttu-id="e6cd6-137">Retorna um ponteiro para o buffer de atributos lógicos para uma cadeia de caracteres de texto sem formatação analisada.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-137">Returns a pointer to the logical attributes buffer for an analyzed plain text string.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6cd6-138"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-138"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></span></span></td>
<td><span data-ttu-id="e6cd6-139">Retorna um ponteiro para o tamanho (largura e altura) de uma cadeia de caracteres de texto sem formatação analisada.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-139">Returns a pointer to the size (width and height) for an analyzed plain text string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6cd6-140"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-140"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></span></span></td>
<td><span data-ttu-id="e6cd6-141">Identifica sequências de ponto de código não válidas no script especificado.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-141">Identifies code point sequences not valid in the given script.</span></span> <span data-ttu-id="e6cd6-142">Essa função é diferente de <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>, que identifica pontos de código que não estão presentes em uma fonte.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-142">This function is different from <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>, which identifies code points not present in a font.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6cd6-143"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6cd6-143"><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></span></span></td>
<td><span data-ttu-id="e6cd6-144">Converte uma coordenada x em uma posição de caractere.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-144">Converts an x coordinate to a character position.</span></span> <span data-ttu-id="e6cd6-145">Essa função corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-145">This function corresponds to <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e6cd6-146">Para exibir apenas texto sem formatação sem modificações, um aplicativo deve chamar [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)e, em seguida, [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree).</span><span class="sxs-lookup"><span data-stu-id="e6cd6-146">To only display plain text without any modifications, an application should call [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout), and then [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree).</span></span> <span data-ttu-id="e6cd6-147">As outras funções são usadas para modificar o texto sem formatação antes da exibição.</span><span class="sxs-lookup"><span data-stu-id="e6cd6-147">The other functions are used to modify the plain text before display.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6cd6-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6cd6-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6cd6-149">Usando o Uniscribe</span><span class="sxs-lookup"><span data-stu-id="e6cd6-149">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 
