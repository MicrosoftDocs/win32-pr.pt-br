---
description: Fornece uma pesquisa difusa, sem diferenciação de maiúsculas e minúsculas, para os traços de escrita analisado e os traços de desenho analisados que têm tipos reconhecidos.
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: 'Método IInkAnalyzer:: Search (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Search
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ea9755c0f2836b363b967a3d6bfdc5d64a1305b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090517"
---
# <a name="iinkanalyzersearch-method"></a><span data-ttu-id="b25c1-103">Método IInkAnalyzer:: Search</span><span class="sxs-lookup"><span data-stu-id="b25c1-103">IInkAnalyzer::Search method</span></span>

<span data-ttu-id="b25c1-104">Fornece uma pesquisa difusa, sem diferenciação de maiúsculas e minúsculas, para os traços de escrita analisado e os traços de desenho analisados que têm tipos reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="b25c1-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="b25c1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b25c1-105">Syntax</span></span>


```C++
HRESULT Search(
  [in]      BSTR  bstrPhraseToMatch,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="b25c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b25c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b25c1-107">*bstrPhraseToMatch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b25c1-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b25c1-108">A frase que será encontrada nas alternativas para os traços analisados no momento.</span><span class="sxs-lookup"><span data-stu-id="b25c1-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="b25c1-109">*pulSearchResultCount* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b25c1-109">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b25c1-110">O número máximo de resultados retornados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b25c1-110">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="b25c1-111">*ppulStrokeCountPerResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b25c1-111">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b25c1-112">Ponteiro para uma matriz do número de traços em cada resultado da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b25c1-112">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="b25c1-113">*pulStrokeIdsCount* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b25c1-113">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b25c1-114">O número de IDs de traço em *ppulStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="b25c1-114">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="b25c1-115">*ppulStrokeIds* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b25c1-115">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b25c1-116">Ponteiro para uma matriz de IDs de traço que representa um conjunto de conjuntos de traços.</span><span class="sxs-lookup"><span data-stu-id="b25c1-116">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b25c1-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b25c1-117">Return value</span></span>

<span data-ttu-id="b25c1-118">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b25c1-118">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b25c1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b25c1-119">Remarks</span></span>

<span data-ttu-id="b25c1-120">Esta pesquisa localiza subcadeias de caracteres de várias palavras e de palavras únicas.</span><span class="sxs-lookup"><span data-stu-id="b25c1-120">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="b25c1-121">Os resultados de reconhecimento alternativos e as segmentações alternativas são pesquisados.</span><span class="sxs-lookup"><span data-stu-id="b25c1-121">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="b25c1-122">Todas as cadeias de caracteres de entrada serão convertidas em uma única caixa para comparação, utilizando o LCID do thread atual para fazer essa conversão para respeitar as convenções de casos culturais.</span><span class="sxs-lookup"><span data-stu-id="b25c1-122">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="b25c1-123">A cadeia de caracteres passada é tratada como uma frase.</span><span class="sxs-lookup"><span data-stu-id="b25c1-123">The string passed is treated as a phrase.</span></span> <span data-ttu-id="b25c1-124">Palavras e caracteres devem aparecer no alterantes para os traços na ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="b25c1-124">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="b25c1-125">A primeira e última palavras da frase podem ser correspondidas como subcadeias de caracteres (a primeira palavra que aparece no final de uma alternativa e a última palavra que aparece no begginging de uma), mas quaisquer outras palavras (aquelas dentro da frase) devem aparecer como palavras inteiras.</span><span class="sxs-lookup"><span data-stu-id="b25c1-125">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="b25c1-126">Se a cadeia de caracteres passada não tiver espaço em branco entre os caracteres, a subcadeia de caracteres poderá ser encontrada em qualquer lugar dentro de uma única palavra em uma alternativa.</span><span class="sxs-lookup"><span data-stu-id="b25c1-126">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="b25c1-127">Somente a presença ou a ausência de espaço em branco entre caracteres altera os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b25c1-127">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="b25c1-128">O espaço em branco que não está entre caracteres é ignorado.</span><span class="sxs-lookup"><span data-stu-id="b25c1-128">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="b25c1-129">O tipo de espaço em branco é ignorado (uma guia ou um espaço entre os caracteres fornecerá o mesmo resultado).</span><span class="sxs-lookup"><span data-stu-id="b25c1-129">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="b25c1-130">A quantidade de espaço em branco não importa, um espaço ou dois espaços entre caracteres fornecerá o mesmo resultado.</span><span class="sxs-lookup"><span data-stu-id="b25c1-130">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="b25c1-131">A pesquisa não gera eventos PopulateContextNode.</span><span class="sxs-lookup"><span data-stu-id="b25c1-131">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="b25c1-132">Somente os traços que já foram preenchidos serão pesquisados.</span><span class="sxs-lookup"><span data-stu-id="b25c1-132">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="b25c1-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b25c1-133">Requirements</span></span>



| <span data-ttu-id="b25c1-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b25c1-134">Requirement</span></span> | <span data-ttu-id="b25c1-135">Valor</span><span class="sxs-lookup"><span data-stu-id="b25c1-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b25c1-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b25c1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b25c1-137">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b25c1-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b25c1-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b25c1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b25c1-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b25c1-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b25c1-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b25c1-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b25c1-141"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b25c1-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b25c1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b25c1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b25c1-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b25c1-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b25c1-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="b25c1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b25c1-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b25c1-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




