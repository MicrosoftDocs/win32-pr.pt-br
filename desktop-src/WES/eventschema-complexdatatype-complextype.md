---
title: Tipo complexo ComplexDataType
description: Define uma estrutura que contém um ou mais itens de dados.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- Tipo complexo ComplexDataType EventLog
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f86b15defc32469dd1a4abd0f6366e1a93d4b83441b1e1518ff7ac999f30bd59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055804"
---
# <a name="complexdatatype-complex-type"></a>Tipo complexo ComplexDataType

Define uma estrutura que contém um ou mais itens de dados.

``` syntax
<xs:complexType name="ComplexDataType">
    <xs:sequence>
        <xs:element name="Data"
            type="DataType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                  | Type                                                      | Descrição                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Dados**](eventschema-data-complexdatatype-element.md) | [**DataType**](eventschema-datafieldtype-complextype.md) | A lista de itens de dados na estrutura. A lista de itens está na mesma ordem definida no modelo.<br/> |



## <a name="attributes"></a>Atributos



| Nome | Tipo   | Descrição                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome | cadeia de caracteres | O nome da estrutura. Esse é o nome especificado quando você definiu a estrutura no modelo (consulte o tipo complexo [**TemplateItemType).**](eventmanifestschema-templateitemtype-complextype.md)<br/> |



## <a name="remarks"></a>Comentários

A [**função EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) renderiza o conteúdo de uma estrutura como um blob binário; a função não renderiza os itens de dados individuais da estrutura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





