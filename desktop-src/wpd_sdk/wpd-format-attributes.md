---
description: Por Windows 7, Windows Dispositivos Portáteis dá suporte aos seguintes atributos para formatos em um serviço de dispositivo. Esses atributos são retornados pelo método IPortableDeviceServiceCapabilities::GetFormatAttributes.
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: Atributos de formato (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Format
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: d8144c8a290b6ab7e3d3b13b1f3ee53d377e015950fea6d7e1ebf6786fd9d854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117652690"
---
# <a name="format-attributes"></a>Atributos de formato

Por Windows 7, Windows Dispositivos Portáteis dá suporte aos seguintes atributos para formatos em um serviço de dispositivo. Esses atributos são retornados pelo [**método IPortableDeviceServiceCapabilities::GetFormatAttributes.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes)




| **Atributo**                        | **VarType**    | **Descrição**                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| **ATRIBUTO DE FORMATO WPD \_ \_ \_ MIMETYPE** | **VT \_ LPWSTR** | O tipo MIME de formato.                                                                                                     |
| **NOME DO ATRIBUTO DE FORMATO WPD \_ \_ \_**     | **VT \_ LPWSTR** | Uma cadeia de caracteres que especifica o nome amigável de script do formato. Os caracteres válidos são alfanuméricos \[ a-zA-Z0-9 \] e ' \_ '. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos**](properties-and-attributes.md)
</dt> </dl>

 

 




