---
description: O elemento <supportsAdvancedQuerySyntax> booliana especifica se o provedor de pesquisa dá suporte à Sintaxe de Consulta Avançada. O padrão é falso. Esse elemento é opcional e não tem nenhum elemento filho e nenhum atributos.
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: Elemento supportsAdvancedQuerySyntax (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8235c1021ae04cbbce65500ebf008f645ef74c1f2bb6ea7f3a9edfe4253e035
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844506"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a>Elemento supportsAdvancedQuerySyntax (esquema do conector de pesquisa)

O elemento <supportsAdvancedQuerySyntax> booliana especifica se o provedor de pesquisa dá suporte à [Sintaxe de Consulta Avançada](-search-3x-advancedquerysyntax.md). O padrão é falso. Esse elemento é opcional e não tem nenhum elemento filho e nenhum atributos.

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

O valor indica que o provedor de pesquisa dá `true` suporte à Sintaxe de Consulta Avançada enviada em consultas de pesquisa.

## <a name="example"></a>Exemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 



