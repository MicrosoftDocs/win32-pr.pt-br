---
title: Método IDeviceController CachedDevices
description: Recupera uma coleção de ponteiros de interface IBasicDevice que representa a exibição armazenada em cache de todos os dispositivos DLNA detectáveis. | Método IDeviceController CachedDevices
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- API de streaming de mídia do método CachedDevices
- API de streaming de mídia do método CachedDevices, interface IDeviceController
- API de streaming de mídia da interface IDeviceController, método CachedDevices
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69be1faea277fa8999ae5ddf3658aaa61a1116b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930512"
---
# <a name="idevicecontrollercacheddevices-method"></a><span data-ttu-id="095a6-107">Método IDeviceController:: CachedDevices</span><span class="sxs-lookup"><span data-stu-id="095a6-107">IDeviceController::CachedDevices method</span></span>

<span data-ttu-id="095a6-108">Recupera uma coleção de ponteiros de interface [**IBasicDevice**](ibasicdevice.md) que representa a exibição armazenada em cache de todos os dispositivos DLNA detectáveis.</span><span class="sxs-lookup"><span data-stu-id="095a6-108">Retrieves a collection of [**IBasicDevice**](ibasicdevice.md) interface pointers that represents the cached view of all discoverable DLNA devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="095a6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="095a6-109">Syntax</span></span>


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a><span data-ttu-id="095a6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="095a6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="095a6-111">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="095a6-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="095a6-112">Recebe uma coleção enumerável de ponteiros de interface [**IBasicDevice**](ibasicdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="095a6-112">Receives an enumerable collection of [**IBasicDevice**](ibasicdevice.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="095a6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="095a6-113">Return value</span></span>

<span data-ttu-id="095a6-114">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="095a6-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="095a6-115">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="095a6-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="095a6-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="095a6-116">Return code</span></span>                                                                          | <span data-ttu-id="095a6-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="095a6-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="095a6-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="095a6-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="095a6-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="095a6-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="095a6-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="095a6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="095a6-121">**IDeviceController**</span><span class="sxs-lookup"><span data-stu-id="095a6-121">**IDeviceController**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

