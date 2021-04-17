---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de dados da seção.
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: Propriedades de atributo de seção (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Section
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 383e2e50aa5d2a922ad50609e316b3dc9905cc38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105808233"
---
# <a name="section-attribute-properties"></a>Propriedades de atributo de seção

Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de dados da seção.



| Propriedade                                             | VarType         | Descrição                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_comprimento de \_ dados da seção WPD \_**                       | **\_UI8 VT**     | Especifica o comprimento do objeto referenciado.                                                                                                                                                                                                                                                                                              |
| **\_deslocamento de \_ dados da seção WPD \_**                       | **\_UI8 VT**     | Especifica o deslocamento de base zero dos dados para o objeto referenciado.                                                                                                                                                                                                                                                                      |
| **\_recurso de \_ \_ objeto referenciado de dados da \_ seção WPD \_** | **VT \_ desconhecido** | Um [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contém um único valor que especifica a chave para um determinado recurso. Esse recurso é o objeto referenciado por \_ um \_ deslocamento de dados da seção WPD \_ e \_ comprimento de dados da seção WPD \_ \_ .<br/> Se essa propriedade não existir, o \_ padrão de recursos WPD \_ será assumido.<br/> |
| **\_unidades de \_ dados da seção WPD \_**                        | **\_UI4 VT**     | Especifica as unidades usadas para esse deslocamento, por exemplo, bytes, milissegundos e assim por diante. Os valores possíveis para essa propriedade são definidos na enumeração **de \_ \_ valores das \_ unidades \_ de dados da seção WPD** no arquivo PortableDevice. h.<br/> Se nenhuma unidade for especificada, serão assumidos bytes.<br/>                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




