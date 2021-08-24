---
description: A interface IWpdSerializer é usada pelo driver de dispositivo para serializar interfaces IPortableDeviceValues de e para os buffers de dados brutos usados para se comunicar com o aplicativo. Os aplicativos não precisam usar essa interface, pois os dados são serializados e desserializados automaticamente ao chamar IPortableDevice::SendCommand.Para obter essa interface, chame CoCreateInstance e passe IID \_ IWpdSerializer.
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: Interface IWpdSerializer (PortableDeviceTypes.h)
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
ms.openlocfilehash: 51bb44a7ffec600ff6a059815f096b6920095ece1abd6606e9449045137dbc61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704456"
---
# <a name="iwpdserializer-interface"></a>Interface IWpdSerializer

A interface **IWpdSerializer** é usada pelo driver de dispositivo para serializar interfaces [**IPortableDeviceValues**](iportabledevicevalues.md) de e para os buffers de dados brutos usados para se comunicar com o aplicativo.

Os aplicativos não precisam usar essa interface, pois os dados são serializados e desserializados automaticamente ao chamar [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

Para obter essa interface, chame **CoCreateInstance** e passe **IID \_ IWpdSerializer**.

## <a name="members"></a>Membros

A interface **IWpdSerializer** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWpdSerializer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWpdSerializer** tem esses métodos.



| Método                                                                                          | Descrição                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md) | Serializa uma interface **IPortableDeviceValues** enviada para uma matriz de byte alocada.<br/>                |
| [**GetIPortableDeviceValuesFromBuffer**](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | Deserializa uma matriz de byte para uma interface **IPortableDeviceValues.**<br/>                                  |
| [**GetSerializedSize**](iwpdserializer-getserializedsize.md)                                   | Calcula o tamanho do buffer necessário para manter uma interface **IPortableDeviceValues** serializada.<br/> |
| [**WriteIPortableDeviceValuesToBuffer**](iwpdserializer-writeiportabledevicevaluestobuffer.md) | Serializa uma interface **IPortableDeviceValues** para uma matriz de byte alocada pelo chamador.<br/>                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Driver Interfaces**](driver-interfaces.md)
</dt> </dl>

 

