---
description: O método GetNextTrans recupera a primeira transição que aparece na hora especificada ou posteriormente.
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: 'Método IAMTimelineTransable:: GetNextTrans (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc8f7c88dab2b8c0dfece6f2799b6648c0b9da2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761755"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a><span data-ttu-id="d0e27-103">Método IAMTimelineTransable:: GetNextTrans</span><span class="sxs-lookup"><span data-stu-id="d0e27-103">IAMTimelineTransable::GetNextTrans method</span></span>

> [!Note]  
> <span data-ttu-id="d0e27-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d0e27-104">\[Deprecated.</span></span> <span data-ttu-id="d0e27-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0e27-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d0e27-106">O `GetNextTrans` método recupera a primeira transição que aparece na hora especificada ou posteriormente.</span><span class="sxs-lookup"><span data-stu-id="d0e27-106">The `GetNextTrans` method retrieves the first transition that appears at the specified time or later.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e27-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0e27-107">Syntax</span></span>


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="d0e27-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0e27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0e27-109">*ppTrans* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d0e27-109">*ppTrans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e27-110">Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto de transição.</span><span class="sxs-lookup"><span data-stu-id="d0e27-110">Receives a pointer to the transition object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d0e27-111">*Aquecimento*</span><span class="sxs-lookup"><span data-stu-id="d0e27-111">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="d0e27-112">Ponteiro para uma variável que especifica a hora em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="d0e27-112">Pointer to a variable that specifies the time in 100-nanosecond units.</span></span> <span data-ttu-id="d0e27-113">Na entrada, esse valor especifica a hora a partir da qual encontrar a transição.</span><span class="sxs-lookup"><span data-stu-id="d0e27-113">On input, this value specifies the time from which to find the transition.</span></span> <span data-ttu-id="d0e27-114">Na saída, se uma transição for recuperada, esse valor será definido como a hora de parada da transição.</span><span class="sxs-lookup"><span data-stu-id="d0e27-114">On output, if a transition is retrieved, this value is set to the stop time of the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0e27-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0e27-115">Return value</span></span>

<span data-ttu-id="d0e27-116">Retornará S \_ OK se o método recuperar uma transição ou S \_ false se não encontrar uma transição.</span><span class="sxs-lookup"><span data-stu-id="d0e27-116">Returns S\_OK if the method retrieves a transition, or S\_FALSE if it does not find a transition.</span></span> <span data-ttu-id="d0e27-117">Caso contrário, retorna um valor **HRESULT** que indica a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="d0e27-117">Otherwise, returns an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0e27-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0e27-118">Remarks</span></span>

<span data-ttu-id="d0e27-119">A hora de início da transição pode ser menor que a hora especificada em *pinagem*, se a transição abranger o tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="d0e27-119">The start time of the transition might be less than the time that you specify in *pInOut*, if the transition spans the specified time.</span></span>

<span data-ttu-id="d0e27-120">Se o método retornar S \_ OK, a interface [**IAMTimelineObj**](iamtimelineobj.md) que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="d0e27-120">If the method returns S\_OK, the [**IAMTimelineObj**](iamtimelineobj.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="d0e27-121">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="d0e27-121">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="d0e27-122">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="d0e27-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d0e27-123">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d0e27-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d0e27-124">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d0e27-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d0e27-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0e27-125">Requirements</span></span>



| <span data-ttu-id="d0e27-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0e27-126">Requirement</span></span> | <span data-ttu-id="d0e27-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d0e27-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e27-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0e27-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d0e27-129"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0e27-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d0e27-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0e27-130">Library</span></span><br/> | <dl> <span data-ttu-id="d0e27-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0e27-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0e27-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0e27-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0e27-133">**Interface IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="d0e27-133">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="d0e27-134">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="d0e27-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




