---
description: O método GetStartStop recupera as horas de início e de parada do objeto, em relação ao pai do objeto.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: 'Método IAMTimelineObj:: GetStartStop (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aa4204f2bd41d72a6d3ef67f633f8b64a58051b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792553"
---
# <a name="iamtimelineobjgetstartstop-method"></a><span data-ttu-id="ad741-103">Método IAMTimelineObj:: GetStartStop</span><span class="sxs-lookup"><span data-stu-id="ad741-103">IAMTimelineObj::GetStartStop method</span></span>

> [!Note]  
> <span data-ttu-id="ad741-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="ad741-104">\[Deprecated.</span></span> <span data-ttu-id="ad741-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ad741-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ad741-106">O `GetStartStop` método recupera as horas de início e de parada do objeto, em relação ao pai do objeto.</span><span class="sxs-lookup"><span data-stu-id="ad741-106">The `GetStartStop` method retrieves the object's start and stop times, relative to the object's parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad741-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad741-107">Syntax</span></span>


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="ad741-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad741-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad741-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="ad741-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="ad741-110">Recebe a hora de início, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="ad741-110">Receives the start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="ad741-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="ad741-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="ad741-112">Recebe a hora de parada, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="ad741-112">Receives the stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad741-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad741-113">Return value</span></span>

<span data-ttu-id="ad741-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ad741-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ad741-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ad741-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad741-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad741-116">Remarks</span></span>

<span data-ttu-id="ad741-117">Composições, grupos e faixas sempre têm uma hora de início de 0.</span><span class="sxs-lookup"><span data-stu-id="ad741-117">Compositions, groups, and tracks always have a start time of 0.</span></span>

<span data-ttu-id="ad741-118">Durante a renderização, o DES arredonda os horários de início e de parada de um objeto para o limite de quadro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="ad741-118">During rendering, DES rounds an object's start and stop times to the nearest frame boundary.</span></span> <span data-ttu-id="ad741-119">No entanto, o DES não substitui os horários do objeto.</span><span class="sxs-lookup"><span data-stu-id="ad741-119">However, DES does not overwrite the object's times.</span></span> <span data-ttu-id="ad741-120">Se você alterar a taxa de quadros do grupo, os horários arredondados serão sempre calculados a partir dos horários originais.</span><span class="sxs-lookup"><span data-stu-id="ad741-120">If you change the group frame rate, the rounded times are always calculated from the original times.</span></span> <span data-ttu-id="ad741-121">Para obter mais informações, [tempo em serviços de edição do DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="ad741-121">For more information, [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="ad741-122">Para determinar os horários de início e de parada no projeto renderizado, passe os valores retornados por `GetStartStop` para o método [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) .</span><span class="sxs-lookup"><span data-stu-id="ad741-122">To determine the start and stop times in the rendered project, pass the values returned by `GetStartStop` to the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="ad741-123">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="ad741-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ad741-124">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ad741-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ad741-125">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ad741-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ad741-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad741-126">Requirements</span></span>



| <span data-ttu-id="ad741-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad741-127">Requirement</span></span> | <span data-ttu-id="ad741-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ad741-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad741-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad741-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ad741-130"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad741-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ad741-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad741-131">Library</span></span><br/> | <dl> <span data-ttu-id="ad741-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad741-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad741-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad741-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad741-134">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="ad741-134">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="ad741-135">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="ad741-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




