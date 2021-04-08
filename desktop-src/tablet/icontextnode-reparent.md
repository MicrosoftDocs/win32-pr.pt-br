---
description: Move este objeto IContextNode da coleção de subnós do seu nó de contexto pai para a coleção de subnós do nó de contexto especificado.
ms.assetid: e19ecbe3-f7aa-499c-86a1-236dc9056fd9
title: 'Método IContextNode:: reparente (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Reparent
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 805b96b2a392a4f7b70aa4ce5913b48ffaf33551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010526"
---
# <a name="icontextnodereparent-method"></a><span data-ttu-id="4d2d6-103">Método IContextNode:: reparente</span><span class="sxs-lookup"><span data-stu-id="4d2d6-103">IContextNode::Reparent method</span></span>

<span data-ttu-id="4d2d6-104">Move este objeto [**IContextNode**](icontextnode.md) da coleção de subnós do seu nó de contexto pai para a coleção de subnós do nó de contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="4d2d6-104">Moves this [**IContextNode**](icontextnode.md) object from its parent context node's collection of subnodes to the specified context node's collection of subnodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d2d6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d2d6-105">Syntax</span></span>


```C++
HRESULT Reparent(
  [in] IContextNode *pNewParent
);
```



## <a name="parameters"></a><span data-ttu-id="4d2d6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d2d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d2d6-107">*pNewParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4d2d6-107">*pNewParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d2d6-108">O novo nó pai deste objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="4d2d6-108">The new parent node for this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d2d6-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d2d6-109">Return value</span></span>

<span data-ttu-id="4d2d6-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4d2d6-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d2d6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d2d6-111">Requirements</span></span>



| <span data-ttu-id="4d2d6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d2d6-112">Requirement</span></span> | <span data-ttu-id="4d2d6-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4d2d6-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d2d6-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d2d6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4d2d6-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4d2d6-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4d2d6-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d2d6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4d2d6-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4d2d6-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4d2d6-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4d2d6-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d2d6-119"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4d2d6-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4d2d6-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4d2d6-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d2d6-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d2d6-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4d2d6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d2d6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d2d6-123">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="4d2d6-123">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="4d2d6-124">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="4d2d6-124">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="4d2d6-125">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="4d2d6-125">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="4d2d6-126">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="4d2d6-126">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




