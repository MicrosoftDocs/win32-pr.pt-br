---
title: Tipo complexo ComplexDataType
description: Define uma estrutura que contém um ou mais itens de dados.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- Log de eventos do tipo complexo ComplexDataType
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 598f2cc02f1e3675ff0c8fd6eae7f9a5e02b9407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794542"
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
| [**Dados**](eventschema-data-complexdatatype-element.md) | [**Tipo de dados**](eventschema-datafieldtype-complextype.md) | A lista de itens de dados na estrutura. A lista de itens está na mesma ordem definida no modelo.<br/> |



## <a name="attributes"></a>Atributos



| Nome | Tipo   | Descrição                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome | cadeia de caracteres | O nome da estrutura. Esse é o nome especificado quando você definiu a estrutura no modelo (consulte o tipo complexo [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).<br/> |



## <a name="remarks"></a>Comentários

A função [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) processa o conteúdo de uma estrutura como um blob binário; a função não processa os itens de dados individuais da estrutura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





