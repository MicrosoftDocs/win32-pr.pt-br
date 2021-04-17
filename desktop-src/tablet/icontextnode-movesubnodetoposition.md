---
description: Reordena um objeto IContextNode filho especificado para o índice especificado.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: 'Método IContextNode:: MoveSubNodeToPosition (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 398a56cf2c30c93a72e061dfe968de24276888f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763422"
---
# <a name="icontextnodemovesubnodetoposition-method"></a><span data-ttu-id="1fb92-103">Método IContextNode:: MoveSubNodeToPosition</span><span class="sxs-lookup"><span data-stu-id="1fb92-103">IContextNode::MoveSubNodeToPosition method</span></span>

<span data-ttu-id="1fb92-104">Reordena um objeto [**IContextNode**](icontextnode.md) filho especificado para o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="1fb92-104">Reorders a specified child [**IContextNode**](icontextnode.md) object to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb92-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fb92-105">Syntax</span></span>


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a><span data-ttu-id="1fb92-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fb92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fb92-107">*pSubnodeToMove* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fb92-107">*pSubnodeToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fb92-108">O objeto [**IContextNode**](icontextnode.md) a ser movido.</span><span class="sxs-lookup"><span data-stu-id="1fb92-108">The [**IContextNode**](icontextnode.md) object to move.</span></span>

</dd> <dt>

<span data-ttu-id="1fb92-109">*ulNewIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fb92-109">*ulNewIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fb92-110">O índice da nova posição do subnó.</span><span class="sxs-lookup"><span data-stu-id="1fb92-110">The index for the new position of the subnode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fb92-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1fb92-111">Return value</span></span>

<span data-ttu-id="1fb92-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1fb92-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1fb92-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fb92-113">Remarks</span></span>

<span data-ttu-id="1fb92-114">Retorna **E \_ INVALIDARG** se *pSubnodeToMove* não for um nó filho desse [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="1fb92-114">Returns **E\_INVALIDARG** if *pSubnodeToMove* is not a child node of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb92-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fb92-115">Requirements</span></span>



| <span data-ttu-id="1fb92-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fb92-116">Requirement</span></span> | <span data-ttu-id="1fb92-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1fb92-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb92-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fb92-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1fb92-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1fb92-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1fb92-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fb92-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1fb92-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1fb92-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1fb92-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fb92-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fb92-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1fb92-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1fb92-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1fb92-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fb92-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fb92-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1fb92-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fb92-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb92-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="1fb92-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="1fb92-128">**IContextNode::CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="1fb92-128">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="1fb92-129">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="1fb92-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




