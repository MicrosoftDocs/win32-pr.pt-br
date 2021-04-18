---
description: 'Para o Windows 7, os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos para métodos de um serviço de dispositivo. Esses atributos são retornados pelo método IPortableDeviceServiceCapabilities:: getmethodattributes.'
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: Atributos do método (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Method
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: fe638bcd0d87af7b16bfb4f202f21cea97908fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105807139"
---
# <a name="method-attributes"></a>Atributos de método

Para o Windows 7, os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos para métodos de um serviço de dispositivo. Esses atributos são retornados pelo método [**IPortableDeviceServiceCapabilities:: Getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) .




| Atributo                                      | VarType         | Descrição                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| **\_acesso de \_ atributo de método WPD \_**             | **CLSID do VT \_**   | O método necessário de acesso.                                                                                               |
| **\_ \_ formato associado de atributo de método WPD \_ \_** | **CLSID do VT \_**   | O formato associado ao método ou ao **GUID \_ NULL** se não houver nenhum formato associado.                                |
| **\_nome do \_ atributo do método WPD \_**               | **LPWStr do VT \_**  | Uma cadeia de caracteres que especifica o nome amigável de script do método. Os caracteres válidos são alfanuméricos \[ a-zA-Z0-9 \] e ' \_ '. |
| **\_parâmetros de \_ atributo do método WPD \_**         | **VT \_ desconhecido** | Uma interface [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contém os parâmetros do método.    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




