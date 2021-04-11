---
description: Recupera o objeto IContextNode que é o destino para este IContextLink.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: 'Método IContextLink:: GetDestinationNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 86d34bfcca39f7df9d9010e8dae32747ca8f1d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296394"
---
# <a name="icontextlinkgetdestinationnode-method"></a><span data-ttu-id="dec0c-103">Método IContextLink:: GetDestinationNode</span><span class="sxs-lookup"><span data-stu-id="dec0c-103">IContextLink::GetDestinationNode method</span></span>

<span data-ttu-id="dec0c-104">Recupera o objeto [**IContextNode**](icontextnode.md) que é o destino para este [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="dec0c-104">Retrieves the [**IContextNode**](icontextnode.md) object that is the destination for this [**IContextLink**](icontextlink.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dec0c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dec0c-105">Syntax</span></span>


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a><span data-ttu-id="dec0c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dec0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dec0c-107">*ppDstContextNodeId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dec0c-107">*ppDstContextNodeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dec0c-108">Um ponteiro para o objeto [**IContextNode**](icontextnode.md) que é o destino para esse [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="dec0c-108">A pointer to the [**IContextNode**](icontextnode.md) object that is the destination for this [**IContextLink**](icontextlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dec0c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dec0c-109">Return value</span></span>

<span data-ttu-id="dec0c-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="dec0c-110">For a description of return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dec0c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dec0c-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="dec0c-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppDstContextNodeId* quando você não precisar mais usar o nó de destino.</span><span class="sxs-lookup"><span data-stu-id="dec0c-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppDstContextNodeId* when you no longer need to use the destination node.</span></span>

 

<span data-ttu-id="dec0c-113">Se o objeto [**IContextLink**](icontextlink.md) vincular-se entre um nó que contém a gravação e um nó que contém o desenho, o nó de destino será geralmente o nó que contém a gravação.</span><span class="sxs-lookup"><span data-stu-id="dec0c-113">If the [**IContextLink**](icontextlink.md) object links between a node that contains writing and a node that contains drawing, the destination node is generally the node that contains writing.</span></span>

<span data-ttu-id="dec0c-114">Se o objeto [**IContextLink**](icontextlink.md) tiver um tipo de link de delimitados (consulte [**IContextLink:: GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), o nó de destino será o objeto [**IContextNode**](icontextnode.md) que está incluído.</span><span class="sxs-lookup"><span data-stu-id="dec0c-114">If the [**IContextLink**](icontextlink.md) object has a link type of Encloses (see [**IContextLink::GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), the destination node is the [**IContextNode**](icontextnode.md) object that is enclosed.</span></span>

## <a name="requirements"></a><span data-ttu-id="dec0c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dec0c-115">Requirements</span></span>



| <span data-ttu-id="dec0c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dec0c-116">Requirement</span></span> | <span data-ttu-id="dec0c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dec0c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec0c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dec0c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dec0c-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dec0c-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dec0c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dec0c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dec0c-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dec0c-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="dec0c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dec0c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dec0c-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dec0c-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dec0c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="dec0c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dec0c-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dec0c-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="dec0c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="dec0c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec0c-127">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="dec0c-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="dec0c-128">**IContextLink::GetSourceNode**</span><span class="sxs-lookup"><span data-stu-id="dec0c-128">**IContextLink::GetSourceNode**</span></span>](icontextlink-getsourcenode.md)
</dt> <dt>

[<span data-ttu-id="dec0c-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="dec0c-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="dec0c-130">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="dec0c-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

