---
description: O <mode> elemento especifica se a URL deve ser incluída ou excluída do escopo do conector de pesquisa. Os valores permitidos são Incluir e Excluir. Esse elemento não tem nenhum elemento filho e nenhum atributos.
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: Elemento mode (Esquema do Conector de Pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a210abf5c9c2bbc4cd5d53978866a729d834928cf39e54bfb6e6fcc9c42c7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944316"
---
# <a name="mode-element-search-connector-schema"></a>Elemento mode (Esquema do Conector de Pesquisa)

O <mode> elemento especifica se a URL deve ser incluída ou excluída do escopo do conector de pesquisa. Os valores permitidos são `Include` e `Exclude` . Esse elemento não tem nenhum elemento filho e nenhum atributos.

## <a name="syntax"></a>Syntax


```
<!-- mode -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="mode" default="Include">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Include"/>
                                            <xs:enumeration value="Exclude"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
                            </xs:all>
                        </xs:complexType>
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



| Elemento pai                                                                   | Elementos filho |
|----------------------------------------------------------------------------------|----------------|
| [Elemento scopeItem (esquema do conector de pesquisa)](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>Comentários

Um escopo excluído não pode ser pesquisado ou pesquisado. Você pode aninhar URLs scopeItem. Por exemplo, você pode incluir um escopo pai e todos os seus filhos, exceto um, adicionando a URL pai como incluída, com o valor de profundidade Deep e excluindo a URL filho.

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
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



