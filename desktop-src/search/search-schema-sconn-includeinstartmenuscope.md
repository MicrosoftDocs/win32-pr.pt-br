---
description: O elemento <includeInStartMenuScope> booliana opcional especifica se esse conector de pesquisa deve ser incluído no escopo menu Iniciar pesquisa.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: Elemento includeInStartMenuScope (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60941ef06f3f7220c7bbbae652f5e8256c6256660ea8e9ece2ddd330858958b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937946"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a>Elemento includeInStartMenuScope (esquema do conector de pesquisa)

O elemento <includeInStartMenuScope> booliana opcional especifica se esse conector de pesquisa deve ser incluído no escopo menu Iniciar pesquisa. O valor padrão é verdadeiro para conectores de pesquisa que usam o sistema de arquivos como uma fonte de dados e false para conectores de pesquisa usados por manipuladores de propriedade. Esse elemento não tem nenhum elemento filho e nenhum atributos.

## <a name="syntax"></a>Syntax


```
<!-- includeInStartMenuScope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
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

Se você incluir o conector de pesquisa no escopo menu Iniciar, os usuários poderão pesquisar seu local na caixa de pesquisa no menu Iniciar.

## <a name="example"></a>Exemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



