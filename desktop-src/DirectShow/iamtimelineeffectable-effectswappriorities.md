---
description: O método EffectSwapPriorities alterna os níveis de prioridade de dois efeitos.
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: 'Método IAMTimelineEffectable:: EffectSwapPriorities (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fb6a7dbee2d7f90da8f32e2a034e82df485f1ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792554"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a><span data-ttu-id="603f3-103">Método IAMTimelineEffectable:: EffectSwapPriorities</span><span class="sxs-lookup"><span data-stu-id="603f3-103">IAMTimelineEffectable::EffectSwapPriorities method</span></span>

> [!Note]  
> <span data-ttu-id="603f3-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="603f3-104">\[Deprecated.</span></span> <span data-ttu-id="603f3-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="603f3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="603f3-106">O `EffectSwapPriorities` método alterna os níveis de prioridade de dois efeitos.</span><span class="sxs-lookup"><span data-stu-id="603f3-106">The `EffectSwapPriorities` method switches the priority levels of two effects.</span></span>

<span data-ttu-id="603f3-107">Considerando dois valores de prioridade, esse método troca os efeitos nessas prioridades.</span><span class="sxs-lookup"><span data-stu-id="603f3-107">Given two priority values, this method swaps the effects at those priorities.</span></span> <span data-ttu-id="603f3-108">Quando o método retorna, o efeito que estava no primeiro nível de prioridade é no segundo nível de prioridade, e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="603f3-108">When the method returns, the effect that was at the first priority level is at the second priority level, and vice versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="603f3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="603f3-109">Syntax</span></span>


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a><span data-ttu-id="603f3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="603f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="603f3-111">*Prioridade*</span><span class="sxs-lookup"><span data-stu-id="603f3-111">*PriorityA*</span></span> 
</dt> <dd>

<span data-ttu-id="603f3-112">Primeiro nível de prioridade no qual alternar efeitos.</span><span class="sxs-lookup"><span data-stu-id="603f3-112">First priority level at which to swap effects.</span></span>

</dd> <dt>

<span data-ttu-id="603f3-113">*PriorityB*</span><span class="sxs-lookup"><span data-stu-id="603f3-113">*PriorityB*</span></span> 
</dt> <dd>

<span data-ttu-id="603f3-114">Segundo nível de prioridade no qual alternar efeitos.</span><span class="sxs-lookup"><span data-stu-id="603f3-114">Second priority level at which to swap effects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="603f3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="603f3-115">Return value</span></span>

<span data-ttu-id="603f3-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="603f3-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="603f3-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="603f3-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="603f3-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="603f3-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="603f3-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="603f3-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="603f3-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="603f3-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="603f3-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="603f3-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="603f3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="603f3-122">Requirements</span></span>



| <span data-ttu-id="603f3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="603f3-123">Requirement</span></span> | <span data-ttu-id="603f3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="603f3-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="603f3-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="603f3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="603f3-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="603f3-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="603f3-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="603f3-127">Library</span></span><br/> | <dl> <span data-ttu-id="603f3-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="603f3-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="603f3-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="603f3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="603f3-130">**Interface IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="603f3-130">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="603f3-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="603f3-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




