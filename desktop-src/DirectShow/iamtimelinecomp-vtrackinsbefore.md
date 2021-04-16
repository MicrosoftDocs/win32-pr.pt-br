---
description: O método VTrackInsBefore insere uma faixa virtual na composição na prioridade especificada.
ms.assetid: 82ae0867-13b6-41ae-adb9-a55ac78e21cb
title: 'Método IAMTimelineComp:: VTrackInsBefore (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ff5356591db6ccd20de720efd898387240075f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786976"
---
# <a name="iamtimelinecompvtrackinsbefore-method"></a><span data-ttu-id="1be00-103">Método IAMTimelineComp:: VTrackInsBefore</span><span class="sxs-lookup"><span data-stu-id="1be00-103">IAMTimelineComp::VTrackInsBefore method</span></span>

> [!Note]  
> <span data-ttu-id="1be00-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="1be00-104">\[Deprecated.</span></span> <span data-ttu-id="1be00-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1be00-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1be00-106">O `VTrackInsBefore` método insere uma faixa virtual na composição na prioridade especificada.</span><span class="sxs-lookup"><span data-stu-id="1be00-106">The `VTrackInsBefore` method inserts a virtual track into the composition at the specified priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="1be00-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1be00-107">Syntax</span></span>


```C++
HRESULT VTrackInsBefore(
   IAMTimelineObj *pVirtualTrack,
   long           Priority
);
```



## <a name="parameters"></a><span data-ttu-id="1be00-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1be00-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1be00-109">*pVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="1be00-109">*pVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="1be00-110">Ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) da faixa virtual.</span><span class="sxs-lookup"><span data-stu-id="1be00-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the virtual track.</span></span>

</dd> <dt>

<span data-ttu-id="1be00-111">*Prioridade*</span><span class="sxs-lookup"><span data-stu-id="1be00-111">*Priority*</span></span> 
</dt> <dd>

<span data-ttu-id="1be00-112">Prioridade na qual inserir a faixa virtual ou – 1 para inserir a faixa virtual no final da lista de prioridades.</span><span class="sxs-lookup"><span data-stu-id="1be00-112">Priority at which to insert the virtual track, or –1 to insert the virtual track at the end of the priority list.</span></span> <span data-ttu-id="1be00-113">A lista de prioridades determina quais clipes são visíveis.</span><span class="sxs-lookup"><span data-stu-id="1be00-113">The priority list determines which clips are visible.</span></span> <span data-ttu-id="1be00-114">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="1be00-114">See Remarks for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1be00-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1be00-115">Return value</span></span>

<span data-ttu-id="1be00-116">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="1be00-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="1be00-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1be00-117">Return code</span></span>                                                                                   | <span data-ttu-id="1be00-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="1be00-118">Description</span></span>                               |
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="1be00-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1be00-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1be00-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="1be00-120">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="1be00-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1be00-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1be00-122">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="1be00-122">Invalid argument.</span></span><br/>              |
| <dl> <span data-ttu-id="1be00-123"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="1be00-123"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="1be00-124">O objeto não é uma faixa virtual.</span><span class="sxs-lookup"><span data-stu-id="1be00-124">Object is not a virtual track.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1be00-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1be00-125">Remarks</span></span>

<span data-ttu-id="1be00-126">Cada faixa virtual em composição tem um nível de prioridade exclusivo.</span><span class="sxs-lookup"><span data-stu-id="1be00-126">Each virtual track in composition has a unique priority level.</span></span> <span data-ttu-id="1be00-127">Os níveis de prioridade variam de 0 a *n* -1, em que *n* é o número de faixas virtuais na composição.</span><span class="sxs-lookup"><span data-stu-id="1be00-127">Priority levels range from 0 to *n* - 1, where *n* is the number of virtual tracks in the composition.</span></span> <span data-ttu-id="1be00-128">Para grupos de vídeos, uma faixa virtual oculta todas as faixas virtuais com um nível de prioridade mais baixo, exceto em locais onde a faixa está vazia ou contém uma transição.</span><span class="sxs-lookup"><span data-stu-id="1be00-128">For video groups, a virtual track hides any virtual tracks with a lower priority level, except in places where the track is empty or contains a transition.</span></span> <span data-ttu-id="1be00-129">Você pode considerar as faixas virtuais como camadas na composição final.</span><span class="sxs-lookup"><span data-stu-id="1be00-129">You can think of virtual tracks as being layers in the final composition.</span></span> <span data-ttu-id="1be00-130">A faixa 1 está em camadas sobre o Track 0, o Track 2 é colocado em camadas na parte superior do Track 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="1be00-130">Track 1 is layered on top of track 0, track 2 is layered on top of track 1, and so forth.</span></span>

<span data-ttu-id="1be00-131">Se você especificar-1 para o parâmetro *Priority* , a faixa virtual será inserida no final da lista, com um valor de prioridade mais alto do que as faixas existentes.</span><span class="sxs-lookup"><span data-stu-id="1be00-131">If you specify -1 for the *Priority* parameter, the virtual track is inserted at the end of the list, with a higher priority value than the existing tracks.</span></span> <span data-ttu-id="1be00-132">Se você especificar um valor de prioridade que já existe na composição, cada faixa com uma prioridade igual ou maior moverá um nível de prioridade acima.</span><span class="sxs-lookup"><span data-stu-id="1be00-132">If you specify a priority value that already exists in the composition, every track with an equal or greater priority moves up one priority level.</span></span>

<span data-ttu-id="1be00-133">**Exemplo**: Track A tem prioridade 0 e Track B tem prioridade 1.</span><span class="sxs-lookup"><span data-stu-id="1be00-133">**Example**: Track A has priority 0, and track B has priority 1.</span></span> <span data-ttu-id="1be00-134">Se Track C for inserido na prioridade 0, Track a passa para a prioridade 1 e Track B passa para a prioridade 2.</span><span class="sxs-lookup"><span data-stu-id="1be00-134">If track C is inserted at priority 0, track A moves to priority 1, and track B moves to priority 2.</span></span>

<span data-ttu-id="1be00-135">Se a prioridade especificada for maior que o número atual de faixas na composição, o método falhará.</span><span class="sxs-lookup"><span data-stu-id="1be00-135">If the specified priority is greater than the current number of tracks in the composition, the method fails.</span></span>

> [!Note]  
> <span data-ttu-id="1be00-136">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="1be00-136">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1be00-137">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1be00-137">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1be00-138">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1be00-138">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1be00-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1be00-139">Requirements</span></span>



| <span data-ttu-id="1be00-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="1be00-140">Requirement</span></span> | <span data-ttu-id="1be00-141">Valor</span><span class="sxs-lookup"><span data-stu-id="1be00-141">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1be00-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1be00-142">Header</span></span><br/>  | <dl> <span data-ttu-id="1be00-143"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1be00-143"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1be00-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1be00-144">Library</span></span><br/> | <dl> <span data-ttu-id="1be00-145"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1be00-145"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1be00-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="1be00-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1be00-147">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="1be00-147">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="1be00-148">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="1be00-148">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




