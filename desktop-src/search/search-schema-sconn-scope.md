---
description: O elemento de escopo opcional especifica uma coleção de elementos scopeItem que definem as inclusões e exclusões de escopo &lt; para esse conector de pesquisa &gt; &lt; &gt; específico.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Elemento scope (Esquema do Conector de Pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c011eee8def80a7f1d395a7a52a72d30fb4935
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886699"
---
# <a name="scope-element-search-connector-schema"></a>Elemento scope (Esquema do Conector de Pesquisa)

O elemento de escopo opcional especifica uma coleção de elementos scopeItem que definem as inclusões e exclusões de escopo &lt; para esse conector de pesquisa &gt; &lt; &gt; específico. Se &lt; o escopo estiver &gt; presente, ele DEVERÁ conter pelo menos um &lt; elemento &gt; scopeItem. Esse elemento não tem atributos.

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
| [Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)](search-schema-searchconnectordescription.md) | [Elemento scopeItem (esquema do conector de pesquisa)](search-schema-sconn-scopeitem.md). |



 

## <a name="remarks"></a>Comentários

Use os &lt; elementos scope &gt; e &lt; scopeItem &gt; para identificar quais locais devem ser pesquisados e quais locais devem ser excluídos da pesquisa.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra um escopo de pesquisa que inclui C: ExampleFolder e todas as suas pastas filho, exceto \\ C: \\ ExampleFolder \\ ExcludeMe.


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



 

 



