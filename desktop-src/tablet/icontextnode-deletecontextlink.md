---
description: Exclui um objeto IContextLink da coleção de links do objeto IContextNode.
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: 'IContextNode: método eleteContextLink de:D (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac5676635bec961129078ed8689169d1a81cd87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787746"
---
# <a name="icontextnodedeletecontextlink-method"></a><span data-ttu-id="f695e-103">IContextNode: método eleteContextLink de:D</span><span class="sxs-lookup"><span data-stu-id="f695e-103">IContextNode::DeleteContextLink method</span></span>

<span data-ttu-id="f695e-104">Exclui um objeto [**IContextLink**](icontextlink.md) da coleção de links do objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="f695e-104">Deletes an [**IContextLink**](icontextlink.md) object from the [**IContextNode**](icontextnode.md) object's link collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f695e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f695e-105">Syntax</span></span>


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="f695e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f695e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f695e-107">*pContextLinkToDelete* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f695e-107">*pContextLinkToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f695e-108">O objeto [**IContextLink**](icontextlink.md) a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="f695e-108">The [**IContextLink**](icontextlink.md) object to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f695e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f695e-109">Return value</span></span>

<span data-ttu-id="f695e-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f695e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f695e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f695e-111">Remarks</span></span>

<span data-ttu-id="f695e-112">Um link de contexto tem um nó de origem e um nó de destino (consulte [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md) e [**IContextLink:: GetDestinationNode**](icontextlink-getdestinationnode.md)).</span><span class="sxs-lookup"><span data-stu-id="f695e-112">A context link has a source node and a destination node (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) and [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).</span></span> <span data-ttu-id="f695e-113">Esse método remove o [**IContextLink**](icontextlink.md) da coleção de links de contexto de ambos os nós de origem e de destino (consulte [**IContextNode:: GetContextLinks**](icontextnode-getcontextlinks.md)).</span><span class="sxs-lookup"><span data-stu-id="f695e-113">This method removes the [**IContextLink**](icontextlink.md) from both the source and destination nodes' collection of context links (see [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="f695e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f695e-114">Requirements</span></span>



| <span data-ttu-id="f695e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f695e-115">Requirement</span></span> | <span data-ttu-id="f695e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f695e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f695e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f695e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f695e-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f695e-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f695e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f695e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f695e-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f695e-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f695e-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f695e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f695e-122"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f695e-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f695e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f695e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f695e-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f695e-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f695e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f695e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f695e-126">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="f695e-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f695e-127">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="f695e-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="f695e-128">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="f695e-128">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="f695e-129">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="f695e-129">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="f695e-130">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="f695e-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




