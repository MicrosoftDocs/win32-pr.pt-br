---
description: O <version> elemento Especifica a versão de conteúdo desta biblioteca. Este elemento não tem atributos nem elementos filho.
ms.assetid: 77FD5EF6-6B6F-48e1-973F-AC069F729613
title: Elemento Version (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7b16a6078a16f4ebbe5e995503114996572f1b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967474"
---
# <a name="version-element-library-schema"></a>Elemento Version (esquema de biblioteca)

O <version> elemento Especifica a versão de conteúdo desta biblioteca. Este elemento não tem atributos nem elementos filho.

## <a name="syntax"></a>Syntax

``` syntax
<!-- version -->
<xs:element name="version" type="xs:int" minOccurs="0"/>
```

## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                               | Elementos filho |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) | Nenhum           |



 

## <a name="remarks"></a>Comentários

A versão de conteúdo da biblioteca é diferente da versão do formato de arquivo da biblioteca ( \* . Library-MS). A versão de formato de arquivo da biblioteca é especificada no [namespace](library-schema-entry.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Esquema de descrição da biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de descrição do conector de pesquisa](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
