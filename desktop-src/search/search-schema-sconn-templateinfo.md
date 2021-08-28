---
description: Esse &lt; elemento templateInfo opcional &gt; especifica um tipo de pasta para exibir os resultados de uma consulta nesse conector de pesquisa. Este elemento não tem atributos e apenas um filho obrigatório.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: Elemento templateInfo (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c815d04e23f1e1af9582ad93ba08d118855676
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880389"
---
# <a name="templateinfo-element-search-connector-schema"></a>Elemento templateInfo (esquema do conector de pesquisa)

Esse &lt; elemento templateInfo opcional &gt; especifica um tipo de pasta para exibir os resultados de uma consulta nesse conector de pesquisa. Este elemento não tem atributos e apenas um filho obrigatório.

## <a name="syntax"></a>Syntax


```
<!-- templateInfo -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="templateInfo" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="folderType" minOccurs="0"/>
                    </xs:all>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                                                                   | Elementos filho                                                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)](search-schema-searchconnectordescription.md) | [Elemento FolderType (esquema do conector de pesquisa)](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a>Comentários

se você não especificar um tipo de pasta específico no &lt; &gt; elemento templateInfo, Windows usará o tipo de pasta do conector de pesquisa geral {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.

## <a name="example-of-a-templateinfo-element"></a>Exemplo de um elemento templateInfo


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



