---
title: Método IMediaRendererFactory CreateMediaRendererAsync
description: Cria de forma assíncrona uma nova instância de um objeto que implementa a interface IMediaRenderer usando o nome de dispositivo exclusivo especificado (UDN).
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- API de streaming de mídia do método CreateMediaRendererAsync
- API de streaming de mídia do método CreateMediaRendererAsync, interface IMediaRendererFactory
- API de streaming de mídia da interface IMediaRendererFactory, método CreateMediaRendererAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b152e5889ad83440a48e178be0b89a97d2a9f664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640745"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a><span data-ttu-id="eced9-106">Método IMediaRendererFactory:: CreateMediaRendererAsync</span><span class="sxs-lookup"><span data-stu-id="eced9-106">IMediaRendererFactory::CreateMediaRendererAsync method</span></span>

<span data-ttu-id="eced9-107">Cria de forma assíncrona uma nova instância de um objeto que implementa a interface [**IMediaRenderer**](imediarenderer.md) usando o nome de dispositivo exclusivo especificado (UDN).</span><span class="sxs-lookup"><span data-stu-id="eced9-107">Asynchronously creates a new instance of an object that implements the [**IMediaRenderer**](imediarenderer.md) interface using the specified Unique Device Name (UDN).</span></span>

## <a name="syntax"></a><span data-ttu-id="eced9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eced9-108">Syntax</span></span>


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="eced9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eced9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eced9-110">*deviceIdentifier* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eced9-110">*deviceIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eced9-111">Um HSTRING que contém um UDN que identifica o dispositivo DMR DLNA para o qual uma instância de [**IMediaRenderer**](imediarenderer.md) será criada.</span><span class="sxs-lookup"><span data-stu-id="eced9-111">An HSTRING containing a UDN that identifies the DLNA DMR device for which an instance of [**IMediaRenderer**](imediarenderer.md) will be created.</span></span>

</dd> <dt>

<span data-ttu-id="eced9-112">*valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="eced9-112">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="eced9-113">Recebe uma referência a um objeto [**CreateMediaRendererOperation**](createmediarendereroperation.md) que é usado para obter resultados da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="eced9-113">Receives a reference to a [**CreateMediaRendererOperation**](createmediarendereroperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eced9-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eced9-114">Return value</span></span>

<span data-ttu-id="eced9-115">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="eced9-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="eced9-116">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="eced9-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="eced9-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="eced9-117">Return code</span></span>                                                                          | <span data-ttu-id="eced9-118">Description</span><span class="sxs-lookup"><span data-stu-id="eced9-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="eced9-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eced9-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="eced9-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="eced9-120">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="eced9-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="eced9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eced9-122">**IMediaRendererFactory**</span><span class="sxs-lookup"><span data-stu-id="eced9-122">**IMediaRendererFactory**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

