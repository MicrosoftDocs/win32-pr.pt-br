---
description: O elemento opcional especifica uma coleção de elementos que definem as inclusões e exclusões de escopo <scope> para esse conector de pesquisa <scopeItem> específico.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Elemento scope (Esquema do Conector de Pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d5fcdb3908f495d07199c61a2005a4f97ba5a01c641fb4e854961489e7abe0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944296"
---
# <a name="scope-element-search-connector-schema"></a>Elemento scope (Esquema do Conector de Pesquisa)

O elemento opcional especifica uma coleção de elementos que definem as inclusões e exclusões de escopo <scope> para esse conector de pesquisa <scopeItem> específico. Se <scope> estiver presente, ele DEVERÁ conter pelo menos um <scopeItem> elemento. Esse elemento não tem atributos.

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

Use os <scope> elementos e para identificar quais locais devem ser <scopeItem> pesquisados e quais locais devem ser excluídos da pesquisa.

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



 

 



