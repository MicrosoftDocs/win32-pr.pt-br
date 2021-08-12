---
title: Tipo complexo QueryType
description: Define um conjunto de consultas de seletor e supressor que são usadas para incluir eventos em ou excluir eventos do conjunto de resultados.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- Tipo complexo QueryType EventLog
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6585b43e1e9e48bc0be69001d471c74e52506177250d66316273ca447b38084a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587621"
---
# <a name="querytype-complex-type"></a>Tipo complexo QueryType

Define um conjunto de consultas de seletor e supressor que são usadas para incluir eventos em ou excluir eventos do conjunto de resultados.

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
| [**Selecionar**](queryschema-select-querytype-element.md)     |      | Uma consulta XPath que identifica os eventos a incluir no conjunto de resultados da consulta. Especifique o XPath no corpo do texto desse elemento. O XPath é limitado a 32 expressões.<br/>   |
| [**Suprimir**](queryschema-suppress-querytype-element.md) |      | Uma consulta XPath que identifica os eventos a excluir do conjunto de resultados da consulta. Especifique o XPath no corpo do texto desse elemento. O XPath é limitado a 32 expressões.<br/> |



## <a name="attributes"></a>Atributos



| Nome | Tipo   | Descrição                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID   | long   | Um identificador que identifica exclusivamente essa consulta em sua lista de consultas. O identificador é baseado em zero. Você deverá especificar um identificador se a lista de consultas contiver mais de uma consulta.<br/> |
| Caminho | anyURI | O nome do canal ou o caminho para o arquivo de log que contém os eventos.<br/>                                                                                                            |
| Caminho | anyURI | O nome do canal ou o caminho para o arquivo de log que contém os eventos.<br/>                                                                                                            |
| Caminho | anyURI | Não usado.<br/>                                                                                                                                                                                |



## <a name="remarks"></a>Comentários

A consulta deve ter pelo menos uma instrução select. Para cada instrução suppress, deve haver pelo menos uma instrução select que especifique o mesmo caminho. Se a consulta select e suppress retornar os mesmos eventos, a instrução suppress tem precedência. Se você selecionar eventos de várias fontes, os eventos serão retornados na ordem do carimbo de data/hora. Se você usar o carimbo de data/hora do sistema e a taxa de eventos for alta, é possível que mais de um evento tenha o mesmo carimbo de data/hora. Quando isso ocorre, a ordenação de eventos se torna ambígua e os eventos podem aparecer fora de ordem.

Se você especificar um caminho para uma das consultas na lista de consultas, todas as consultas deverão especificar um caminho. Se você não especificar um caminho para todas as consultas, deverá especificar o caminho ao chamar a função [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) ou [**EvtSubscribe.**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





