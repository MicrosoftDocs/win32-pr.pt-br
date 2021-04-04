---
description: Recupera o identificador de traço para o traço referenciado por um valor de índice dentro do objeto IContextNode.
ms.assetid: faac142e-cac1-45f9-9b40-76c50ac7006b
title: 'Método IContextNode:: getstrokeid (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b193b3719ac6b67284e3ff8c4297455888f6c9cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647235"
---
# <a name="icontextnodegetstrokeid-method"></a><span data-ttu-id="971bf-103">Método IContextNode:: getstrokeid</span><span class="sxs-lookup"><span data-stu-id="971bf-103">IContextNode::GetStrokeId method</span></span>

<span data-ttu-id="971bf-104">Recupera o identificador de traço para o traço referenciado por um valor de índice dentro do objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="971bf-104">Retrieves the stroke identifier for the stroke referenced by an index value within the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="971bf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="971bf-105">Syntax</span></span>


```C++
HRESULT GetStrokeId(
  [in]  ULONG ulIndex,
  [out] LONG  *plStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="971bf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="971bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="971bf-107">*ulIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="971bf-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="971bf-108">O índice do traço a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="971bf-108">The index of the stroke to be returned.</span></span>

</dd> <dt>

<span data-ttu-id="971bf-109">*plStrokeId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="971bf-109">*plStrokeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="971bf-110">O identificador de traço para o traço referenciado pelo parâmetro *ulIndex* no objeto [**IContextNode**](icontextnode.md) atual.</span><span class="sxs-lookup"><span data-stu-id="971bf-110">The stroke identifier for the stroke referenced by the *ulIndex* parameter within the current [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="971bf-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="971bf-111">Return value</span></span>

<span data-ttu-id="971bf-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="971bf-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="971bf-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="971bf-113">Requirements</span></span>



| <span data-ttu-id="971bf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="971bf-114">Requirement</span></span> | <span data-ttu-id="971bf-115">Valor</span><span class="sxs-lookup"><span data-stu-id="971bf-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="971bf-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="971bf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="971bf-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="971bf-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="971bf-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="971bf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="971bf-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="971bf-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="971bf-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="971bf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="971bf-121"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="971bf-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="971bf-122">DLL</span><span class="sxs-lookup"><span data-stu-id="971bf-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="971bf-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="971bf-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="971bf-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="971bf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="971bf-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="971bf-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="971bf-126">**IContextNode::GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="971bf-126">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="971bf-127">**IContextNode::GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="971bf-127">**IContextNode::GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)
</dt> <dt>

[<span data-ttu-id="971bf-128">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="971bf-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




