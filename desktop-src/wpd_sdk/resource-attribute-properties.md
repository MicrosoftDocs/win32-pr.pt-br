---
description: Windows Os Dispositivos Portáteis são compatíveis com as seguintes propriedades de atributo de recurso.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Propriedades do Atributo de Recurso (PortableDevice.h)
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
ms.openlocfilehash: 956cd349089afb00a1350bf32e8f06acd5747599f6d5a731e4bf5d8dd1c96295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928066"
---
# <a name="resource-attribute-properties"></a>Propriedades do atributo de recurso

Windows Os Dispositivos Portáteis são compatíveis com as seguintes propriedades de atributo de recurso.



| Propriedade                                    | VarType         | Descrição                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CHAVE DE RECURSO \_ DO \_ ATRIBUTO DE RECURSO \_ \_ WPD** | **VT \_ UNKNOWN** | Essa é uma [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contém um único valor, que é a chave que identifica o recurso.                     |
| **FORMATO DE \_ ATRIBUTO DE \_ RECURSO WPD \_**        | **\_CLSID da VT**   | Um valor guid que especifica o formato do recurso. Consulte [Formatos de objeto](object-format-guids.md) para ver uma lista de formatos que são definidos por Windows Dispositivos Portáteis. |
| **TAMANHO TOTAL \_ DO \_ ATRIBUTO DE RECURSO \_ WPD \_**   | **VT \_ UI8**     | O tamanho total dos dados do recurso, em bytes.                                                                                                                            |



 

## <a name="remarks"></a>Comentários

Esses atributos são retornados pelo [**método IPortableDeviceResources::GetResourceAttributes.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




