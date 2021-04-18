---
description: Os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos de recurso.
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: Atributos de recurso (PortableDevice. h)
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
ms.openlocfilehash: 300add64d332dbc509bef6ec5bb2ad124f7a6b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791417"
---
# <a name="resource-attributes"></a>Atributos de recurso

Os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos de recurso. Esses atributos são retornados pelos seguintes métodos:

-   [**IPortableDeviceResources:: getresourceattributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| Atributo                                                  | VarType      | Descrição                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **o \_ atributo de recurso WPD \_ \_ pode \_ excluir**                  | **BOOL do VT \_** | Um valor booliano que especifica se um cliente tem permissão para excluir o recurso. Se estiver ausente, presume-se que seja falso.                |
| **o \_ atributo de recurso WPD \_ \_ pode \_ ler**                    | **BOOL do VT \_** | Um valor booliano que especifica se um cliente tem permissão para abrir o recurso para acesso de leitura. Se estiver ausente, presume-se que seja falso.  |
| **o \_ atributo de recurso WPD \_ \_ pode \_ gravar**                   | **BOOL do VT \_** | Um valor booliano que especifica se um cliente tem permissão para abrir o recurso para acesso de gravação. Se estiver ausente, presume-se que seja falso. |
| **\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de leitura \_ \_**  | **\_UI4 VT**  | O tamanho de buffer recomendado que um chamador deve usar para leituras em buffer do recurso.                                                  |
| **\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de gravação \_ \_** | **\_UI4 VT**  | O tamanho de buffer recomendado que um chamador deve usar para gravações em buffer no recurso.                                                   |
| **\_ \_ Tamanho total do atributo de recurso WPD \_ \_**                  | **\_UI8 VT**  | O tamanho total dos dados do recurso, em bytes.                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades**](properties-and-attributes.md)
</dt> </dl>

 

 




