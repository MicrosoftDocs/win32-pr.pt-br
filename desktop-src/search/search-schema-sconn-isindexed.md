---
description: O elemento booliano opcional <isIndexed> especifica se o local descrito pelo conector de pesquisa é indexado (local ou remotamente usando o Windows Search 4 ou superior).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Elemento IsIndexed (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f658f6b932f6241b7af84e763d564ca0a8f1b5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090044"
---
# <a name="isindexed-element-search-connector-schema"></a>Elemento IsIndexed (esquema do conector de pesquisa)

O elemento booliano opcional <isIndexed> especifica se o local descrito pelo conector de pesquisa é indexado (local ou remotamente usando o Windows Search 4 ou superior). O valor padrão é true para pastas locais. Este elemento não tem elementos filho e nenhum atributo.

## <a name="syntax"></a>Sintaxe


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



 

 



