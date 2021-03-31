---
description: Fornece uma pesquisa difusa, sem diferenciação de maiúsculas e minúsculas, para os traços de escrita analisado e os traços de desenho analisados que têm tipos reconhecidos.
ms.assetid: dfd481f9-38fd-433f-b1fc-697c735c13da
title: 'Método IInkAnalyzer:: SearchWithLanguageId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SearchWithLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 829878a6fd326abb8a685b644cfc222ba6921385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647223"
---
# <a name="iinkanalyzersearchwithlanguageid-method"></a><span data-ttu-id="e7a09-103">Método IInkAnalyzer:: SearchWithLanguageId</span><span class="sxs-lookup"><span data-stu-id="e7a09-103">IInkAnalyzer::SearchWithLanguageId method</span></span>

<span data-ttu-id="e7a09-104">Fornece uma pesquisa difusa, sem diferenciação de maiúsculas e minúsculas, para os traços de escrita analisado e os traços de desenho analisados que têm tipos reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="e7a09-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a09-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7a09-105">Syntax</span></span>


```C++
HRESULT SearchWithLanguageId(
  [in]      BSTR  bstrPhraseToMatch,
  [in]      LONG  lSearchStringLanguageId,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="e7a09-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7a09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7a09-107">*bstrPhraseToMatch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7a09-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a09-108">A frase que será encontrada nas alternativas para os traços analisados no momento.</span><span class="sxs-lookup"><span data-stu-id="e7a09-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="e7a09-109">*lSearchStringLanguageId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7a09-109">*lSearchStringLanguageId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a09-110">O LCID associado à cadeia de caracteres que é passada.</span><span class="sxs-lookup"><span data-stu-id="e7a09-110">The LCID associated with the string that is passed.</span></span> <span data-ttu-id="e7a09-111">Usado para converter o caso internamente para dar suporte a comparações que não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e7a09-111">Used to convert the case internally to support case insensitive comparisons.</span></span>

</dd> <dt>

<span data-ttu-id="e7a09-112">*pulSearchResultCount* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e7a09-112">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a09-113">O número máximo de resultados retornados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e7a09-113">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="e7a09-114">*ppulStrokeCountPerResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e7a09-114">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a09-115">Ponteiro para uma matriz do número de traços em cada resultado da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e7a09-115">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="e7a09-116">*pulStrokeIdsCount* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e7a09-116">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a09-117">O número de IDs de traço em *ppulStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="e7a09-117">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="e7a09-118">*ppulStrokeIds* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e7a09-118">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a09-119">Ponteiro para uma matriz de IDs de traço que representa um conjunto de conjuntos de traços.</span><span class="sxs-lookup"><span data-stu-id="e7a09-119">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7a09-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7a09-120">Return value</span></span>

<span data-ttu-id="e7a09-121">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e7a09-121">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7a09-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7a09-122">Remarks</span></span>

<span data-ttu-id="e7a09-123">Esta pesquisa localiza subcadeias de caracteres de várias palavras e de palavras únicas.</span><span class="sxs-lookup"><span data-stu-id="e7a09-123">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="e7a09-124">Os resultados de reconhecimento alternativos e as segmentações alternativas são pesquisados.</span><span class="sxs-lookup"><span data-stu-id="e7a09-124">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="e7a09-125">Todas as cadeias de caracteres de entrada serão convertidas em uma única caixa para comparação, utilizando o LCID do thread atual para fazer essa conversão para respeitar as convenções de casos culturais.</span><span class="sxs-lookup"><span data-stu-id="e7a09-125">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="e7a09-126">A cadeia de caracteres passada é tratada como uma frase.</span><span class="sxs-lookup"><span data-stu-id="e7a09-126">The string passed is treated as a phrase.</span></span> <span data-ttu-id="e7a09-127">Palavras e caracteres devem aparecer no alterantes para os traços na ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="e7a09-127">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="e7a09-128">A primeira e última palavras da frase podem ser correspondidas como subcadeias de caracteres (a primeira palavra que aparece no final de uma alternativa e a última palavra que aparece no begginging de uma), mas quaisquer outras palavras (aquelas dentro da frase) devem aparecer como palavras inteiras.</span><span class="sxs-lookup"><span data-stu-id="e7a09-128">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="e7a09-129">Se a cadeia de caracteres passada não tiver espaço em branco entre os caracteres, a subcadeia de caracteres poderá ser encontrada em qualquer lugar dentro de uma única palavra em uma alternativa.</span><span class="sxs-lookup"><span data-stu-id="e7a09-129">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="e7a09-130">Somente a presença ou a ausência de espaço em branco entre caracteres altera os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e7a09-130">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="e7a09-131">O espaço em branco que não está entre caracteres é ignorado.</span><span class="sxs-lookup"><span data-stu-id="e7a09-131">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="e7a09-132">O tipo de espaço em branco é ignorado (uma guia ou um espaço entre os caracteres fornecerá o mesmo resultado).</span><span class="sxs-lookup"><span data-stu-id="e7a09-132">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="e7a09-133">A quantidade de espaço em branco não importa, um espaço ou dois espaços entre caracteres fornecerá o mesmo resultado.</span><span class="sxs-lookup"><span data-stu-id="e7a09-133">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="e7a09-134">A pesquisa não gera eventos PopulateContextNode.</span><span class="sxs-lookup"><span data-stu-id="e7a09-134">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="e7a09-135">Somente os traços que já foram preenchidos serão pesquisados.</span><span class="sxs-lookup"><span data-stu-id="e7a09-135">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7a09-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7a09-136">Requirements</span></span>



| <span data-ttu-id="e7a09-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7a09-137">Requirement</span></span> | <span data-ttu-id="e7a09-138">Valor</span><span class="sxs-lookup"><span data-stu-id="e7a09-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a09-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7a09-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e7a09-140">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e7a09-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e7a09-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7a09-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e7a09-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e7a09-142">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e7a09-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7a09-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7a09-144"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e7a09-144"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e7a09-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e7a09-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7a09-146"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7a09-146"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e7a09-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7a09-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7a09-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e7a09-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




