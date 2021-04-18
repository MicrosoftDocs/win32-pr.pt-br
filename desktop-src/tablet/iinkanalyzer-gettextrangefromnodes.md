---
description: Localiza o intervalo de texto na cadeia de caracteres reconhecida que corresponde a uma coleção de objetos IContextNode.
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: 'Método IInkAnalyzer:: GetTextRangeFromNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetTextRangeFromNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da27206a33ca58cebd10192393c4cf2efd1d5919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768324"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a><span data-ttu-id="57f2f-103">Método IInkAnalyzer:: GetTextRangeFromNodes</span><span class="sxs-lookup"><span data-stu-id="57f2f-103">IInkAnalyzer::GetTextRangeFromNodes method</span></span>

<span data-ttu-id="57f2f-104">Localiza o intervalo de texto na cadeia de caracteres reconhecida que corresponde a uma coleção de objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="57f2f-104">Finds the text range in the recognized string that corresponds to a collection of [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="57f2f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57f2f-105">Syntax</span></span>


```C++
HRESULT GetTextRangeFromNodes(
  [out] LONG          *plStart,
  [out] LONG          *plLength,
  [in]  IContextNodes *pNodesToSearch
);
```



## <a name="parameters"></a><span data-ttu-id="57f2f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57f2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57f2f-107">*plStart* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="57f2f-107">*plStart* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57f2f-108">Um inteiro com sinal de 32 bits que indica o início do intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="57f2f-108">A 32-bit signed integer that indicates the start of the text range.</span></span> <span data-ttu-id="57f2f-109">Este parâmetro é passado não inicializado.</span><span class="sxs-lookup"><span data-stu-id="57f2f-109">This parameter is passed uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="57f2f-110">*plLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="57f2f-110">*plLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57f2f-111">Um inteiro com sinal de 32 bits que indica o comprimento do intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="57f2f-111">A 32-bit signed integer that indicates the length of the text range.</span></span> <span data-ttu-id="57f2f-112">Este parâmetro é passado não inicializado.</span><span class="sxs-lookup"><span data-stu-id="57f2f-112">This parameter is passed uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="57f2f-113">*pNodesToSearch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="57f2f-113">*pNodesToSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57f2f-114">A coleção de objetos [**IContextNode**](icontextnode.md) para os quais encontrar o intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="57f2f-114">The collection of [**IContextNode**](icontextnode.md) objects for which to find the text range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57f2f-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57f2f-115">Return value</span></span>

<span data-ttu-id="57f2f-116">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="57f2f-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="57f2f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="57f2f-117">Remarks</span></span>

<span data-ttu-id="57f2f-118">Se *pNodesToSearch* contiver objetos [**IContextNode**](icontextnode.md) que não são adjacentes, esse método retornará o menor intervalo de texto que abrange todos os objetos **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="57f2f-118">If *pNodesToSearch* contains [**IContextNode**](icontextnode.md) objects that are not adjacent, this method returns the smallest text range that covers all of the **IContextNode** objects.</span></span>

<span data-ttu-id="57f2f-119">Esse método gera uma \_ exceção E INVALIDARG quando *pNodesToSearch* contém um [**IContextNode**](icontextnode.md) que não está associado ao [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="57f2f-119">This method throws an E\_INVALIDARG exception when *pNodesToSearch* contains an [**IContextNode**](icontextnode.md) that is not associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57f2f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57f2f-120">Requirements</span></span>



| <span data-ttu-id="57f2f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="57f2f-121">Requirement</span></span> | <span data-ttu-id="57f2f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="57f2f-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57f2f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57f2f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="57f2f-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="57f2f-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="57f2f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57f2f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="57f2f-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="57f2f-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="57f2f-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57f2f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="57f2f-128"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="57f2f-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="57f2f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="57f2f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57f2f-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57f2f-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="57f2f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="57f2f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57f2f-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="57f2f-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




