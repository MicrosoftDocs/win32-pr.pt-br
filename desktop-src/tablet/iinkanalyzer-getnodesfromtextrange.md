---
description: Recupera uma coleção de objetos IContextNode que são relevantes para o intervalo de texto especificado para os nós de contexto especificados.
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: 'Método IInkAnalyzer:: GetNodesFromTextRange (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetNodesFromTextRange
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ada60a64bb4e7d8b4604b18982630dabd7e44256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647227"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a><span data-ttu-id="d34ff-103">Método IInkAnalyzer:: GetNodesFromTextRange</span><span class="sxs-lookup"><span data-stu-id="d34ff-103">IInkAnalyzer::GetNodesFromTextRange method</span></span>

<span data-ttu-id="d34ff-104">Recupera uma coleção de objetos [**IContextNode**](icontextnode.md) que são relevantes para o intervalo de texto especificado para os nós de contexto especificados.</span><span class="sxs-lookup"><span data-stu-id="d34ff-104">Retrieves a collection of [**IContextNode**](icontextnode.md) objects that are relevant to the specified text range for the specified context nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d34ff-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d34ff-105">Syntax</span></span>


```C++
HRESULT GetNodesFromTextRange(
  [in, out] LONG          *plStart,
  [in, out] LONG          *plLength,
  [out]     IContextNodes **ppContextNodes,
  [in]      IContextNodes *pNodesToSearch = defaultvalue
);
```



## <a name="parameters"></a><span data-ttu-id="d34ff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d34ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d34ff-107">*plStart* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d34ff-107">*plStart* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d34ff-108">Uma referência ao início do intervalo de texto na parte *pNodesToSearch* da cadeia de caracteres reconhecida.</span><span class="sxs-lookup"><span data-stu-id="d34ff-108">A reference to the start of the text range in the *pNodesToSearch* portion of the recognized string.</span></span>

</dd> <dt>

<span data-ttu-id="d34ff-109">*plLength* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d34ff-109">*plLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d34ff-110">Uma referência ao comprimento do intervalo de texto na parte *pNodesToSearch* da cadeia de caracteres reconhecida.</span><span class="sxs-lookup"><span data-stu-id="d34ff-110">A reference to the length of the text range in the *pNodesToSearch* portion of the recognized string.</span></span>

</dd> <dt>

<span data-ttu-id="d34ff-111">*ppContextNodes* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d34ff-111">*ppContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d34ff-112">Um ponteiro para os objetos [**IContextNode**](icontextnode.md) que são relevantes para o intervalo de texto especificado para os nós de contexto especificados.</span><span class="sxs-lookup"><span data-stu-id="d34ff-112">A pointer to the [**IContextNode**](icontextnode.md) objects that are relevant to the specified text range for the specified context nodes.</span></span>

</dd> <dt>

<span data-ttu-id="d34ff-113">*pNodesToSearch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d34ff-113">*pNodesToSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34ff-114">Os objetos [**IContextNode**](icontextnode.md) para limitar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d34ff-114">The [**IContextNode**](icontextnode.md) objects to which to limit the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d34ff-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d34ff-115">Return value</span></span>

<span data-ttu-id="d34ff-116">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d34ff-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d34ff-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d34ff-117">Remarks</span></span>

<span data-ttu-id="d34ff-118">O intervalo de texto especificado deve ser relativo à parte *pNodesToSearch* da cadeia de caracteres reconhecida do [**IInkAnalyzer**](iinkanalyzer.md), e não à cadeia de caracteres reconhecida do **IInkAnalyzer** inteiro.</span><span class="sxs-lookup"><span data-stu-id="d34ff-118">The specified text range should be relative to the *pNodesToSearch* portion of the recognized string of the [**IInkAnalyzer**](iinkanalyzer.md), rather than to the recognized string of the entire **IInkAnalyzer**.</span></span>

<span data-ttu-id="d34ff-119">Esse método modifica os valores dos parâmetros *plStart* e *plLength* expandindo o intervalo de texto para os limites de palavras mais próximos.</span><span class="sxs-lookup"><span data-stu-id="d34ff-119">This method modifies the values of the *plStart* and *plLength* parameters by expanding the text range to the nearest word boundaries.</span></span>

<span data-ttu-id="d34ff-120">Por exemplo, se a cadeia de caracteres reconhecida for "Estou atrasado" e você chamar esse método usando os valores de parâmetro de 6 para *plStart* e 1 para *plLength*, que corresponde à letra "a" em "tardia", esse método retornará uma coleção que contém um único [**IContextNode**](icontextnode.md), o InkWord ou o textword que corresponde à palavra "tardia".</span><span class="sxs-lookup"><span data-stu-id="d34ff-120">For example, if the recognized string is "I am late" and you call this method using the parameter values of 6 for *plStart* and 1 for *plLength*, which corresponds to the letter "a" in "late", this method returns a collection containing a single [**IContextNode**](icontextnode.md), the InkWord or TextWord that corresponds to the word "late".</span></span> <span data-ttu-id="d34ff-121">Para este exemplo, esse método também modifica o valor de *plStart* para 5 e o valor de *plLength* para 4, que corresponde à palavra "tardia".</span><span class="sxs-lookup"><span data-stu-id="d34ff-121">For this example, this method also modifies the value of *plStart* to 5 and the value of *plLength* to 4, which corresponds to the word "late".</span></span>

> [!Note]  
> <span data-ttu-id="d34ff-122">O parâmetro *plStart* é relativo à cadeia de caracteres reconhecida do parâmetro *pNodesToSearch* .</span><span class="sxs-lookup"><span data-stu-id="d34ff-122">The *plStart* parameter is relative to the recognized string of the *pNodesToSearch* parameter.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d34ff-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d34ff-123">Requirements</span></span>



| <span data-ttu-id="d34ff-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d34ff-124">Requirement</span></span> | <span data-ttu-id="d34ff-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d34ff-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d34ff-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d34ff-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d34ff-127">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d34ff-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d34ff-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d34ff-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d34ff-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d34ff-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d34ff-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d34ff-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d34ff-131"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d34ff-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d34ff-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d34ff-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d34ff-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d34ff-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d34ff-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d34ff-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34ff-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d34ff-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




