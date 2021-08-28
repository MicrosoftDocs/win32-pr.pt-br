---
description: O &lt; elemento scopeItem &gt; representa uma única entrada na tabela de escopo de exclusão/inclusão.
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: Elemento scopeItem (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a585acd065efcbc58091d4c8bebce733ed2c73
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880445"
---
# <a name="scopeitem-element-search-connector-schema"></a>Elemento scopeItem (esquema do conector de pesquisa)

O &lt; elemento scopeItem &gt; representa uma única entrada na tabela de escopo de exclusão/inclusão. &lt;scopeItem estende o tipo shellLinkType padrão adicionando três novos elementos que controlam a inclusão e a exclusão de pastas, controlam a profundidade dos resultados e especificam o local do &gt; escopo. Se o &lt; elemento &gt; de escopo existir, esse elemento será necessário. Ele tem três elementos filho e nenhum atributos.

## <a name="syntax"></a>Syntax


```
<!-- scopeItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                <xs:element name="mode" default="Include">
                                    ...
                                </xs:element>
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    ...
                                </xs:element>
                                <xs:element name="url" type="xs:anyURI"/>
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



| Elemento pai                                                           | Elementos filho                                                                        |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Elemento scope (Esquema do Conector de Pesquisa)](search-schema-sconn-scope.md) | [Elemento scope (Esquema do Conector de Pesquisa)](search-schema-sconn-scope-mode.md).        |
|                                                                          | [Elemento scope (Esquema do Conector de Pesquisa)](search-schema-sconn-scope-depth.md).       |
|                                                                          | [Elemento scopeItem url (Esquema do Conector de Pesquisa)](search-schema-sconn-scope-url.md). |



 

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



 

 



