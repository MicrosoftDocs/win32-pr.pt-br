---
description: O <isLibraryPinned> elemento especifica se essa biblioteca está fixada no painel de navegação no Windows Explorer. Esse elemento é opcional e não tem nenhum elemento filho e nenhum atributo.
title: Elemento isLibraryPinned (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: AD8307E5-5676-4d43-8FEE-695F168F677D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 743ddc6df6b4a1a0df44e19bf063e417fc052e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989108"
---
# <a name="islibrarypinned-element-library-schema"></a>Elemento isLibraryPinned (esquema de biblioteca)

O <isLibraryPinned> elemento especifica se essa biblioteca está fixada no painel de navegação no Windows Explorer. Esse elemento é opcional e não tem nenhum elemento filho e nenhum atributo.

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

Se for true, a biblioteca será fixada no painel de navegação do Windows Explorer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[Elemento searchConnectorDescription (esquema de biblioteca)](schema-library-searchconnectordescription.md)
</dt> </dl>

 

 



