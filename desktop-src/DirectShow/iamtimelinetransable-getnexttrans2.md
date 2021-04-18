---
description: 'O método GetNextTrans2 recupera a primeira transição que aparece na hora especificada ou posteriormente. Esse método é equivalente a IAMTimelineTransable:: GetNextTrans, mas usa um valor de REFTIME.'
ms.assetid: e6910e94-f289-4a5d-9976-1e8f7373c882
title: 'Método IAMTimelineTransable:: GetNextTrans2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c5f79ff20507247fbcac3badceaf2c3e28f0303
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759438"
---
# <a name="iamtimelinetransablegetnexttrans2-method"></a><span data-ttu-id="a06e0-104">Método IAMTimelineTransable:: GetNextTrans2</span><span class="sxs-lookup"><span data-stu-id="a06e0-104">IAMTimelineTransable::GetNextTrans2 method</span></span>

> [!Note]  
> <span data-ttu-id="a06e0-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="a06e0-105">\[Deprecated.</span></span> <span data-ttu-id="a06e0-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a06e0-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a06e0-107">O `GetNextTrans2` método recupera a primeira transição que aparece na hora especificada ou posteriormente.</span><span class="sxs-lookup"><span data-stu-id="a06e0-107">The `GetNextTrans2` method retrieves the first transition that appears at the specified time or later.</span></span> <span data-ttu-id="a06e0-108">Esse método é equivalente a [**IAMTimelineTransable:: GetNextTrans**](iamtimelinetransable-getnexttrans.md), mas usa um valor de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="a06e0-108">This method is equivalent to [**IAMTimelineTransable::GetNextTrans**](iamtimelinetransable-getnexttrans.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a06e0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a06e0-109">Syntax</span></span>


```C++
HRESULT GetNextTrans2(
  [out] IAMTimelineObj **ppTrans,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="a06e0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a06e0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a06e0-111">*ppTrans* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a06e0-111">*ppTrans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a06e0-112">Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto de transição.</span><span class="sxs-lookup"><span data-stu-id="a06e0-112">Receives a pointer to the transition object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a06e0-113">*Aquecimento*</span><span class="sxs-lookup"><span data-stu-id="a06e0-113">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="a06e0-114">Ponteiro para uma variável que especifica o tempo em segundos.</span><span class="sxs-lookup"><span data-stu-id="a06e0-114">Pointer to a variable that specifies the time in seconds.</span></span> <span data-ttu-id="a06e0-115">Na entrada, esse valor especifica a hora a partir da qual encontrar a transição.</span><span class="sxs-lookup"><span data-stu-id="a06e0-115">On input, this value specifies the time from which to find the transition.</span></span> <span data-ttu-id="a06e0-116">Na saída, se uma transição for recuperada, esse valor será definido como a hora de parada da transição.</span><span class="sxs-lookup"><span data-stu-id="a06e0-116">On output, if a transition is retrieved, this value is set to the stop time of the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a06e0-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a06e0-117">Return value</span></span>

<span data-ttu-id="a06e0-118">Retornará S \_ OK se o método recuperar uma transição ou S \_ false se não encontrar uma transição.</span><span class="sxs-lookup"><span data-stu-id="a06e0-118">Returns S\_OK if the method retrieves a transition, or S\_FALSE if it does not find a transition.</span></span> <span data-ttu-id="a06e0-119">Caso contrário, retorna um valor **HRESULT** que indica a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="a06e0-119">Otherwise, returns an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a06e0-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a06e0-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a06e0-121">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="a06e0-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a06e0-122">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a06e0-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a06e0-123">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a06e0-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a06e0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a06e0-124">Requirements</span></span>



| <span data-ttu-id="a06e0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a06e0-125">Requirement</span></span> | <span data-ttu-id="a06e0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a06e0-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a06e0-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a06e0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a06e0-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a06e0-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a06e0-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a06e0-129">Library</span></span><br/> | <dl> <span data-ttu-id="a06e0-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a06e0-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a06e0-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="a06e0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a06e0-132">**Interface IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="a06e0-132">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="a06e0-133">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="a06e0-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




