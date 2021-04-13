---
title: Tipo complexo de tipo de dados (log de eventos do Windows)
description: Define um item de dados.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- Log de tipos complexo de tipo de dados
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d3ac6e545cbe8567bbe041568c442f762743ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295859"
---
# <a name="datatype-complex-type"></a>Tipo complexo de tipo de dados

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
| Nome | cadeia de caracteres | O nome de um item de dados que foi definido no modelo (consulte o tipo complexo [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).<br/> |
| Tipo | QName  | Não usado.<br/>                                                                                                                                                     |



## <a name="remarks"></a>Comentários

O item de dados pode ser um item de dados de nível superior ou um item de dados em uma estrutura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





