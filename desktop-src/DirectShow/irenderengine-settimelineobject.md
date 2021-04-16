---
description: O método settimelineobject define a linha do tempo para o mecanismo de renderização usar.
ms.assetid: 9b60b148-9768-43ba-a986-a96838c4d2bb
title: 'Método IRenderEngine:: settimelineobject (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 954fab15e92e6111439abb66d53d53525a5afdb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789639"
---
# <a name="irenderenginesettimelineobject-method"></a><span data-ttu-id="5d6fe-103">Método IRenderEngine:: settimelineobject</span><span class="sxs-lookup"><span data-stu-id="5d6fe-103">IRenderEngine::SetTimelineObject method</span></span>

> [!Note]  
> <span data-ttu-id="5d6fe-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-104">\[Deprecated.</span></span> <span data-ttu-id="5d6fe-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5d6fe-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5d6fe-106">O `SetTimelineObject` método define a linha do tempo para o mecanismo de renderização usar.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-106">The `SetTimelineObject` method sets the timeline for the render engine to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d6fe-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d6fe-107">Syntax</span></span>


```C++
HRESULT SetTimelineObject(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="5d6fe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d6fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d6fe-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="5d6fe-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="5d6fe-110">Ponteiro para a interface [**IAMTimeline**](iamtimeline.md) do objeto de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-110">Pointer to the timeline object's [**IAMTimeline**](iamtimeline.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d6fe-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d6fe-111">Return value</span></span>

<span data-ttu-id="5d6fe-112">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="5d6fe-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="5d6fe-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5d6fe-113">Return code</span></span>                                                                                            | <span data-ttu-id="5d6fe-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d6fe-114">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="5d6fe-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5d6fe-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="5d6fe-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-116">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="5d6fe-117"><dt>**E \_ deve \_ iniciar o \_ renderizador**</dt></span><span class="sxs-lookup"><span data-stu-id="5d6fe-117"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="5d6fe-118">Falha ao inicializar o mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-118">Render engine failed to initialize.</span></span><br/> |
| <dl> <span data-ttu-id="5d6fe-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5d6fe-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="5d6fe-120">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-120">Insufficient memory.</span></span><br/>                |
| <dl> <span data-ttu-id="5d6fe-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="5d6fe-121"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="5d6fe-122">Ponteiro inválido.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-122">Invalid pointer.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="5d6fe-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d6fe-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5d6fe-124">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5d6fe-125">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5d6fe-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5d6fe-126">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d6fe-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d6fe-127">Requirements</span></span>



| <span data-ttu-id="5d6fe-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d6fe-128">Requirement</span></span> | <span data-ttu-id="5d6fe-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5d6fe-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d6fe-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d6fe-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5d6fe-131"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d6fe-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5d6fe-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d6fe-132">Library</span></span><br/> | <dl> <span data-ttu-id="5d6fe-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d6fe-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d6fe-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d6fe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d6fe-135">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="5d6fe-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="5d6fe-136">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="5d6fe-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




