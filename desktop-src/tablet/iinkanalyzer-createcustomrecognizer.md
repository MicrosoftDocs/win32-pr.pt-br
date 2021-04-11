---
description: Cria um novo nó de reconhecedor personalizado para o IInkAnalyzer.
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: 'Método IInkAnalyzer:: CreateCustomRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 70cc5741faa8d54d09af000d4dbbb3c0fc423df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164542"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a><span data-ttu-id="00d9d-103">Método IInkAnalyzer:: CreateCustomRecognizer</span><span class="sxs-lookup"><span data-stu-id="00d9d-103">IInkAnalyzer::CreateCustomRecognizer method</span></span>

<span data-ttu-id="00d9d-104">Cria um novo nó de reconhecedor personalizado para o [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="00d9d-104">Creates a new custom recognizer node for the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="00d9d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00d9d-105">Syntax</span></span>


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="00d9d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00d9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00d9d-107">*pInkAnalysisRecognizerId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="00d9d-107">*pInkAnalysisRecognizerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d9d-108">O GUID (identificador global exclusivo) do [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) para o qual criar um nó.</span><span class="sxs-lookup"><span data-stu-id="00d9d-108">The globally unique identifier (GUID) of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) for which to create a node.</span></span>

</dd> <dt>

<span data-ttu-id="00d9d-109">*ppContextNode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="00d9d-109">*ppContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00d9d-110">Um ponteiro para o objeto [**IContextNode**](icontextnode.md) que representa o novo nó de reconhecedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="00d9d-110">A pointer to the [**IContextNode**](icontextnode.md) object representing the new custom recognizer node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00d9d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00d9d-111">Return value</span></span>

<span data-ttu-id="00d9d-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="00d9d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="00d9d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="00d9d-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="00d9d-114">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em ppContextNode quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="00d9d-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on ppContextNode when you no longer need to use the object.</span></span>

 

<span data-ttu-id="00d9d-115">Esse método cria um novo [**IContextNode**](icontextnode.md) com um tipo de CustomRecognizer (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="00d9d-115">This method creates a new [**IContextNode**](icontextnode.md) with a type of CustomRecognizer (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="00d9d-116">Em seguida, ele adiciona o novo nó de reconhecedor personalizado à coleção de subnós do nó raiz do objeto [**IInkAnalyzer**](iinkanalyzer.md) (consulte o método [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) e [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="00d9d-116">It then adds the new custom recognizer node to the subnodes collection of the [**IInkAnalyzer**](iinkanalyzer.md) object's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="00d9d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00d9d-117">Requirements</span></span>



| <span data-ttu-id="00d9d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="00d9d-118">Requirement</span></span> | <span data-ttu-id="00d9d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="00d9d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d9d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00d9d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="00d9d-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="00d9d-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="00d9d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00d9d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="00d9d-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="00d9d-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="00d9d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00d9d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="00d9d-125"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="00d9d-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="00d9d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="00d9d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00d9d-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00d9d-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="00d9d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="00d9d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d9d-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="00d9d-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="00d9d-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="00d9d-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="00d9d-131">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="00d9d-131">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="00d9d-132">**Método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**</span><span class="sxs-lookup"><span data-stu-id="00d9d-132">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="00d9d-133">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="00d9d-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

