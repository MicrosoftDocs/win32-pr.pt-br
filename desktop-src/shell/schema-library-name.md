---
description: O &lt; elemento name especifica o nome dessa &gt; biblioteca. Esse elemento é necessário e não tem atributos ou elementos filho.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Elemento name (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d32b6d929a58f19cc2b87a79af846d22fc0ebda
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880852"
---
# <a name="name-element-library-schema"></a>Elemento name (esquema de biblioteca)

O &lt; elemento name especifica o nome dessa &gt; biblioteca. Esse elemento é necessário e não tem atributos ou elementos filho.

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

O nome é o nome amigável da biblioteca que é exibido no Windows Explorer. O nome pode ser especificado em um &lt; dllname &gt; , formato de &lt; &gt; índice, como no exemplo a seguir.


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

 

 
