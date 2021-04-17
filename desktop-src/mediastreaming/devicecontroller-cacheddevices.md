---
title: Método DeviceController. CachedDevices
description: Recupera uma coleção de ponteiros de interface IBasicDevice que representa a exibição armazenada em cache de todos os dispositivos DLNA detectáveis. | Método DeviceController. CachedDevices
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- API de streaming de mídia do método CachedDevices
- API de streaming de mídia do método CachedDevices, interface DeviceController
- API de streaming de mídia da interface DeviceController, método CachedDevices
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0bb39e03a9788e0c444f682b61d39fc1c65781b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105785185"
---
# <a name="devicecontrollercacheddevices-method"></a><span data-ttu-id="d7333-107">Método DeviceController. CachedDevices</span><span class="sxs-lookup"><span data-stu-id="d7333-107">DeviceController.CachedDevices method</span></span>

<span data-ttu-id="d7333-108">Recupera uma coleção de ponteiros de interface [**IBasicDevice**](ibasicdevice.md) que representa a exibição armazenada em cache de todos os dispositivos DLNA detectáveis.</span><span class="sxs-lookup"><span data-stu-id="d7333-108">Retrieves a collection of [**IBasicDevice**](ibasicdevice.md) interface pointers that represents the cached view of all discoverable DLNA devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7333-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7333-109">Syntax</span></span>


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a><span data-ttu-id="d7333-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7333-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7333-111">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="d7333-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7333-112">Recebe uma coleção enumerável de ponteiros de interface [**IBasicDevice**](ibasicdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="d7333-112">Receives an enumerable collection of [**IBasicDevice**](ibasicdevice.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7333-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7333-113">Return value</span></span>

<span data-ttu-id="d7333-114">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d7333-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d7333-115">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d7333-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d7333-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d7333-116">Return code</span></span>                                                                          | <span data-ttu-id="d7333-117">Description</span><span class="sxs-lookup"><span data-stu-id="d7333-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d7333-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d7333-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d7333-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d7333-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d7333-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7333-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="d7333-121">[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7333-121">[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))</span></span>
</dt> </dl>

 

