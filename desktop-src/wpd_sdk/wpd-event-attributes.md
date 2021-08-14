---
description: 'para Windows 7, Windows dispositivos portáteis dão suporte aos seguintes atributos para eventos de um serviço de dispositivo. Esses atributos são retornados pelo método IPortableDeviceServiceCapabilities:: geteventattributes.'
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
ms.openlocfilehash: 9ee6fe335d5e3906a923dfe5c470142cdf36fb1e521c3498963e478369a9b251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193287"
---
# <a name="event-attributes-portabledeviceh"></a>Atributos de evento (PortableDevice. h)

para Windows 7, Windows dispositivos portáteis dão suporte aos seguintes atributos para eventos de um serviço de dispositivo. Esses atributos são retornados pelo método [**IPortableDeviceServiceCapabilities:: Geteventattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) .




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

 

 




