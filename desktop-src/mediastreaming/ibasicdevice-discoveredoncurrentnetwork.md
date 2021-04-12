---
title: Método IBasicDevice DiscoveredOnCurrentNetwork
description: Recupera um valor que indica se o dispositivo está na rede atual.
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- API de streaming de mídia do método DiscoveredOnCurrentNetwork
- API de streaming de mídia do método DiscoveredOnCurrentNetwork, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método DiscoveredOnCurrentNetwork
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e79a012413b3b3d78a9c4617f01ca6cc01cf7e1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364738"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a><span data-ttu-id="797b7-106">IBasicDevice: método iscoveredOnCurrentNetwork de:D</span><span class="sxs-lookup"><span data-stu-id="797b7-106">IBasicDevice::DiscoveredOnCurrentNetwork method</span></span>

<span data-ttu-id="797b7-107">Recupera um valor que indica se o dispositivo está na rede atual.</span><span class="sxs-lookup"><span data-stu-id="797b7-107">Retrieves a value that indicates if the device is on the current network.</span></span>

## <a name="syntax"></a><span data-ttu-id="797b7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="797b7-108">Syntax</span></span>


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="797b7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="797b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="797b7-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="797b7-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="797b7-111">Recebe um ponteiro para um valor booliano que é **verdadeiro** se o dispositivo estiver na rede atual.</span><span class="sxs-lookup"><span data-stu-id="797b7-111">Receives a pointer to a boolean value that is **True** if the device is on the current network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="797b7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="797b7-112">Return value</span></span>

<span data-ttu-id="797b7-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="797b7-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="797b7-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="797b7-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="797b7-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="797b7-115">Return code</span></span>                                                                          | <span data-ttu-id="797b7-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="797b7-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="797b7-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="797b7-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="797b7-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="797b7-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="797b7-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="797b7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="797b7-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="797b7-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





