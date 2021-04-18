---
description: O <scope> elemento opcional especifica uma coleção de <scopeItem> elementos que definem as inclusões e exclusões de escopo para esse conector de pesquisa específico.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Elemento Scope (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f49041170db80de48d312596249d5c4dca835e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810617"
---
# <a name="scope-element-search-connector-schema"></a>Elemento Scope (esquema do conector de pesquisa)

O <scope> elemento opcional especifica uma coleção de <scopeItem> elementos que definem as inclusões e exclusões de escopo para esse conector de pesquisa específico. Se <scope> estiver presente, ele deve conter pelo menos um <scopeItem> elemento. Esse elemento não tem atributos.

## <a name="syntax"></a>Syntax


```
<!-- scope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                       ...
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                                                                   | Elementos filho                                                                    |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)](search-schema-searchconnectordescription.md) | [elemento scopeItem (esquema do conector de pesquisa)](search-schema-sconn-scopeitem.md). |



 

## <a name="remarks"></a>Comentários

Use os <scope> <scopeItem> elementos e para identificar quais locais devem ser pesquisados e quais locais devem ser excluídos da pesquisa.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra um escopo de pesquisa que inclui C: \\ ExampleFolder e todas as suas pastas filho, exceto c: \\ ExampleFolder \\ ExcludeMe.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Exclude</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



