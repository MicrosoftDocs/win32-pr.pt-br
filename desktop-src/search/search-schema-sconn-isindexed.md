---
description: o elemento booliano opcional <isIndexed> especifica se o local descrito pelo conector de pesquisa é indexado (local ou remotamente usando Windows search 4 ou superior).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Elemento IsIndexed (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afcd1a95ec14b3bbea80374d8925a88231feb0110a421c2c850a297672d0c1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711046"
---
# <a name="isindexed-element-search-connector-schema"></a>Elemento IsIndexed (esquema do conector de pesquisa)

o elemento booliano opcional <isIndexed> especifica se o local descrito pelo conector de pesquisa é indexado (local ou remotamente usando Windows search 4 ou superior). O valor padrão é true para pastas locais. Este elemento não tem elementos filho e nenhum atributo.

## <a name="syntax"></a>Syntax


```
<!-- isIndexed -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isIndexed" type="xsIboolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                                                                   | Elementos filho |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a>Exemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 



