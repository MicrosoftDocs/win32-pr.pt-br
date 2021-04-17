---
description: O elemento booliano <supportsAdvancedQuerySyntax> especifica se o provedor de pesquisa dá suporte à sintaxe de consulta avançada. O padrão é falso. Esse elemento é opcional e não tem nenhum elemento filho e nenhum atributo.
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: Elemento supportsAdvancedQuerySyntax (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d31eb96615c952f703729fd9d22f2e5d27f38b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763152"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a>Elemento supportsAdvancedQuerySyntax (esquema do conector de pesquisa)

O elemento booliano <supportsAdvancedQuerySyntax> especifica se o provedor de pesquisa dá suporte à [sintaxe de consulta avançada](-search-3x-advancedquerysyntax.md). O padrão é falso. Esse elemento é opcional e não tem nenhum elemento filho e nenhum atributo.

## <a name="syntax"></a>Syntax


```
<!-- supportsAdvancedQuerySyntax -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
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



 

## <a name="remarks"></a>Comentários

O valor `true` indica que o provedor de pesquisa dá suporte à sintaxe de consulta avançada enviada em consultas de pesquisa.

## <a name="example"></a>Exemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 



