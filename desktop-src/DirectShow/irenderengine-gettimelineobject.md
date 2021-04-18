---
description: O método gettimelineobject recupera a linha do tempo que o mecanismo de processamento está usando no momento.
ms.assetid: 74398f85-07b2-42fa-bb4f-a1e7e1669e3f
title: 'Método IRenderEngine:: gettimelineobject (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aab8e9a5f77affc464763b1c5a5045eaa4fc042a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779521"
---
# <a name="irenderenginegettimelineobject-method"></a><span data-ttu-id="4b96a-103">Método IRenderEngine:: gettimelineobject</span><span class="sxs-lookup"><span data-stu-id="4b96a-103">IRenderEngine::GetTimelineObject method</span></span>

> [!Note]  
> <span data-ttu-id="4b96a-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="4b96a-104">\[Deprecated.</span></span> <span data-ttu-id="4b96a-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4b96a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4b96a-106">O `GetTimelineObject` método recupera a linha do tempo que o mecanismo de processamento está usando no momento.</span><span class="sxs-lookup"><span data-stu-id="4b96a-106">The `GetTimelineObject` method retrieves the timeline that the render engine is currently using.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b96a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b96a-107">Syntax</span></span>


```C++
HRESULT GetTimelineObject(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="4b96a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b96a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b96a-109">*ppTimeline* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4b96a-109">*ppTimeline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b96a-110">Recebe um ponteiro para a interface [**IAMTimeline**](iamtimeline.md) da linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="4b96a-110">Receives a pointer to the timeline's [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="4b96a-111">Ele receberá o valor **NULL** se não houver linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="4b96a-111">It receives the value **NULL** if there is no timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b96a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b96a-112">Return value</span></span>

<span data-ttu-id="4b96a-113">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="4b96a-113">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="4b96a-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4b96a-114">Return code</span></span>                                                                                            | <span data-ttu-id="4b96a-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b96a-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="4b96a-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4b96a-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="4b96a-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="4b96a-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="4b96a-118"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="4b96a-118"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="4b96a-119">Ponteiro inválido.</span><span class="sxs-lookup"><span data-stu-id="4b96a-119">Invalid pointer.</span></span><br/>                    |
| <dl> <span data-ttu-id="4b96a-120"><dt>**E \_ deve \_ iniciar o \_ renderizador**</dt></span><span class="sxs-lookup"><span data-stu-id="4b96a-120"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="4b96a-121">Falha ao inicializar o mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="4b96a-121">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4b96a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b96a-122">Remarks</span></span>

<span data-ttu-id="4b96a-123">No retorno, se o valor de *\* ppTimeline* for não **nulo**, a interface **IAMTimeline** terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="4b96a-123">On return, if the value of *\*ppTimeline* is non-**NULL**, the **IAMTimeline** interface has an outstanding reference count.</span></span> <span data-ttu-id="4b96a-124">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="4b96a-124">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="4b96a-125">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="4b96a-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4b96a-126">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4b96a-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4b96a-127">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4b96a-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4b96a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b96a-128">Requirements</span></span>



| <span data-ttu-id="4b96a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b96a-129">Requirement</span></span> | <span data-ttu-id="4b96a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="4b96a-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b96a-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b96a-131">Header</span></span><br/>  | <dl> <span data-ttu-id="4b96a-132"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b96a-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4b96a-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b96a-133">Library</span></span><br/> | <dl> <span data-ttu-id="4b96a-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b96a-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b96a-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b96a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b96a-136">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="4b96a-136">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="4b96a-137">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="4b96a-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




