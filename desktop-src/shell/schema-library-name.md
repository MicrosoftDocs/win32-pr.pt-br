---
description: O <name> elemento Especifica o nome dessa biblioteca. Esse elemento é necessário e não tem atributos ou elementos filho.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Elemento Name (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 179d8b4a1f4358ccb441cc38c6c0765a6dc4d9ade8b3c32a1504be2151cfedaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883936"
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

o nome é o nome da biblioteca amigável exibido no Windows Explorer. O nome pode ser especificado em um <dllname> <index> formato, como no exemplo a seguir.


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

 

 
