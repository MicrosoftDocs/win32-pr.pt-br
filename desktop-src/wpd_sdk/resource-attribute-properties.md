---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de atributo de recurso.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Propriedades do atributo de recurso (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 64f4f394fcd91d50f323a8e46a9556daa6a8dbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814517"
---
# <a name="resource-attribute-properties"></a>Propriedades do atributo de recurso

Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de atributo de recurso.



| Propriedade                                    | VarType         | Descrição                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_chave de \_ recurso de atributo de recurso WPD \_ \_** | **VT \_ desconhecido** | Isso é um [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contém um único valor, que é a chave que identifica o recurso.                     |
| **\_formato de \_ atributo de recurso WPD \_**        | **CLSID do VT \_**   | Um valor de GUID que especifica o formato do recurso. Consulte [formatos de objeto](object-format-guids.md) para obter uma lista de formatos que são definidos por dispositivos portáteis do Windows. |
| **\_ \_ Tamanho total do atributo de recurso WPD \_ \_**   | **\_UI8 VT**     | O tamanho total dos dados do recurso, em bytes.                                                                                                                            |



 

## <a name="remarks"></a>Comentários

Esses atributos são retornados pelo método [**IPortableDeviceResources:: Getresourceattributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceResources:: getresourceattributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




