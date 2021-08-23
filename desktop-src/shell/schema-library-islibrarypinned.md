---
description: o <isLibraryPinned> elemento especifica se essa biblioteca está fixada no painel de navegação no Windows Explorer. Esse elemento é opcional e não tem nenhum elemento filho e nenhum atributo.
title: Elemento isLibraryPinned (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: AD8307E5-5676-4d43-8FEE-695F168F677D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8b5fe37b2a9b31708c1b6a49bd22745b37af8fa8ec21b0b424b7c6da3baaae53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592856"
---
# <a name="islibrarypinned-element-library-schema"></a>Elemento isLibraryPinned (esquema de biblioteca)

o <isLibraryPinned> elemento especifica se essa biblioteca está fixada no painel de navegação no Windows Explorer. Esse elemento é opcional e não tem nenhum elemento filho e nenhum atributo.

## <a name="syntax"></a>Syntax


```
<!-- isLibraryPinned -->
    <xs:element name="isLibraryPinned" type="xs:boolean" default="false" minOccurs="0"/>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                               | Elementos filho |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Comentários

se for true, a biblioteca será fixada no painel de navegação do Windows Explorer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[Elemento searchConnectorDescription (esquema de biblioteca)](schema-library-searchconnectordescription.md)
</dt> </dl>

 

 



