---
description: Recupera dados específicos do aplicativo ou outros dados de propriedade para o identificador especificado.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: 'Método IContextNode:: GetPropertyData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 381d137dd73056a2a6f4c2e9cd3746f9f16c5b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647236"
---
# <a name="icontextnodegetpropertydata-method"></a><span data-ttu-id="9269f-103">Método IContextNode:: GetPropertyData</span><span class="sxs-lookup"><span data-stu-id="9269f-103">IContextNode::GetPropertyData method</span></span>

<span data-ttu-id="9269f-104">Recupera dados específicos do aplicativo ou outros dados de propriedade para o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="9269f-104">Retrieves application-specific data or other property data for the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="9269f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9269f-105">Syntax</span></span>


```C++
HRESULT GetPropertyData(
  [in]      const GUID  *pPropertyDataId,
  [in, out]       ULONG *pulPropertyDataSize,
  [out]           BYTE  **ppbPropertyData
);
```



## <a name="parameters"></a><span data-ttu-id="9269f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9269f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9269f-107">*pPropertyDataId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9269f-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9269f-108">O identificador dos dados.</span><span class="sxs-lookup"><span data-stu-id="9269f-108">The identifier for the data.</span></span>

</dd> <dt>

<span data-ttu-id="9269f-109">*pulPropertyDataSize* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="9269f-109">*pulPropertyDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9269f-110">O tamanho dos dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="9269f-110">The size of the data in bytes.</span></span> <span data-ttu-id="9269f-111">O valor que é passado não é usado.</span><span class="sxs-lookup"><span data-stu-id="9269f-111">The value that is passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9269f-112">*ppbPropertyData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9269f-112">*ppbPropertyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9269f-113">Um ponteiro para uma matriz de inteiros sem sinal de 8 bits que contém os dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="9269f-113">A pointer to an 8-bit unsigned integer array that contains the property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9269f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9269f-114">Return value</span></span>

<span data-ttu-id="9269f-115">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9269f-115">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9269f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9269f-116">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="9269f-117">Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *ppbPropertyData* quando você não precisar mais das informações.</span><span class="sxs-lookup"><span data-stu-id="9269f-117">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbPropertyData* when you no longer need the information.</span></span>

 

<span data-ttu-id="9269f-118">Além de recuperar dados específicos do aplicativo que foram adicionados com [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md), esse método é usado para recuperar propriedades comuns que são descritas pelas constantes de [Propriedades do nó de contexto](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="9269f-118">In addition to retrieving application-specific data that was added with [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md), this method is used to retrieve common properties that are described by the [Context Node Properties](context-node-properties.md) constants.</span></span>

<span data-ttu-id="9269f-119">As propriedades do tipo de cadeia de caracteres incluem:</span><span class="sxs-lookup"><span data-stu-id="9269f-119">The string-type properties include:</span></span>

-   <span data-ttu-id="9269f-120">GUID \_ CNP \_ reconhecívelstring</span><span class="sxs-lookup"><span data-stu-id="9269f-120">GUID\_CNP\_RECOGNIZEDSTRING</span></span>
-   <span data-ttu-id="9269f-121">GUID \_ CNP \_ FormatName</span><span class="sxs-lookup"><span data-stu-id="9269f-121">GUID\_CNP\_SHAPENAME</span></span>
-   <span data-ttu-id="9269f-122">GUID \_ AHP \_ ANALYSISHINTNAME</span><span class="sxs-lookup"><span data-stu-id="9269f-122">GUID\_AHP\_ANALYSISHINTNAME</span></span>
-   <span data-ttu-id="9269f-123">GUID \_ AHP \_ PREFIXTEXT</span><span class="sxs-lookup"><span data-stu-id="9269f-123">GUID\_AHP\_PREFIXTEXT</span></span>
-   <span data-ttu-id="9269f-124">GUID \_ AHP \_ SUFFIXTEXT</span><span class="sxs-lookup"><span data-stu-id="9269f-124">GUID\_AHP\_SUFFIXTEXT</span></span>
-   <span data-ttu-id="9269f-125">\_factor de AHP GUID \_</span><span class="sxs-lookup"><span data-stu-id="9269f-125">GUID\_AHP\_FACTOID</span></span>

<span data-ttu-id="9269f-126">O valor de retorno é \*\* \* WCHAR\*_. Se você converter o \_ parâmetro *ppbPropertyData* para \**WCHAR \**_ , seu comprimento retornado será `(length of the string + 1) _ sizeof(WCHAR)` .</span><span class="sxs-lookup"><span data-stu-id="9269f-126">The return value is \**WCHAR\**_. If you cast the \_*ppbPropertyData* parameter to \**WCHAR\**_ its returned length is `(length of the string + 1) _ sizeof(WCHAR)`.</span></span>

<span data-ttu-id="9269f-127">As propriedades do tipo booliano incluem:</span><span class="sxs-lookup"><span data-stu-id="9269f-127">The Boolean-type properties include:</span></span>

-   <span data-ttu-id="9269f-128">GUID \_ AHP \_ OVERRIDELANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="9269f-128">GUID\_AHP\_OVERRIDELANGUAGEID</span></span>
-   <span data-ttu-id="9269f-129">GUID \_ AHP \_ COERCETOFACTOID</span><span class="sxs-lookup"><span data-stu-id="9269f-129">GUID\_AHP\_COERCETOFACTOID</span></span>
-   <span data-ttu-id="9269f-130">GUID \_ AHP \_ WordMode</span><span class="sxs-lookup"><span data-stu-id="9269f-130">GUID\_AHP\_WORDMODE</span></span>

<span data-ttu-id="9269f-131">O valor de retorno **é \_ booliano de Variant**.</span><span class="sxs-lookup"><span data-stu-id="9269f-131">The return value is **VARIANT\_BOOL**.</span></span> <span data-ttu-id="9269f-132">Se você converter o \* parâmetro *ppbPropertyData* para \**Variant \_ bool \** _, seu comprimento retornado será `sizeof(VARIANT_BOOL)` .</span><span class="sxs-lookup"><span data-stu-id="9269f-132">If you cast the \**ppbPropertyData* parameter to \**VARIANT\_BOOL\** _ its returned length is `sizeof(VARIANT_BOOL)`.</span></span>

<span data-ttu-id="9269f-133">GUID \_ AHP \_ guia é uma propriedade do tipo guia.</span><span class="sxs-lookup"><span data-stu-id="9269f-133">GUID\_AHP\_GUIDE is a guide-type property.</span></span> <span data-ttu-id="9269f-134">O valor de retorno _*é \* InkAnalysisRecognitionGuide*_.</span><span class="sxs-lookup"><span data-stu-id="9269f-134">The return value is _*InkAnalysisRecognitionGuide\**_.</span></span> <span data-ttu-id="9269f-135">Se você converter o \_ parâmetro *ppbPropertyData* para \**InkAnalysisRecognitionGuide \**, seu comprimento retornado será `sizeof(InkAnalysisRecognitionGuide)` .</span><span class="sxs-lookup"><span data-stu-id="9269f-135">If you cast the \_*ppbPropertyData* parameter to \**InkAnalysisRecognitionGuide\** _ its returned length is `sizeof(InkAnalysisRecognitionGuide)`.</span></span>

<span data-ttu-id="9269f-136">As propriedades do tipo inteiro incluem:</span><span class="sxs-lookup"><span data-stu-id="9269f-136">Integer-type properties include:</span></span>

-   <span data-ttu-id="9269f-137">GUID \_ CNP \_ LINENUMBER</span><span class="sxs-lookup"><span data-stu-id="9269f-137">GUID\_CNP\_LINENUMBER</span></span>
-   <span data-ttu-id="9269f-138">GUID \_ CNP \_ POINTSPERINCH</span><span class="sxs-lookup"><span data-stu-id="9269f-138">GUID\_CNP\_POINTSPERINCH</span></span>
-   <span data-ttu-id="9269f-139">GUID \_ CNP \_ CONFIDENCELEVEL</span><span class="sxs-lookup"><span data-stu-id="9269f-139">GUID\_CNP\_CONFIDENCELEVEL</span></span>
-   <span data-ttu-id="9269f-140">\_confirmação de CNP GUID \_</span><span class="sxs-lookup"><span data-stu-id="9269f-140">GUID\_CNP\_CONFIRMATION</span></span>
-   <span data-ttu-id="9269f-141">GUID \_ CNP \_ MAXIMUMSTROKECOUNT</span><span class="sxs-lookup"><span data-stu-id="9269f-141">GUID\_CNP\_MAXIMUMSTROKECOUNT</span></span>
-   <span data-ttu-id="9269f-142">\_segmentação de CNP GUID \_</span><span class="sxs-lookup"><span data-stu-id="9269f-142">GUID\_CNP\_SEGMENTATION</span></span>
-   <span data-ttu-id="9269f-143">GUID \_ CNP \_ ALIGNMENTLEVEL</span><span class="sxs-lookup"><span data-stu-id="9269f-143">GUID\_CNP\_ALIGNMENTLEVEL</span></span>

<span data-ttu-id="9269f-144">O valor de retorno _*é \* longo*_.</span><span class="sxs-lookup"><span data-stu-id="9269f-144">The return value is _*LONG\**_.</span></span> <span data-ttu-id="9269f-145">Se você converter o \_ parâmetro *ppbPropertyData* para \**Long \** _, seu comprimento retornado será `sizeof(LONG)` .</span><span class="sxs-lookup"><span data-stu-id="9269f-145">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)`.</span></span>

<span data-ttu-id="9269f-146">Métricas de linha – as propriedades do tipo incluem:</span><span class="sxs-lookup"><span data-stu-id="9269f-146">Line metrics-type properties include:</span></span>

-   <span data-ttu-id="9269f-147">GUID \_ CNP \_ ascendentes</span><span class="sxs-lookup"><span data-stu-id="9269f-147">GUID\_CNP\_ASCENDERS</span></span>
-   <span data-ttu-id="9269f-148">GUID \_ CNP \_ descendentes</span><span class="sxs-lookup"><span data-stu-id="9269f-148">GUID\_CNP\_DESCENDERS</span></span>
-   <span data-ttu-id="9269f-149">\_linha de \_ base CNP GUID</span><span class="sxs-lookup"><span data-stu-id="9269f-149">GUID\_CNP\_BASELINE</span></span>
-   <span data-ttu-id="9269f-150">GUID \_ CNP \_ Tabs no meio</span><span class="sxs-lookup"><span data-stu-id="9269f-150">GUID\_CNP\_MIDLINE</span></span>

<span data-ttu-id="9269f-151">O valor de retorno _*é \* longo*_.</span><span class="sxs-lookup"><span data-stu-id="9269f-151">The return value is _*LONG\**_.</span></span> <span data-ttu-id="9269f-152">Se você converter o \_ parâmetro *ppbPropertyData* para \**Long \** _, seu comprimento retornado será `sizeof(LONG)_4` , significando os valores (x, y) para os pontos iniciais seguidos dos valores (x, y) dos pontos finais.</span><span class="sxs-lookup"><span data-stu-id="9269f-152">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)_4`, signifying the (x, y) values for the starting points followed by the (x, y) values for the ending points.</span></span>

<span data-ttu-id="9269f-153">GUID \_ CNP \_ TEXTRECOGNIZERID é uma propriedade **GUID** .</span><span class="sxs-lookup"><span data-stu-id="9269f-153">GUID\_CNP\_TEXTRECOGNIZERID is a **GUID** property.</span></span> <span data-ttu-id="9269f-154">O valor de retorno é \*\* \* GUID\*_. Se você converter o \_ parâmetro *ppbPropertyData* para \**GUID \** ,_ seu comprimento retornado será `sizeof(GUID)` .</span><span class="sxs-lookup"><span data-stu-id="9269f-154">The return value is \**GUID\**_. If you cast the \_*ppbPropertyData* parameter to \**GUID\**_ its returned length is `sizeof(GUID)`.</span></span>

<span data-ttu-id="9269f-155">GUID \_ CNP \_ ROTATEDBOUNDINGBOX é uma propriedade de caixa delimitadora girada.</span><span class="sxs-lookup"><span data-stu-id="9269f-155">GUID\_CNP\_ROTATEDBOUNDINGBOX is a rotated bounding box property.</span></span> <span data-ttu-id="9269f-156">O valor de retorno _*é \* longo*_.</span><span class="sxs-lookup"><span data-stu-id="9269f-156">The return value is _*LONG\**_.</span></span> <span data-ttu-id="9269f-157">Se você converter o \_ parâmetro *ppbPropertyData* para \**Long \** _, seu comprimento retornado será `sizeof(LONG)_8` , significando os valores (x, y) para os quatro cantos da caixa.</span><span class="sxs-lookup"><span data-stu-id="9269f-157">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)_8`, signifying the (x, y) values for the four corners of the box.</span></span>

<span data-ttu-id="9269f-158">GUID \_ CNP \_ HOTPOINT é uma propriedade de ponto de acesso.</span><span class="sxs-lookup"><span data-stu-id="9269f-158">GUID\_CNP\_HOTPOINT is a hot point property.</span></span> <span data-ttu-id="9269f-159">O valor de retorno é \*\* \* Long\*_. Se você converter o \_ parâmetro *ppbPropertyData* para \**longo \**_ seu comprimento retornado é `sizeof(LONG)_2` , significando os valores (x, y) para o ponto.</span><span class="sxs-lookup"><span data-stu-id="9269f-159">The return value is \**LONG\**_. If you cast the \_*ppbPropertyData* parameter to \**LONG\**_ its returned length is `sizeof(LONG)_2`, signifying the (x, y) values for the point.</span></span>

<span data-ttu-id="9269f-160">\_O AHP \_ de palavras do GUID é uma propriedade da lista de palavras.</span><span class="sxs-lookup"><span data-stu-id="9269f-160">GUID\_AHP\_WORDLIST is a word list property.</span></span> <span data-ttu-id="9269f-161">O valor de retorno é \*\* \* WCHAR\*_. Se você converter o \_ parâmetro *ppbPropertyData* para \**WCHAR \**_ , seu comprimento retornado será `n _ sizeof(WCHAR)` , em que `n` é a soma dos comprimentos das cadeias de caracteres do número de cadeias na lista mais 1 para cada caractere de término **nulo** para cada cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9269f-161">The return value is \**WCHAR\**_. If you cast the \_*ppbPropertyData* parameter to \**WCHAR\**_ its returned length is `n _ sizeof(WCHAR)`, where `n` is the sum of the string lengths of the number of strings in the list plus 1 for each **NULL** termination character for each string.</span></span>

## <a name="examples"></a><span data-ttu-id="9269f-162">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9269f-162">Examples</span></span>

<span data-ttu-id="9269f-163">Este exemplo mostra um método que acessa a propriedade do nó de contexto AlignmentLevel de um tipo de nó de contexto de parágrafo.</span><span class="sxs-lookup"><span data-stu-id="9269f-163">This example shows a method that accesses the AlignmentLevel context node property of a Paragraph context node type.</span></span>


```C++
// Checks a paragraph context node's alignment level property.
// Only paragraph type context nodes contain the alignment level property.
HRESULT CMyClass::ExploreParagraphNode(
    IContextNode *pParagraphNode)
{
    // Get the AlignmentLevel property data for the paragraph.
    LONG * alignmentLevel = NULL;
    ULONG ulDataLen = 0;

    HRESULT hr = pParagraphNode->GetPropertyData(
        (const GUID*)&GUID_CNP_ALIGNMENTLEVEL,
        &ulDataLen,
        (BYTE**)&alignmentLevel);

    if( FAILED(hr) ||
        ulDataLen != sizeof(LONG) ||
        alignmentLevel == NULL )
    {
        // Insert code that handles an error here.
    }
    else
    {
        // Insert code that uses the alignment level here.
    }

    // Free the memory allocated for the property data.
    ::CoTaskMemFree(alignmentLevel);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="9269f-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9269f-164">Requirements</span></span>



| <span data-ttu-id="9269f-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="9269f-165">Requirement</span></span> | <span data-ttu-id="9269f-166">Valor</span><span class="sxs-lookup"><span data-stu-id="9269f-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9269f-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9269f-167">Minimum supported client</span></span><br/> | <span data-ttu-id="9269f-168">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9269f-168">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9269f-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9269f-169">Minimum supported server</span></span><br/> | <span data-ttu-id="9269f-170">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9269f-170">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9269f-171">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9269f-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="9269f-172"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9269f-172"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9269f-173">DLL</span><span class="sxs-lookup"><span data-stu-id="9269f-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9269f-174"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9269f-174"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9269f-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="9269f-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9269f-176">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="9269f-176">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9269f-177">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="9269f-177">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="9269f-178">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="9269f-178">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="9269f-179">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="9269f-179">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="9269f-180">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="9269f-180">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="9269f-181">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="9269f-181">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="9269f-182">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="9269f-182">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="9269f-183">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="9269f-183">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

