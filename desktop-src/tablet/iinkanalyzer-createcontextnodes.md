---
description: Cria um objeto IContextNodes.
ms.assetid: d6d37595-307b-4cbc-9d48-ad10f8b272dd
title: 'Método IInkAnalyzer:: CreateContextNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07bdfc9a32fd4aec8e716cdd3c788c211c1adaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787660"
---
# <a name="iinkanalyzercreatecontextnodes-method"></a><span data-ttu-id="3f4d7-103">Método IInkAnalyzer:: CreateContextNodes</span><span class="sxs-lookup"><span data-stu-id="3f4d7-103">IInkAnalyzer::CreateContextNodes method</span></span>

<span data-ttu-id="3f4d7-104">Cria um objeto [**IContextNodes**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="3f4d7-104">Creates an [**IContextNodes**](icontextnodes.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f4d7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f4d7-105">Syntax</span></span>


```C++
HRESULT CreateContextNodes(
  [out] IContextNodes **ppContextNodes
);
```



## <a name="parameters"></a><span data-ttu-id="3f4d7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f4d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f4d7-107">*ppContextNodes* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3f4d7-107">*ppContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f4d7-108">Um ponteiro para o objeto [**IContextNodes**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="3f4d7-108">A pointer to the [**IContextNodes**](icontextnodes.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f4d7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f4d7-109">Return value</span></span>

<span data-ttu-id="3f4d7-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3f4d7-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f4d7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f4d7-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="3f4d7-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodes* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="3f4d7-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodes* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="3f4d7-113">Use este método para criar uma coleção [**IContextNodes**](icontextnodes.md) vazia que está associada ao [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="3f4d7-113">Use this method to create an empty [**IContextNodes**](icontextnodes.md) collection that is associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="3f4d7-114">A nova coleção **IContextNodes** não faz parte da árvore de contexto do objeto **IInkAnalyzer** .</span><span class="sxs-lookup"><span data-stu-id="3f4d7-114">The new **IContextNodes** collection is not part of the **IInkAnalyzer** object's context tree.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f4d7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f4d7-115">Requirements</span></span>



| <span data-ttu-id="3f4d7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f4d7-116">Requirement</span></span> | <span data-ttu-id="3f4d7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3f4d7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f4d7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f4d7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3f4d7-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3f4d7-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3f4d7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f4d7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3f4d7-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3f4d7-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3f4d7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f4d7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f4d7-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3f4d7-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3f4d7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3f4d7-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f4d7-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f4d7-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3f4d7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f4d7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f4d7-127">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="3f4d7-127">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="3f4d7-128">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="3f4d7-128">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="3f4d7-129">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="3f4d7-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

