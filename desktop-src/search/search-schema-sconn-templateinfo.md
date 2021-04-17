---
description: Esse <templateInfo> elemento opcional especifica um tipo de pasta para exibir os resultados de uma consulta nesse conector de pesquisa. Este elemento não tem atributos e apenas um filho obrigatório.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: Elemento templateInfo (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fd28780689b4d544f251bbaf1542bc379ecdaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763970"
---
# <a name="templateinfo-element-search-connector-schema"></a>Elemento templateInfo (esquema do conector de pesquisa)

Esse <templateInfo> elemento opcional especifica um tipo de pasta para exibir os resultados de uma consulta nesse conector de pesquisa. Este elemento não tem atributos e apenas um filho obrigatório.

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

Se você não especificar um tipo de pasta específico no <templateInfo> elemento, o Windows usará o tipo de pasta do conector de pesquisa geral {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.

## <a name="example-of-a-templateinfo-element"></a>Exemplo de um elemento templateInfo


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



