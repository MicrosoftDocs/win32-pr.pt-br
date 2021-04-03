---
title: Método IMediaRendererFactory CreateMediaRendererFromBasicDeviceAsync
description: Cria de forma assíncrona uma nova instância de um objeto que implementa a interface IMediaRenderer usando a interface IBasicDevice especificada.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- API de streaming de mídia do método CreateMediaRendererFromBasicDeviceAsync
- API de streaming de mídia do método CreateMediaRendererFromBasicDeviceAsync, interface IMediaRendererFactory
- API de streaming de mídia da interface IMediaRendererFactory, método CreateMediaRendererFromBasicDeviceAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e4ee614cca9a03ca203ecde9203e019fab38ab4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007449"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a><span data-ttu-id="8fc23-106">Método IMediaRendererFactory:: CreateMediaRendererFromBasicDeviceAsync</span><span class="sxs-lookup"><span data-stu-id="8fc23-106">IMediaRendererFactory::CreateMediaRendererFromBasicDeviceAsync method</span></span>

<span data-ttu-id="8fc23-107">Cria de forma assíncrona uma nova instância de um objeto que implementa a interface [**IMediaRenderer**](imediarenderer.md) usando a interface [**IBasicDevice**](ibasicdevice.md) especificada.</span><span class="sxs-lookup"><span data-stu-id="8fc23-107">Asynchronously creates a new instance of an object that implements the [**IMediaRenderer**](imediarenderer.md) interface using the specified [**IBasicDevice**](ibasicdevice.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc23-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8fc23-108">Syntax</span></span>


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="8fc23-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fc23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc23-110">*basicDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8fc23-110">*basicDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc23-111">Um ponteiro para uma interface [**IBasicDevice**](ibasicdevice.md) que representa o dispositivo para o qual uma instância de [**IMediaRenderer**](imediarenderer.md) será criada.</span><span class="sxs-lookup"><span data-stu-id="8fc23-111">A pointer to an [**IBasicDevice**](ibasicdevice.md) interface representing the device for which an instance of [**IMediaRenderer**](imediarenderer.md) will be created.</span></span>

</dd> <dt>

<span data-ttu-id="8fc23-112">*valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8fc23-112">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc23-113">Recebe uma referência a um objeto [**CreateMediaRendererOperation**](createmediarendereroperation.md) que é usado para obter resultados da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8fc23-113">Receives a reference to a [**CreateMediaRendererOperation**](createmediarendereroperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fc23-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8fc23-114">Return value</span></span>

<span data-ttu-id="8fc23-115">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8fc23-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8fc23-116">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8fc23-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8fc23-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8fc23-117">Return code</span></span>                                                                          | <span data-ttu-id="8fc23-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="8fc23-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8fc23-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8fc23-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8fc23-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8fc23-120">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="8fc23-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fc23-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc23-122">**IMediaRendererFactory**</span><span class="sxs-lookup"><span data-stu-id="8fc23-122">**IMediaRendererFactory**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

