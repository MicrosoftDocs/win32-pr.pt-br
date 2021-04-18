---
description: O método ModifyStopTime define a hora de parada, em relação à linha do tempo.
ms.assetid: 0d9b6cf7-d029-4c35-9045-82cbeff1e3ae
title: 'Método IAMTimelineSrc:: ModifyStopTime (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5e0f3ac58df4e74926d2163705261ffad4551e69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786974"
---
# <a name="iamtimelinesrcmodifystoptime-method"></a><span data-ttu-id="7ff7f-103">Método IAMTimelineSrc:: ModifyStopTime</span><span class="sxs-lookup"><span data-stu-id="7ff7f-103">IAMTimelineSrc::ModifyStopTime method</span></span>

> [!Note]  
> <span data-ttu-id="7ff7f-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="7ff7f-104">\[Deprecated.</span></span> <span data-ttu-id="7ff7f-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7ff7f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7ff7f-106">O `ModifyStopTime` método define a hora de parada, em relação à linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="7ff7f-106">The `ModifyStopTime` method sets the stop time, relative to the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff7f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ff7f-107">Syntax</span></span>


```C++
HRESULT ModifyStopTime(
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="7ff7f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ff7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ff7f-109">*Parar*</span><span class="sxs-lookup"><span data-stu-id="7ff7f-109">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="7ff7f-110">Nova hora de parada, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="7ff7f-110">New stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ff7f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ff7f-111">Return value</span></span>

<span data-ttu-id="7ff7f-112">Retorna S \_ OK, ou E \_ INVALIDARG se a hora especificada não for válida.</span><span class="sxs-lookup"><span data-stu-id="7ff7f-112">Returns S\_OK, or E\_INVALIDARG if the specified time is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ff7f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ff7f-113">Remarks</span></span>

<span data-ttu-id="7ff7f-114">Esse método é equivalente a chamar [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) com a hora de início original e uma nova hora de parada.</span><span class="sxs-lookup"><span data-stu-id="7ff7f-114">This method is equivalent to calling [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) with the original start time and a new stop time.</span></span>

> [!Note]  
> <span data-ttu-id="7ff7f-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="7ff7f-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7ff7f-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ff7f-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7ff7f-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7ff7f-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ff7f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ff7f-118">Requirements</span></span>



| <span data-ttu-id="7ff7f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ff7f-119">Requirement</span></span> | <span data-ttu-id="7ff7f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7ff7f-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff7f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ff7f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7ff7f-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ff7f-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7ff7f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ff7f-123">Library</span></span><br/> | <dl> <span data-ttu-id="7ff7f-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ff7f-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ff7f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ff7f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff7f-126">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="7ff7f-126">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="7ff7f-127">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="7ff7f-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




