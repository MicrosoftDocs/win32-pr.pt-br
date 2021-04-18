---
description: Recupera uma coleção de objetos IContextLink que representa relações com outros objetos IContextNode.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: 'Método IContextNode:: GetContextLinks (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de62550a09d0a538ddc680f6d57c35a1016fe255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751802"
---
# <a name="icontextnodegetcontextlinks-method"></a><span data-ttu-id="812b4-103">Método IContextNode:: GetContextLinks</span><span class="sxs-lookup"><span data-stu-id="812b4-103">IContextNode::GetContextLinks method</span></span>

<span data-ttu-id="812b4-104">Recupera uma coleção de objetos [**IContextLink**](icontextlink.md) que representa relações com outros objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="812b4-104">Retrieves a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="812b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="812b4-105">Syntax</span></span>


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a><span data-ttu-id="812b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="812b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="812b4-107">*ppContextLinks* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="812b4-107">*ppContextLinks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="812b4-108">Um ponteiro para uma coleção de objetos [**IContextLink**](icontextlink.md) que representa relações com outros objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="812b4-108">A pointer to a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other [**IContextNode**](icontextnode.md) objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="812b4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="812b4-109">Return value</span></span>

<span data-ttu-id="812b4-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="812b4-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="812b4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="812b4-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="812b4-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppContextLinks* quando você não precisar mais usar a coleção de links de contexto.</span><span class="sxs-lookup"><span data-stu-id="812b4-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLinks* when you no longer need to use the context links collection.</span></span>

 

<span data-ttu-id="812b4-113">Para obter informações sobre relações de nó pai ou filho, use [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) ou [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md).</span><span class="sxs-lookup"><span data-stu-id="812b4-113">To get information about parent or child node relationships, use [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) or [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md).</span></span>

<span data-ttu-id="812b4-114">Para obter mais informações sobre os tipos de relações que são descritos por links, consulte [**IContextLink**](icontextlink.md) e [**ContextLinkDirection**](contextlinkdirection.md).</span><span class="sxs-lookup"><span data-stu-id="812b4-114">For more information about the kinds of relationships that are described by links, see [**IContextLink**](icontextlink.md) and [**ContextLinkDirection**](contextlinkdirection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="812b4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="812b4-115">Requirements</span></span>



| <span data-ttu-id="812b4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="812b4-116">Requirement</span></span> | <span data-ttu-id="812b4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="812b4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="812b4-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="812b4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="812b4-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="812b4-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="812b4-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="812b4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="812b4-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="812b4-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="812b4-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="812b4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="812b4-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="812b4-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="812b4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="812b4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="812b4-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="812b4-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="812b4-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="812b4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="812b4-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="812b4-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="812b4-128">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="812b4-128">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="812b4-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="812b4-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="812b4-130">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="812b4-130">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="812b4-131">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="812b4-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

