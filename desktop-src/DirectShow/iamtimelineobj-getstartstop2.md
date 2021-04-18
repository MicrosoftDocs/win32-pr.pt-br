---
description: 'O método GetStartStop2 recupera as horas de início e de parada do objeto, em relação ao pai do objeto. Esse método é equivalente a IAMTimelineObj:: GetStartStop, mas usa os valores de REFTIME.'
ms.assetid: 140842f5-3a24-4947-a360-ef97cba414ee
title: 'Método IAMTimelineObj:: GetStartStop2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 211bd54ee755a08d3e592a856c792eba6e3d4e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760088"
---
# <a name="iamtimelineobjgetstartstop2-method"></a><span data-ttu-id="be3fb-104">Método IAMTimelineObj:: GetStartStop2</span><span class="sxs-lookup"><span data-stu-id="be3fb-104">IAMTimelineObj::GetStartStop2 method</span></span>

> [!Note]  
> <span data-ttu-id="be3fb-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="be3fb-105">\[Deprecated.</span></span> <span data-ttu-id="be3fb-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="be3fb-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="be3fb-107">O `GetStartStop2` método recupera as horas de início e de parada do objeto, em relação ao pai do objeto.</span><span class="sxs-lookup"><span data-stu-id="be3fb-107">The `GetStartStop2` method retrieves the object's start and stop times, relative to the object's parent.</span></span> <span data-ttu-id="be3fb-108">Esse método é equivalente a [**IAMTimelineObj:: GetStartStop**](iamtimelineobj-getstartstop.md), mas usa os valores de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="be3fb-108">This method is equivalent to [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="be3fb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be3fb-109">Syntax</span></span>


```C++
HRESULT GetStartStop2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="be3fb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be3fb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be3fb-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="be3fb-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="be3fb-112">Recebe a hora de início, em segundos.</span><span class="sxs-lookup"><span data-stu-id="be3fb-112">Receives the start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="be3fb-113">*pStop*</span><span class="sxs-lookup"><span data-stu-id="be3fb-113">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="be3fb-114">Recebe a hora de parada, em segundos.</span><span class="sxs-lookup"><span data-stu-id="be3fb-114">Receives the stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be3fb-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be3fb-115">Return value</span></span>

<span data-ttu-id="be3fb-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="be3fb-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="be3fb-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="be3fb-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="be3fb-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="be3fb-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="be3fb-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="be3fb-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="be3fb-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="be3fb-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="be3fb-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="be3fb-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="be3fb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be3fb-122">Requirements</span></span>



| <span data-ttu-id="be3fb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="be3fb-123">Requirement</span></span> | <span data-ttu-id="be3fb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="be3fb-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be3fb-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be3fb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="be3fb-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="be3fb-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="be3fb-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be3fb-127">Library</span></span><br/> | <dl> <span data-ttu-id="be3fb-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be3fb-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be3fb-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="be3fb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be3fb-130">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="be3fb-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="be3fb-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="be3fb-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




