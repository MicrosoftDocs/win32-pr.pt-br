---
description: O elemento booliana opcional especifica se o local descrito no conector de pesquisa deve ser usado como o local de salvar padrão quando um usuário de outro computador em um Grupo Doméstico optar por salvar <isDefaultNonOwnerSaveLocation> um item.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: Elemento isDefaultNonOwnerSaveLocation (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7bbffe620e5d59b3ff7a868048f3518b8fc0ea2737a1597f3594412b8839c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118051528"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a>Elemento isDefaultNonOwnerSaveLocation (esquema do conector de pesquisa)

O elemento booliana opcional especifica se o local descrito no conector de pesquisa deve ser usado como o local de salvar padrão quando um usuário de outro computador em um Grupo Doméstico optar por salvar <isDefaultNonOwnerSaveLocation> um item. Esse elemento não tem nenhum elemento filho e nenhum atributos.

## <a name="syntax"></a>Syntax


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
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

Se for true, quando um usuário de outro computador em um Grupo Doméstico optar por salvar um item, o Windows Explorer salvará o item no local especificado no <simpleLocation> elemento.

## <a name="example"></a>Exemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



