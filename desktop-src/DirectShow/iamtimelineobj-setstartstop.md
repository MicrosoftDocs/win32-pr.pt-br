---
description: O método SetStartStop define as horas de início e de parada do objeto, em relação ao pai do objeto.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: 'Método IAMTimelineObj:: SetStartStop (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7839417a0406fc2702fb0fbd593edc92fa80437
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760087"
---
# <a name="iamtimelineobjsetstartstop-method"></a><span data-ttu-id="12379-103">Método IAMTimelineObj:: SetStartStop</span><span class="sxs-lookup"><span data-stu-id="12379-103">IAMTimelineObj::SetStartStop method</span></span>

> [!Note]  
> <span data-ttu-id="12379-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="12379-104">\[Deprecated.</span></span> <span data-ttu-id="12379-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="12379-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="12379-106">O `SetStartStop` método define as horas de início e de parada do objeto, em relação ao pai do objeto.</span><span class="sxs-lookup"><span data-stu-id="12379-106">The `SetStartStop` method sets the object's start and stop times, relative to the object's parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="12379-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12379-107">Syntax</span></span>


```C++
HRESULT SetStartStop(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="12379-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12379-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12379-109">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="12379-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="12379-110">Nova hora de início, em unidades de 100 a nanossegundos ou – 1 para manter a hora de início existente.</span><span class="sxs-lookup"><span data-stu-id="12379-110">New start time, in 100-nanosecond units, or –1 to keep the existing start time.</span></span>

</dd> <dt>

<span data-ttu-id="12379-111">*Parar*</span><span class="sxs-lookup"><span data-stu-id="12379-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="12379-112">Nova hora de parada, em unidades de 100 a nanossegundos ou – 1 para manter a hora de parada existente.</span><span class="sxs-lookup"><span data-stu-id="12379-112">New stop time, in 100-nanosecond units, or –1 to keep the existing stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12379-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12379-113">Return value</span></span>

<span data-ttu-id="12379-114">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="12379-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="12379-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="12379-115">Return code</span></span>                                                                                  | <span data-ttu-id="12379-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="12379-116">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="12379-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="12379-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="12379-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="12379-118">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="12379-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="12379-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="12379-120">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="12379-120">Invalid argument.</span></span><br/> |
| <dl> <span data-ttu-id="12379-121"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="12379-121"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="12379-122">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="12379-122">Not implemented.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="12379-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="12379-123">Remarks</span></span>

<span data-ttu-id="12379-124">Faixas, composições e grupos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="12379-124">Tracks, compositions, and groups do not implement this method.</span></span> <span data-ttu-id="12379-125">Para esses objetos, a hora de início é sempre zero e a hora de parada é a hora de término máxima dos objetos que eles contêm.</span><span class="sxs-lookup"><span data-stu-id="12379-125">For these objects, the start time is always zero, and the stop time is the maximum stop time of the objects they contain.</span></span>

<span data-ttu-id="12379-126">Não defina os horários sobrepostos em objetos de origem dentro da mesma faixa. Isso pode causar comportamentos indefinidos.</span><span class="sxs-lookup"><span data-stu-id="12379-126">Do not set overlapping times on source objects within the same track. Doing so can cause undefined behaviors.</span></span>

<span data-ttu-id="12379-127">Para os objetos de origem, os horários de início e de parada são independentes das horas de início e de parada de mídia.</span><span class="sxs-lookup"><span data-stu-id="12379-127">For source objects, the start and stop times are independent of the media start and media stop times.</span></span> <span data-ttu-id="12379-128">A alteração de um par de valores não altera o outro.</span><span class="sxs-lookup"><span data-stu-id="12379-128">Changing one pair of values does not change the other.</span></span> <span data-ttu-id="12379-129">Para definir os horários de início e de parada da mídia, chame o método [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) .</span><span class="sxs-lookup"><span data-stu-id="12379-129">To set the media start and stop times, call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="12379-130">Para obter mais informações, consulte [tempo em serviços de edição do DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="12379-130">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="12379-131">Para obter cortes e transições com precisão de quadro, defina os parâmetros *Iniciar* e *parar* como limites de quadro.</span><span class="sxs-lookup"><span data-stu-id="12379-131">To get frame-accurate cuts and transitions, set the *Start* and *Stop* parameters to frame boundaries.</span></span> <span data-ttu-id="12379-132">Você pode usar o método [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) para converter um valor de hora no limite de quadro mais próximo ou usar a seguinte função para converter de número de quadro em tempo de referência:</span><span class="sxs-lookup"><span data-stu-id="12379-132">You can use the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method to convert a time value into the nearest frame boundary, or use the following function to convert from frame number to reference time:</span></span>


```C++
REFERENCE_TIME inline FrameNumToTime(LONGLONG frame, double fps)
{
    double dt = (frame * 10000000 / fps);
    if (frame >= 0) 
    {
        dt += 0.5;    }
    else
    {
        dt -= 0.5;
    }
    return (REFERENCE_TIME)dt;
}
```



> [!Note]  
> <span data-ttu-id="12379-133">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="12379-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="12379-134">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="12379-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="12379-135">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="12379-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="12379-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12379-136">Requirements</span></span>



| <span data-ttu-id="12379-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="12379-137">Requirement</span></span> | <span data-ttu-id="12379-138">Valor</span><span class="sxs-lookup"><span data-stu-id="12379-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12379-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12379-139">Header</span></span><br/>  | <dl> <span data-ttu-id="12379-140"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="12379-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="12379-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12379-141">Library</span></span><br/> | <dl> <span data-ttu-id="12379-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12379-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12379-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="12379-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12379-144">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="12379-144">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="12379-145">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="12379-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




