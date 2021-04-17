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
# <a name="iwpdserializer-interface"></a>Interface IWpdSerializer

A interface **IWpdSerializer** é usada pelo driver de dispositivo para serializar as interfaces [**IPortableDeviceValues**](iportabledevicevalues.md) de e para os buffers de dados brutos usados para se comunicar com o aplicativo.

Os aplicativos não precisam usar essa interface, pois os dados são serializados e desserializados automaticamente ao chamar [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

Para obter essa interface, chame **CoCreateInstance** e transmita **\_ IWpdSerializer IID**.

## <a name="members"></a>Membros

A interface **IWpdSerializer** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWpdSerializer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWpdSerializer** tem esses métodos.



| Método                                                                                          | Descrição                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md) | Serializa uma interface **IPortableDeviceValues** enviada para uma matriz de bytes alocada.<br/>                |
| [**GetIPortableDeviceValuesFromBuffer**](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | Desserializa uma matriz de bytes para uma interface **IPortableDeviceValues** .<br/>                                  |
| [**GetSerializedSize**](iwpdserializer-getserializedsize.md)                                   | Calcula o tamanho do buffer necessário para manter uma interface **IPortableDeviceValues** serializada.<br/> |
| [**WriteIPortableDeviceValuesToBuffer**](iwpdserializer-writeiportabledevicevaluestobuffer.md) | Serializa uma interface **IPortableDeviceValues** para uma matriz de bytes alocada pelo chamador.<br/>                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces de driver**](driver-interfaces.md)
</dt> </dl>

 

