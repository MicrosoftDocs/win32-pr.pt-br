---
description: O &lt; elemento folderType &gt; especifica GUID para o tipo de pasta. Esse elemento será necessário se o &lt; elemento templateInfo &gt; existir. Ele não tem atributos e nenhum elemento filho.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: Elemento folderType (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b693a1ff7007e6d63e108d16abe77ee421b3821a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882469"
---
# <a name="foldertype-element-search-connector-schema"></a>Elemento folderType (esquema do conector de pesquisa)

O &lt; elemento folderType &gt; especifica GUID para o tipo de pasta. Esse elemento será necessário se o &lt; elemento templateInfo &gt; existir. Ele não tem atributos e nenhum elemento filho.

## <a name="syntax"></a>Syntax


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                                         | Elementos filho |
|----------------------------------------------------------------------------------------|----------------|
| [Elemento templateInfo (esquema do conector de pesquisa)](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a>Comentários

O GUID padrão é {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, um tipo de pasta geral para conectores de pesquisa federada (OpenSearch).

## <a name="example-of-a-foldertype-element"></a>Exemplo de um elemento folderType


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



