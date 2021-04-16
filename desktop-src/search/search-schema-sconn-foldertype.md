---
description: O <folderType> elemento Especifica o GUID para o tipo de pasta. Esse elemento será necessário se o <templateInfo> elemento existir. Ele não tem nenhum atributo e nenhum elemento filho.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: Elemento FolderType (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7d2a9e7f83dbe225427a8370cd8f5e948a46cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460980"
---
# <a name="foldertype-element-search-connector-schema"></a>Elemento FolderType (esquema do conector de pesquisa)

O <folderType> elemento Especifica o GUID para o tipo de pasta. Esse elemento será necessário se o <templateInfo> elemento existir. Ele não tem nenhum atributo e nenhum elemento filho.

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

## <a name="example-of-a-foldertype-element"></a>Exemplo de um elemento FolderType


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



