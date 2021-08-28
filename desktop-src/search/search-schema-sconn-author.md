---
description: O &lt; elemento autor opcional &gt; especifica o autor dessa biblioteca. Este elemento não tem elementos filho e nenhum atributo.
ms.assetid: c91042d5-9564-463a-9104-97b927027fc9
title: Elemento Author (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5b99197db6c32be6b6e526a739a5e3fe1f00ef
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887424"
---
# <a name="author-element-search-connector-schema"></a>Elemento Author (esquema do conector de pesquisa)

O &lt; elemento autor opcional &gt; especifica o autor dessa biblioteca. Este elemento não tem elementos filho e nenhum atributo.

## <a name="syntax"></a>Syntax


```
<!-- author -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="author" type="xs:string" minOccurs="0"/>
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
    <author>Joe Smith</author>
    ...
</searchConnectionDescription>
```



 

 



