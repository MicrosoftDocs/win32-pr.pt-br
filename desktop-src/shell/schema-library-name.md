---
description: O <name> elemento Especifica o nome dessa biblioteca. Esse elemento é necessário e não tem atributos ou elementos filho.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Elemento Name (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d38baa32587ee04c62c8c3086d5353e8eed9e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989107"
---
# <a name="name-element-library-schema"></a>Elemento Name (esquema de biblioteca)

O <name> elemento Especifica o nome dessa biblioteca. Esse elemento é necessário e não tem atributos ou elementos filho.

## <a name="syntax"></a>Syntax

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                               | Elementos filho |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Comentários

O nome é o nome da biblioteca amigável que é exibido no Windows Explorer. O nome pode ser especificado em um <dllname> <index> formato, como no exemplo a seguir.


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[Esquema de descrição do conector de pesquisa](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
