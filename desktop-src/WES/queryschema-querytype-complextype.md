---
title: Tipo de consulta complexo
description: Define um conjunto de consultas de seletor e supressor que são usadas para incluir eventos no ou excluir eventos do conjunto de resultados.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- QueryType tipo complexo EventLog
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50c0779b90a6f2e74a873b13d79c6e2083afd0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085511"
---
# <a name="querytype-complex-type"></a>Tipo de consulta complexo

Define um conjunto de consultas de seletor e supressor que são usadas para incluir eventos no ou excluir eventos do conjunto de resultados.

``` syntax
<xs:complexType name="QueryType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="Select">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Suppress">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:attribute name="Id"
        type="long"
        use="optional"
     />
    <xs:attribute name="Path"
        type="anyURI"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                    | Type | Descrição                                                                                                                                                                            |
|------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Não**](queryschema-select-querytype-element.md)     |      | Uma consulta XPath que identifica os eventos a serem incluídos no conjunto de resultados da consulta. Especifique o XPath no corpo de texto deste elemento. O XPath é limitado a 32 expressões.<br/>   |
| [**Suprimir**](queryschema-suppress-querytype-element.md) |      | Uma consulta XPath que identifica os eventos a serem excluídos do conjunto de resultados da consulta. Especifique o XPath no corpo de texto deste elemento. O XPath é limitado a 32 expressões.<br/> |



## <a name="attributes"></a>Atributos



| Nome | Tipo   | Descrição                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID   | long   | Um identificador que identifica exclusivamente essa consulta na lista de consultas. O identificador é baseado em zero. Você deve especificar um identificador se sua lista de consulta contiver mais de uma consulta.<br/> |
| Caminho | anyURI | O nome do canal ou o caminho para o arquivo de log que contém os eventos.<br/>                                                                                                            |
| Caminho | anyURI | O nome do canal ou o caminho para o arquivo de log que contém os eventos.<br/>                                                                                                            |
| Caminho | anyURI | Não usado.<br/>                                                                                                                                                                                |



## <a name="remarks"></a>Comentários

A consulta deve ter pelo menos uma instrução SELECT. Para cada instrução de supressão, deve haver pelo menos uma instrução SELECT que especifique o mesmo caminho. Se a consulta SELECT e dissupressão retornar os mesmos eventos, a instrução suprimir terá precedência. Se você selecionar eventos de várias fontes, os eventos serão retornados na ordem de carimbo de data/hora. Se você usar o carimbo de data/hora do sistema e a taxa de eventos for alta, é possível que mais de um evento tenha o mesmo carimbo de data/hora. Quando isso ocorre, a ordenação de eventos se torna ambígua e os eventos podem aparecer fora de ordem.

Se você especificar um caminho para uma das consultas na lista de consultas, todas as consultas deverão especificar um caminho. Se você não especificar um caminho para todas as consultas, deverá especificar o caminho ao chamar a função [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) ou [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





