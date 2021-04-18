---
description: 'Para o Windows 7, os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos para eventos de um serviço de dispositivo. Esses atributos são retornados pelo método IPortableDeviceServiceCapabilities:: geteventattributes.'
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Atributos de evento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 68a5964a4f64899d4aa116002b1feb14ce360498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788930"
---
# <a name="event-attributes-portabledeviceh"></a>Atributos de evento (PortableDevice. h)

Para o Windows 7, os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos para eventos de um serviço de dispositivo. Esses atributos são retornados pelo método [**IPortableDeviceServiceCapabilities:: Geteventattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) .




| Atributo                             | VarType         | Descrição                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| **\_nome do \_ atributo de evento WPD \_**       | **LPWStr do VT \_**  | Uma cadeia de caracteres que especifica o nome amigável de script do evento. Os caracteres válidos são alfanuméricos \[ a-zA-Z0-9 \] e ' \_ '. |
| **\_Opções de \_ atributo de evento WPD \_**    | **VT \_ desconhecido** | Um [**IPortableDeviceValues**](iportabledevicevalues.md) que contém as opções de evento.                               |
| **\_parâmetros de \_ atributo de evento WPD \_** | **VT \_ desconhecido** | Um [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contém os parâmetros do evento.              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




