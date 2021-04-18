---
description: O método TransAdd adiciona uma transição para o objeto. Um objeto pode ter várias transições, mas eles não devem se sobrepor no tempo. As transições devem estar dentro dos limites de tempo do objeto.
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: 'Método IAMTimelineTransable:: TransAdd (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2636922549635c4a1c5e6e0b36f308f62328dc60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779843"
---
# <a name="iamtimelinetransabletransadd-method"></a><span data-ttu-id="c76fe-105">Método IAMTimelineTransable:: TransAdd</span><span class="sxs-lookup"><span data-stu-id="c76fe-105">IAMTimelineTransable::TransAdd method</span></span>

> [!Note]  
> <span data-ttu-id="c76fe-106">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="c76fe-106">\[Deprecated.</span></span> <span data-ttu-id="c76fe-107">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c76fe-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c76fe-108">O `TransAdd` método adiciona uma transição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c76fe-108">The `TransAdd` method adds a transition to the object.</span></span> <span data-ttu-id="c76fe-109">Um objeto pode ter várias transições, mas eles não devem se sobrepor no tempo.</span><span class="sxs-lookup"><span data-stu-id="c76fe-109">An object can have multiple transitions, but they must not overlap in time.</span></span> <span data-ttu-id="c76fe-110">As transições devem estar dentro dos limites de tempo do objeto.</span><span class="sxs-lookup"><span data-stu-id="c76fe-110">Transitions must fall within the time boundaries of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c76fe-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c76fe-111">Syntax</span></span>


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a><span data-ttu-id="c76fe-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c76fe-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c76fe-113">*pTrans*</span><span class="sxs-lookup"><span data-stu-id="c76fe-113">*pTrans*</span></span> 
</dt> <dd>

<span data-ttu-id="c76fe-114">Ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) da transição a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="c76fe-114">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the transition to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c76fe-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c76fe-115">Return value</span></span>

<span data-ttu-id="c76fe-116">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="c76fe-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="c76fe-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c76fe-117">Return code</span></span>                                                                                   | <span data-ttu-id="c76fe-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="c76fe-118">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="c76fe-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c76fe-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c76fe-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="c76fe-120">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c76fe-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c76fe-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c76fe-122">Não é possível inserir a transição.</span><span class="sxs-lookup"><span data-stu-id="c76fe-122">Cannot insert the transition.</span></span><br/>              |
| <dl> <span data-ttu-id="c76fe-123"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="c76fe-123"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="c76fe-124">*pTrans* não é um ponteiro para uma transição.</span><span class="sxs-lookup"><span data-stu-id="c76fe-124">*pTrans* is not a pointer to a transition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c76fe-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c76fe-125">Remarks</span></span>

<span data-ttu-id="c76fe-126">Se a transição sobrepor uma transição existente, o método retornará E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="c76fe-126">If the transition overlaps an existing transition, the method returns E\_INVALIDARG.</span></span>

> [!Note]  
> <span data-ttu-id="c76fe-127">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="c76fe-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c76fe-128">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c76fe-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c76fe-129">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c76fe-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c76fe-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c76fe-130">Requirements</span></span>



| <span data-ttu-id="c76fe-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c76fe-131">Requirement</span></span> | <span data-ttu-id="c76fe-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c76fe-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c76fe-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c76fe-133">Header</span></span><br/>  | <dl> <span data-ttu-id="c76fe-134"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c76fe-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c76fe-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c76fe-135">Library</span></span><br/> | <dl> <span data-ttu-id="c76fe-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c76fe-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c76fe-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="c76fe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c76fe-138">**Interface IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="c76fe-138">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="c76fe-139">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="c76fe-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




