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
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a>Recuperando propriedades de vários objetos por formato de objeto

Além de uma recuperação em massa de propriedades para uma coleção de identificadores de objeto, um aplicativo também pode executar uma recuperação em massa de propriedades para todos os objetos de um tipo específico. Como no exemplo anterior, a recuperação em massa para um determinado tipo requer que o driver de dispositivo dê suporte a recuperações em massa.

Seu aplicativo pode executar uma recuperação em massa usando as interfaces descritas na tabela a seguir.



| Interface                                                                                      | Descrição                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Fornece acesso aos métodos específicos de conteúdo.                   |
| [**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Usado para identificar as propriedades a serem recuperadas.                   |
| [**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Usado para determinar se um determinado driver dá suporte a operações em massa. |
| [**Interface IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Dá suporte à operação de recuperação em massa.                             |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Usado para armazenar os identificadores de objeto para a operação em massa.       |



 

A função ReadContentPropertiesBulkFilteringFormat no módulo Contentproperties. cpp do aplicativo de exemplo demonstra uma operação de recuperação em massa para objetos de um tipo ou formato específico.

O código encontrado na função ReadContentPropertiesBulkFilteringFormat é quase idêntico ao código encontrado na função ReadContentPropertiesBulk. (Consulte o tópico [Recuperando propriedades de vários objetos](retrieving-properties-for-multiple-objects.md) para obter uma descrição completa dessa função.)

A única diferença principal ocorre quando a operação é enfileirada. Ao filtrar por tipo ou formato, o método [**IPortableDevicePropertiesBulk:: QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) é chamado em vez do método [**IPortableDevicePropertiesBulk:: QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) .


```C++
hr = pPropertiesBulk->QueueGetValuesByObjectFormat(WPD_OBJECT_FORMAT_WMA,
                                                   WPD_DEVICE_OBJECT_ID,
                                                   100,
                                                   pPropertiesToRead,
                                                   pCallback,
                                                   &guidContext);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Interface IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



