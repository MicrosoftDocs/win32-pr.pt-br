---
description: O <iconReference> elemento especifica um ícone personalizado para esta biblioteca. Esse elemento é opcional e não tem atributos ou elementos filho.
title: Elemento iconReference (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f307ecd4fa523cc28881164869dca3329dfd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988850"
---
# <a name="iconreference-element-library-schema"></a>Elemento iconReference (esquema de biblioteca)

O <iconReference> elemento especifica um ícone personalizado para esta biblioteca. Esse elemento é opcional e não tem atributos ou elementos filho.

## <a name="syntax"></a>Syntax


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                               | Elementos filho |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Comentários

A referência do ícone deve ser especificada em um formato adequado para a função [**PathParseIconLocation**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) . Por exemplo: `ModuleFileName,IconResourceIndex`.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Elemento FolderType (esquema de biblioteca)](schema-library-foldertype.md)
</dt> <dt>

[Elemento isLibraryPinned (esquema de biblioteca)](schema-library-islibrarypinned.md)
</dt> <dt>

[Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[Elemento Name (esquema de biblioteca)](schema-library-name.md)
</dt> <dt>

[Elemento OwnerId (esquema de biblioteca)](schema-library-ownersid.md)
</dt> <dt>

[Elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md)
</dt> <dt>

[Elemento searchConnectorDescription (esquema de biblioteca)](schema-library-searchconnectordescription.md)
</dt> <dt>

[Elemento searchConnectorDescriptionList (esquema de biblioteca)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[Elemento templateInfo (esquema de biblioteca)](schema-library-templateinfo.md)
</dt> <dt>

[Elemento Version (esquema de biblioteca)](schema-library-version.md)
</dt> </dl>

 

 



