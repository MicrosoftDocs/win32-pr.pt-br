---
description: O &lt; &gt; elemento Depth especifica se o escopo do conector de pesquisa deve incluir URLs filho. Os valores permitidos são Deep e superficial. Este elemento não tem elementos filho e nenhum atributo.
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: Elemento Depth (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 430ad3d047331a4bb3ffc58bd134d2364aaa0838
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886765"
---
# <a name="depth-element-search-connector-schema"></a>Elemento Depth (esquema do conector de pesquisa)

O &lt; &gt; elemento Depth especifica se o escopo do conector de pesquisa deve incluir URLs filho. Os valores permitidos são `Deep` e `Shallow` . Este elemento não tem elementos filho e nenhum atributo.

## <a name="syntax"></a>Syntax


```
<!-- depth -->
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
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
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

Se a profundidade for profunda, os usuários poderão procurar ou pesquisar itens no nível da URL do scopeItem ou em quaisquer URLs filho.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra um escopo de pesquisa que inclui C: \\ FolderA e todas as suas pastas filho e C: \\ FolderB, mas nenhuma de suas pastas filhas.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



