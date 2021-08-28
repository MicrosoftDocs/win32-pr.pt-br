---
title: Tipo complexo DataType (Windows log de eventos)
description: Define um item de dados.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- Tipo complexo DataType EventLog
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba1fcbf217b16fb675a7a4eca00c8faa201737c07eea35a809f85617e96e9445
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620276"
---
# <a name="datatype-complex-type"></a>Tipo complexo DataType

Define um item de dados.

``` syntax
<xs:complexType name="DataType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="Name"
                type="string"
                use="optional"
             />
            <xs:attribute name="Type"
                type="QName"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nome | Tipo   | Descrição                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome | cadeia de caracteres | O nome de um item de dados que foi definido no modelo (consulte o tipo complexo [**TemplateItemType).**](eventmanifestschema-templateitemtype-complextype.md)<br/> |
| Tipo | QName  | Não usado.<br/>                                                                                                                                                     |



## <a name="remarks"></a>Comentários

O item de dados pode ser um item de dados de nível superior ou um item de dados em uma estrutura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





