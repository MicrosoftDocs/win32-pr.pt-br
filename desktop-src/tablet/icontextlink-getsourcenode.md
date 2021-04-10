---
description: Recupera o objeto IContextNode que é a origem para este IContextLink.
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: 'Método IContextLink:: GetSourceNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eddab21740bf30c67e247cec89723bc47cd9dca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164549"
---
# <a name="icontextlinkgetsourcenode-method"></a><span data-ttu-id="6e900-103">Método IContextLink:: GetSourceNode</span><span class="sxs-lookup"><span data-stu-id="6e900-103">IContextLink::GetSourceNode method</span></span>

<span data-ttu-id="6e900-104">Recupera o objeto [**IContextNode**](icontextnode.md) que é a origem para este [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="6e900-104">Retrieves the [**IContextNode**](icontextnode.md) object that is the source for this [**IContextLink**](icontextlink.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6e900-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e900-105">Syntax</span></span>


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a><span data-ttu-id="6e900-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e900-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e900-107">*ppSrcContextNodeId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6e900-107">*ppSrcContextNodeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e900-108">Um ponteiro para o objeto [**IContextNode**](icontextnode.md) que é a origem para esse [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="6e900-108">A pointer to the [**IContextNode**](icontextnode.md) object that is the source for this [**IContextLink**](icontextlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e900-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e900-109">Return value</span></span>

<span data-ttu-id="6e900-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6e900-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6e900-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e900-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="6e900-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppSrcContextNodeId* quando você não precisar mais usar o nó de origem.</span><span class="sxs-lookup"><span data-stu-id="6e900-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppSrcContextNodeId* when you no longer need to use the source node.</span></span>

 

<span data-ttu-id="6e900-113">Se o objeto [**IContextLink**](icontextlink.md) vincular-se entre um nó que contém a gravação e um nó que contém o desenho, o nó de origem será geralmente o nó que contém o desenho.</span><span class="sxs-lookup"><span data-stu-id="6e900-113">If the [**IContextLink**](icontextlink.md) object links between a node that contains writing and a node that contains drawing, the source node is generally the node that contains drawing.</span></span>

<span data-ttu-id="6e900-114">Se o objeto [**IContextLink**](icontextlink.md) tiver um tipo de link de incloses (consulte [**IContextLink:: GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), o nó de origem será o nó que inclui o nó de destino.</span><span class="sxs-lookup"><span data-stu-id="6e900-114">If the [**IContextLink**](icontextlink.md) object has a link type of Encloses (see [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), the source node is the node that encloses the destination node.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e900-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e900-115">Requirements</span></span>



| <span data-ttu-id="6e900-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e900-116">Requirement</span></span> | <span data-ttu-id="6e900-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6e900-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e900-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e900-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6e900-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6e900-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6e900-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e900-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6e900-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6e900-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6e900-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e900-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e900-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6e900-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6e900-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6e900-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e900-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e900-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6e900-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e900-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e900-127">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="6e900-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="6e900-128">**IContextLink::GetDestinationNode**</span><span class="sxs-lookup"><span data-stu-id="6e900-128">**IContextLink::GetDestinationNode**</span></span>](icontextlink-getdestinationnode.md)
</dt> <dt>

[<span data-ttu-id="6e900-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="6e900-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="6e900-130">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="6e900-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

