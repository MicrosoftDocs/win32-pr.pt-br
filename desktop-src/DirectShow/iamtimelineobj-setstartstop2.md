---
description: 'O método SetStartStop2 define as horas de início e de parada do objeto, em relação ao pai do objeto. Esse método é equivalente a IAMTimelineObj:: SetStartStop, mas usa os valores de REFTIME.'
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: 'Método IAMTimelineObj:: SetStartStop2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 190e47d2ccee00d202dc16e20704b545447d844f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784026"
---
# <a name="iamtimelineobjsetstartstop2-method"></a><span data-ttu-id="b99a6-104">Método IAMTimelineObj:: SetStartStop2</span><span class="sxs-lookup"><span data-stu-id="b99a6-104">IAMTimelineObj::SetStartStop2 method</span></span>

> [!Note]  
> <span data-ttu-id="b99a6-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="b99a6-105">\[Deprecated.</span></span> <span data-ttu-id="b99a6-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b99a6-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b99a6-107">O `SetStartStop2` método define as horas de início e de parada do objeto, em relação ao pai do objeto.</span><span class="sxs-lookup"><span data-stu-id="b99a6-107">The `SetStartStop2` method sets the object's start and stop times, relative to the object's parent.</span></span> <span data-ttu-id="b99a6-108">Esse método é equivalente a [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md), mas usa os valores de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="b99a6-108">This method is equivalent to [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b99a6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b99a6-109">Syntax</span></span>


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="b99a6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b99a6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b99a6-111">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="b99a6-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="b99a6-112">Nova hora de início, em segundos ou – 1 para manter a hora de início existente.</span><span class="sxs-lookup"><span data-stu-id="b99a6-112">New start time, in seconds, or –1 to keep the existing start time.</span></span>

</dd> <dt>

<span data-ttu-id="b99a6-113">*Parar*</span><span class="sxs-lookup"><span data-stu-id="b99a6-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="b99a6-114">Nova hora de parada, em segundos ou – 1 para manter a hora de parada existente.</span><span class="sxs-lookup"><span data-stu-id="b99a6-114">New stop time, in seconds, or –1 to keep the existing stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b99a6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b99a6-115">Return value</span></span>

<span data-ttu-id="b99a6-116">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="b99a6-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="b99a6-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b99a6-117">Return code</span></span>                                                                                  | <span data-ttu-id="b99a6-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="b99a6-118">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="b99a6-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b99a6-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b99a6-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="b99a6-120">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="b99a6-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b99a6-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="b99a6-122">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="b99a6-122">Invalid argument.</span></span><br/> |
| <dl> <span data-ttu-id="b99a6-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="b99a6-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="b99a6-124">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="b99a6-124">Not implemented.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="b99a6-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b99a6-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b99a6-126">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="b99a6-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b99a6-127">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b99a6-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b99a6-128">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b99a6-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b99a6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b99a6-129">Requirements</span></span>



| <span data-ttu-id="b99a6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b99a6-130">Requirement</span></span> | <span data-ttu-id="b99a6-131">Valor</span><span class="sxs-lookup"><span data-stu-id="b99a6-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b99a6-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b99a6-132">Header</span></span><br/>  | <dl> <span data-ttu-id="b99a6-133"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b99a6-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b99a6-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b99a6-134">Library</span></span><br/> | <dl> <span data-ttu-id="b99a6-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b99a6-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b99a6-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="b99a6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b99a6-137">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="b99a6-137">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="b99a6-138">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="b99a6-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




