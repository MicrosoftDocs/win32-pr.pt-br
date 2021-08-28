---
description: O elemento &lt; de domínio opcional especifica a URL do serviço de pesquisa usado por esse conector de &gt; pesquisa. Ele é exibido no painel de detalhes. Esse elemento não tem nenhum elemento filho e nenhum atributos.
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: Elemento domain (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd84ffa2ee5bcc5f5f6dcdb93c9abbd12c57bd96
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882477"
---
# <a name="domain-element-search-connector-schema"></a>Elemento domain (esquema do conector de pesquisa)

O elemento &lt; de domínio opcional especifica a URL do serviço de pesquisa usado por esse conector de &gt; pesquisa. Ele é exibido no painel de detalhes. Esse elemento não tem nenhum elemento filho e nenhum atributos.

## <a name="syntax"></a>Syntax


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
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

A URL deve ser o domínio de nível superior para o provedor de pesquisa. Por exemplo, https://www.example.com.

## <a name="example"></a>Exemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 



