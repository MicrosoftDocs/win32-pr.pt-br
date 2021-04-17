---
description: Recuperando propriedades de vários objetos por formato de objeto
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: Recuperando propriedades de vários objetos por formato de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a352704b3ce5d063c544a41c467f372554bc901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461244"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a><span data-ttu-id="74250-103">Recuperando propriedades de vários objetos por formato de objeto</span><span class="sxs-lookup"><span data-stu-id="74250-103">Retrieving Properties for Multiple Objects by Object Format</span></span>

<span data-ttu-id="74250-104">Além de uma recuperação em massa de propriedades para uma coleção de identificadores de objeto, um aplicativo também pode executar uma recuperação em massa de propriedades para todos os objetos de um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="74250-104">In addition to a bulk retrieval of properties for a collection of object identifiers, an application can also perform a bulk retrieval of properties for all objects of a particular type.</span></span> <span data-ttu-id="74250-105">Como no exemplo anterior, a recuperação em massa para um determinado tipo requer que o driver de dispositivo dê suporte a recuperações em massa.</span><span class="sxs-lookup"><span data-stu-id="74250-105">As in the previous example, bulk retrieval for a given type requires that the device driver support bulk retrievals.</span></span>

<span data-ttu-id="74250-106">Seu aplicativo pode executar uma recuperação em massa usando as interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="74250-106">Your application can perform a bulk retrieval using the interfaces described in the following table.</span></span>



| <span data-ttu-id="74250-107">Interface</span><span class="sxs-lookup"><span data-stu-id="74250-107">Interface</span></span>                                                                                      | <span data-ttu-id="74250-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="74250-108">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="74250-109">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="74250-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="74250-110">Fornece acesso aos métodos específicos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="74250-110">Provides access to the content-specific methods.</span></span>                   |
| [<span data-ttu-id="74250-111">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="74250-111">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="74250-112">Usado para identificar as propriedades a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="74250-112">Used to identify the properties to be retrieved.</span></span>                   |
| [<span data-ttu-id="74250-113">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="74250-113">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="74250-114">Usado para determinar se um determinado driver dá suporte a operações em massa.</span><span class="sxs-lookup"><span data-stu-id="74250-114">Used to determine whether a given driver supports bulk operations.</span></span> |
| [<span data-ttu-id="74250-115">**Interface IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="74250-115">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="74250-116">Dá suporte à operação de recuperação em massa.</span><span class="sxs-lookup"><span data-stu-id="74250-116">Supports the bulk retrieval operation.</span></span>                             |
| [<span data-ttu-id="74250-117">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="74250-117">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="74250-118">Usado para armazenar os identificadores de objeto para a operação em massa.</span><span class="sxs-lookup"><span data-stu-id="74250-118">Used to store the object identifiers for the bulk operation.</span></span>       |



 

<span data-ttu-id="74250-119">A função ReadContentPropertiesBulkFilteringFormat no módulo Contentproperties. cpp do aplicativo de exemplo demonstra uma operação de recuperação em massa para objetos de um tipo ou formato específico.</span><span class="sxs-lookup"><span data-stu-id="74250-119">The ReadContentPropertiesBulkFilteringFormat function in the sample application's ContentProperties.cpp module demonstrates a bulk retrieval operation for objects of a particular type or format.</span></span>

<span data-ttu-id="74250-120">O código encontrado na função ReadContentPropertiesBulkFilteringFormat é quase idêntico ao código encontrado na função ReadContentPropertiesBulk.</span><span class="sxs-lookup"><span data-stu-id="74250-120">The code found in the ReadContentPropertiesBulkFilteringFormat function is almost identical to the code found in the ReadContentPropertiesBulk function.</span></span> <span data-ttu-id="74250-121">(Consulte o tópico [Recuperando propriedades de vários objetos](retrieving-properties-for-multiple-objects.md) para obter uma descrição completa dessa função.)</span><span class="sxs-lookup"><span data-stu-id="74250-121">(See the [Retrieving Properties for Multiple Objects](retrieving-properties-for-multiple-objects.md) topic for a complete description of this function.)</span></span>

<span data-ttu-id="74250-122">A única diferença principal ocorre quando a operação é enfileirada.</span><span class="sxs-lookup"><span data-stu-id="74250-122">The one primary difference occurs when the operation is queued.</span></span> <span data-ttu-id="74250-123">Ao filtrar por tipo ou formato, o método [**IPortableDevicePropertiesBulk:: QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) é chamado em vez do método [**IPortableDevicePropertiesBulk:: QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) .</span><span class="sxs-lookup"><span data-stu-id="74250-123">When filtering by type or format, the [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) method is called instead of the [**IPortableDevicePropertiesBulk::QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) method.</span></span>


```C++
hr = pPropertiesBulk->QueueGetValuesByObjectFormat(WPD_OBJECT_FORMAT_WMA,
                                                   WPD_DEVICE_OBJECT_ID,
                                                   100,
                                                   pPropertiesToRead,
                                                   pCallback,
                                                   &guidContext);
```



## <a name="related-topics"></a><span data-ttu-id="74250-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74250-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74250-125">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="74250-125">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="74250-126">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="74250-126">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="74250-127">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="74250-127">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="74250-128">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="74250-128">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="74250-129">**Interface IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="74250-129">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="74250-130">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="74250-130">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="74250-131">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="74250-131">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



