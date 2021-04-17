---
description: Remove um objeto IContextNode desta coleção.
ms.assetid: ddda506d-4e39-486d-ac7d-211dc7869a73
title: 'Método IContextNodes:: RemoveContextNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.RemoveContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 371722cca3d8ccc132c151b37e9d1a469bdb0c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762500"
---
# <a name="icontextnodesremovecontextnode-method"></a><span data-ttu-id="82f6e-103">Método IContextNodes:: RemoveContextNode</span><span class="sxs-lookup"><span data-stu-id="82f6e-103">IContextNodes::RemoveContextNode method</span></span>

<span data-ttu-id="82f6e-104">Remove um objeto [**IContextNode**](icontextnode.md) desta coleção.</span><span class="sxs-lookup"><span data-stu-id="82f6e-104">Removes an [**IContextNode**](icontextnode.md) object from this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="82f6e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82f6e-105">Syntax</span></span>


```C++
HRESULT RemoveContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="82f6e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82f6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82f6e-107">*pContextNode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82f6e-107">*pContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f6e-108">O objeto [**IContextNode**](icontextnode.md) a ser removido.</span><span class="sxs-lookup"><span data-stu-id="82f6e-108">The [**IContextNode**](icontextnode.md) object to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82f6e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82f6e-109">Return value</span></span>

<span data-ttu-id="82f6e-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="82f6e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82f6e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82f6e-111">Requirements</span></span>



| <span data-ttu-id="82f6e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="82f6e-112">Requirement</span></span> | <span data-ttu-id="82f6e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="82f6e-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82f6e-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82f6e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="82f6e-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="82f6e-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="82f6e-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82f6e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="82f6e-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="82f6e-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="82f6e-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82f6e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="82f6e-119"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="82f6e-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="82f6e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="82f6e-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82f6e-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82f6e-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="82f6e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="82f6e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82f6e-123">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="82f6e-123">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="82f6e-124">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="82f6e-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




