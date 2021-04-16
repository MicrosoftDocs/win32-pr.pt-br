---
description: O método FixTimes arredonda as horas de início e de término especificadas para os limites de quadro mais próximos, conforme definido pela configuração de taxa de quadros do grupo pai.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: 'Método IAMTimelineObj:: FixTimes (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3442d45328b10437111219ad36fc114a9aa15ad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758062"
---
# <a name="iamtimelineobjfixtimes-method"></a><span data-ttu-id="52208-103">Método IAMTimelineObj:: FixTimes</span><span class="sxs-lookup"><span data-stu-id="52208-103">IAMTimelineObj::FixTimes method</span></span>

> [!Note]  
> <span data-ttu-id="52208-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="52208-104">\[Deprecated.</span></span> <span data-ttu-id="52208-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="52208-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="52208-106">O `FixTimes` método arredonda as horas de início e de término especificadas para os limites de quadro mais próximos, conforme definido pela configuração de taxa de quadros do grupo pai.</span><span class="sxs-lookup"><span data-stu-id="52208-106">The `FixTimes` method rounds the specified start and stop times to the nearest frame boundaries, as defined by the parent group's frame rate setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="52208-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52208-107">Syntax</span></span>


```C++
HRESULT FixTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="52208-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52208-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52208-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="52208-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="52208-110">Ponteiro para uma variável que contém a hora de início, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="52208-110">Pointer to a variable that contains the start time, in 100-nanosecond units.</span></span> <span data-ttu-id="52208-111">Se a chamada for realizada com sucesso, essa variável será definida como o tempo arredondado.</span><span class="sxs-lookup"><span data-stu-id="52208-111">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="52208-112">*pStop*</span><span class="sxs-lookup"><span data-stu-id="52208-112">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="52208-113">Ponteiro para uma variável que contém a hora de parada, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="52208-113">Pointer to a variable that contains the stop time, in 100-nanosecond units.</span></span> <span data-ttu-id="52208-114">Se a chamada for realizada com sucesso, essa variável será definida como o tempo arredondado.</span><span class="sxs-lookup"><span data-stu-id="52208-114">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52208-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52208-115">Return value</span></span>

<span data-ttu-id="52208-116">Retornará S \_ OK se for bem-sucedido, ou E \_ NOTINTREE se o objeto não fizer parte de um grupo.</span><span class="sxs-lookup"><span data-stu-id="52208-116">Returns S\_OK if successful, or E\_NOTINTREE if the object is not part of a group.</span></span>

## <a name="remarks"></a><span data-ttu-id="52208-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="52208-117">Remarks</span></span>

<span data-ttu-id="52208-118">Durante a renderização, o DES arredonda as horas de início e de parada do objeto para o limite de quadro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="52208-118">During rendering, DES rounds the object's start and stop times to the nearest frame boundary.</span></span> <span data-ttu-id="52208-119">No entanto, o DES não substitui os horários do objeto.</span><span class="sxs-lookup"><span data-stu-id="52208-119">However, DES does not overwrite the object's times.</span></span> <span data-ttu-id="52208-120">Se você alterar a taxa de quadros do grupo, os horários arredondados serão sempre calculados a partir dos horários originais.</span><span class="sxs-lookup"><span data-stu-id="52208-120">If you change the group frame rate, the rounded times are always calculated from the original times.</span></span> <span data-ttu-id="52208-121">Para obter mais informações, consulte [tempo em serviços de edição do DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="52208-121">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="52208-122">Use esse método para determinar os horários de início e de parada precisos no projeto renderizado.</span><span class="sxs-lookup"><span data-stu-id="52208-122">Use this method to determine accurate start and stop times in the rendered project.</span></span> <span data-ttu-id="52208-123">Por exemplo, você deve procurar os horários arredondados, em vez de os horários de início e de término originais do objeto.</span><span class="sxs-lookup"><span data-stu-id="52208-123">For example, you should seek to the rounded times, rather than the object's original start and stop times.</span></span> <span data-ttu-id="52208-124">Chame [**IAMTimelineObj:: GetStartStop**](iamtimelineobj-getstartstop.md) para obter os horários originais e passe esses valores para `FixTimes` .</span><span class="sxs-lookup"><span data-stu-id="52208-124">Call [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md) to obtain the original times, and pass those values to `FixTimes`.</span></span>

> [!Note]  
> <span data-ttu-id="52208-125">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="52208-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="52208-126">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="52208-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="52208-127">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="52208-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52208-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52208-128">Requirements</span></span>



| <span data-ttu-id="52208-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="52208-129">Requirement</span></span> | <span data-ttu-id="52208-130">Valor</span><span class="sxs-lookup"><span data-stu-id="52208-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52208-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52208-131">Header</span></span><br/>  | <dl> <span data-ttu-id="52208-132"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="52208-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="52208-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52208-133">Library</span></span><br/> | <dl> <span data-ttu-id="52208-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52208-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52208-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="52208-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52208-136">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="52208-136">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="52208-137">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="52208-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




