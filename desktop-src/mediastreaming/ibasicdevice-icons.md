---
title: Método de ícones de IBasicDevice
description: Retorna um vetor de interfaces IDeviceIcon.
ms.assetid: 0C083AF3-FE22-4A8E-87B7-0FFA7B65ADBD
keywords:
- Método de ícones API de streaming de mídia
- Método de ícones API de streaming de mídia, interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, método de ícones
topic_type:
- apiref
api_name:
- IBasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fb6e4b708b4e38ffb39f152308cec7b885a772f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640521"
---
# <a name="ibasicdeviceicons-method"></a><span data-ttu-id="5cb95-106">Método IBasicDevice:: ícones</span><span class="sxs-lookup"><span data-stu-id="5cb95-106">IBasicDevice::Icons method</span></span>

<span data-ttu-id="5cb95-107">Retorna um vetor de interfaces [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="5cb95-107">Returns a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cb95-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5cb95-108">Syntax</span></span>


```C++
HRESULT Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="parameters"></a><span data-ttu-id="5cb95-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5cb95-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cb95-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="5cb95-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5cb95-111">Recebe uma coleção enumerável de ponteiros de interface [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="5cb95-111">Receives an enumerable collection of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cb95-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5cb95-112">Return value</span></span>

<span data-ttu-id="5cb95-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5cb95-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5cb95-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5cb95-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5cb95-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5cb95-115">Return code</span></span>                                                                          | <span data-ttu-id="5cb95-116">Description</span><span class="sxs-lookup"><span data-stu-id="5cb95-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5cb95-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5cb95-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5cb95-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5cb95-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="5cb95-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5cb95-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cb95-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="5cb95-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

