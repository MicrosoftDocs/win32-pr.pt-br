---
description: Adiciona um novo IContextLink à coleção de links de contexto do objeto IContextNode.
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: 'Método IContextNode:: AddContextLink (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eccfcc8be51ff951c1bcd6de55bd3a0f89cdc201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748944"
---
# <a name="icontextnodeaddcontextlink-method"></a><span data-ttu-id="eec04-103">Método IContextNode:: AddContextLink</span><span class="sxs-lookup"><span data-stu-id="eec04-103">IContextNode::AddContextLink method</span></span>

<span data-ttu-id="eec04-104">Adiciona um novo [**IContextLink**](icontextlink.md) à coleção de links de contexto do objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="eec04-104">Adds a new [**IContextLink**](icontextlink.md) to the [**IContextNode**](icontextnode.md) object's collection of context links.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec04-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eec04-105">Syntax</span></span>


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a><span data-ttu-id="eec04-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eec04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec04-107">*pDestinationNode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eec04-107">*pDestinationNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec04-108">O [**IContextNode**](icontextnode.md) de destino para o novo [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="eec04-108">The destination [**IContextNode**](icontextnode.md) for the new [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="eec04-109">*linkDirection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eec04-109">*linkDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec04-110">A direção do objeto [**IContextLink**](icontextlink.md) a ser criado.</span><span class="sxs-lookup"><span data-stu-id="eec04-110">The direction of [**IContextLink**](icontextlink.md) object to create.</span></span>

</dd> <dt>

<span data-ttu-id="eec04-111">*ppContextLinkToAdd* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="eec04-111">*ppContextLinkToAdd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eec04-112">Um ponteiro para o novo objeto [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="eec04-112">A pointer to the new [**IContextLink**](icontextlink.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eec04-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eec04-113">Return value</span></span>

<span data-ttu-id="eec04-114">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="eec04-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eec04-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="eec04-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="eec04-116">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppContextLinkToAdd* quando você não precisar mais usar o nó de contexto.</span><span class="sxs-lookup"><span data-stu-id="eec04-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLinkToAdd* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="eec04-117">Esse objeto [**IContextNode**](icontextnode.md) é o nó de origem (consulte [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md)) para o novo objeto [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="eec04-117">This [**IContextNode**](icontextnode.md) object is the source node (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)) for the new [**IContextLink**](icontextlink.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="eec04-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eec04-118">Requirements</span></span>



| <span data-ttu-id="eec04-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="eec04-119">Requirement</span></span> | <span data-ttu-id="eec04-120">Valor</span><span class="sxs-lookup"><span data-stu-id="eec04-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eec04-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eec04-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eec04-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="eec04-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eec04-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eec04-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eec04-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="eec04-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="eec04-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eec04-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="eec04-126"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="eec04-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="eec04-127">DLL</span><span class="sxs-lookup"><span data-stu-id="eec04-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eec04-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eec04-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="eec04-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="eec04-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec04-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="eec04-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="eec04-131">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="eec04-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="eec04-132">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="eec04-132">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="eec04-133">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="eec04-133">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="eec04-134">**IContextNode::D eleteContextLink**</span><span class="sxs-lookup"><span data-stu-id="eec04-134">**IContextNode::DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)
</dt> <dt>

[<span data-ttu-id="eec04-135">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="eec04-135">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="eec04-136">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="eec04-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

