---
description: 'A interface IWpdSerializer é usada pelo driver de dispositivo para serializar as interfaces IPortableDeviceValues de e para os buffers de dados brutos usados para se comunicar com o aplicativo. Os aplicativos não precisam usar essa interface, porque os dados são serializados e desserializados automaticamente ao chamar IPortableDevice:: SendCommand. para obter essa interface, chame CoCreateInstance e transmita IWpdSerializer de IID \_ .'
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: Interface IWpdSerializer (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: dde4bfeea596ccc2691323d484f5583d55ade621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811252"
---
# <a name="iwpdserializer-interface"></a><span data-ttu-id="51d4d-103">Interface IWpdSerializer</span><span class="sxs-lookup"><span data-stu-id="51d4d-103">IWpdSerializer interface</span></span>

<span data-ttu-id="51d4d-104">A interface **IWpdSerializer** é usada pelo driver de dispositivo para serializar as interfaces [**IPortableDeviceValues**](iportabledevicevalues.md) de e para os buffers de dados brutos usados para se comunicar com o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="51d4d-104">The **IWpdSerializer** interface is used by the device driver to serialize [**IPortableDeviceValues**](iportabledevicevalues.md) interfaces to and from the raw data buffers used to communicate with the application.</span></span>

<span data-ttu-id="51d4d-105">Os aplicativos não precisam usar essa interface, pois os dados são serializados e desserializados automaticamente ao chamar [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="51d4d-105">Applications do not need to use this interface, because the data is serialized and deserialized automatically when calling [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

<span data-ttu-id="51d4d-106">Para obter essa interface, chame **CoCreateInstance** e transmita **\_ IWpdSerializer IID**.</span><span class="sxs-lookup"><span data-stu-id="51d4d-106">To get this interface, call **CoCreateInstance** and pass in **IID\_IWpdSerializer**.</span></span>

## <a name="members"></a><span data-ttu-id="51d4d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="51d4d-107">Members</span></span>

<span data-ttu-id="51d4d-108">A interface **IWpdSerializer** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="51d4d-108">The **IWpdSerializer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="51d4d-109">**IWpdSerializer** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="51d4d-109">**IWpdSerializer** also has these types of members:</span></span>

-   [<span data-ttu-id="51d4d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="51d4d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="51d4d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="51d4d-111">Methods</span></span>

<span data-ttu-id="51d4d-112">A interface **IWpdSerializer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="51d4d-112">The **IWpdSerializer** interface has these methods.</span></span>



| <span data-ttu-id="51d4d-113">Método</span><span class="sxs-lookup"><span data-stu-id="51d4d-113">Method</span></span>                                                                                          | <span data-ttu-id="51d4d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="51d4d-114">Description</span></span>                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51d4d-115">**GetBufferFromIPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="51d4d-115">**GetBufferFromIPortableDeviceValues**</span></span>](iwpdserializer-getbufferfromiportabledevicevalues.md) | <span data-ttu-id="51d4d-116">Serializa uma interface **IPortableDeviceValues** enviada para uma matriz de bytes alocada.</span><span class="sxs-lookup"><span data-stu-id="51d4d-116">Serializes a submitted **IPortableDeviceValues** interface to an allocated byte array.</span></span><br/>                |
| [<span data-ttu-id="51d4d-117">**GetIPortableDeviceValuesFromBuffer**</span><span class="sxs-lookup"><span data-stu-id="51d4d-117">**GetIPortableDeviceValuesFromBuffer**</span></span>](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | <span data-ttu-id="51d4d-118">Desserializa uma matriz de bytes para uma interface **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="51d4d-118">Deserializes a byte array to an **IPortableDeviceValues** interface.</span></span><br/>                                  |
| [<span data-ttu-id="51d4d-119">**GetSerializedSize**</span><span class="sxs-lookup"><span data-stu-id="51d4d-119">**GetSerializedSize**</span></span>](iwpdserializer-getserializedsize.md)                                   | <span data-ttu-id="51d4d-120">Calcula o tamanho do buffer necessário para manter uma interface **IPortableDeviceValues** serializada.</span><span class="sxs-lookup"><span data-stu-id="51d4d-120">Calculates the buffer size that is required to hold a serialized **IPortableDeviceValues** interface.</span></span><br/> |
| [<span data-ttu-id="51d4d-121">**WriteIPortableDeviceValuesToBuffer**</span><span class="sxs-lookup"><span data-stu-id="51d4d-121">**WriteIPortableDeviceValuesToBuffer**</span></span>](iwpdserializer-writeiportabledevicevaluestobuffer.md) | <span data-ttu-id="51d4d-122">Serializa uma interface **IPortableDeviceValues** para uma matriz de bytes alocada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="51d4d-122">Serializes an **IPortableDeviceValues** interface to a caller-allocated byte array.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="51d4d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51d4d-123">Requirements</span></span>



| <span data-ttu-id="51d4d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="51d4d-124">Requirement</span></span> | <span data-ttu-id="51d4d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="51d4d-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51d4d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51d4d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="51d4d-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="51d4d-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="51d4d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="51d4d-128">Library</span></span><br/> | <dl> <span data-ttu-id="51d4d-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51d4d-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51d4d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="51d4d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51d4d-131">**Interfaces de driver**</span><span class="sxs-lookup"><span data-stu-id="51d4d-131">**Driver Interfaces**</span></span>](driver-interfaces.md)
</dt> </dl>

 

