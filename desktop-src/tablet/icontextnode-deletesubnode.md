---
description: Remove um IContextNode filho.
ms.assetid: ed1d7b35-f6ba-4eff-888d-5cc492f02832
title: 'IContextNode: método eleteSubNode de:D (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ffcec19e13a3ad885b3b497f80322caf9365c91a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501815"
---
# <a name="icontextnodedeletesubnode-method"></a><span data-ttu-id="4f342-103">IContextNode: método eleteSubNode de:D</span><span class="sxs-lookup"><span data-stu-id="4f342-103">IContextNode::DeleteSubNode method</span></span>

<span data-ttu-id="4f342-104">Remove um [**IContextNode**](icontextnode.md)filho.</span><span class="sxs-lookup"><span data-stu-id="4f342-104">Removes a child [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f342-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f342-105">Syntax</span></span>


```C++
HRESULT DeleteSubNode(
  [in] IContextNode *pContextNodeToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="4f342-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f342-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f342-107">*pContextNodeToDelete* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f342-107">*pContextNodeToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f342-108">O [**IContextNode**](icontextnode.md) a ser removido.</span><span class="sxs-lookup"><span data-stu-id="4f342-108">The [**IContextNode**](icontextnode.md) to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f342-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f342-109">Return value</span></span>

<span data-ttu-id="4f342-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4f342-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4f342-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f342-111">Remarks</span></span>

<span data-ttu-id="4f342-112">E \_ INVALIDARG será retornado se o parâmetro *pContextNodeToDelete* não for filho desse objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="4f342-112">E\_INVALIDARG is returned if the *pContextNodeToDelete* parameter is not a child of this [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f342-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f342-113">Requirements</span></span>



| <span data-ttu-id="4f342-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f342-114">Requirement</span></span> | <span data-ttu-id="4f342-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4f342-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f342-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f342-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4f342-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4f342-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4f342-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f342-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4f342-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4f342-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4f342-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f342-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f342-121"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4f342-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4f342-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4f342-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f342-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f342-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4f342-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f342-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f342-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="4f342-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="4f342-126">**IContextNode::CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="4f342-126">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="4f342-127">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="4f342-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




