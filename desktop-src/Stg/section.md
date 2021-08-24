---
title: Seção
description: A seção é a terceira parte do fluxo do conjunto de propriedades e contém os valores reais do conjunto de propriedades.
ms.assetid: cb392072-116e-4dca-bd70-5f82f86d8c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71796bca5dd2801e437ecfffe663f2702abc4c202d721ecbda8a9b95656e40a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682796"
---
# <a name="section"></a>Seção

A seção é a terceira parte do fluxo do conjunto de propriedades e contém os valores reais do conjunto de propriedades.

Uma seção contém:

-   Contagem de byte para a seção que é inclusiva da própria contagem de byte.
-   Matriz de pares de ID de propriedade/deslocamento de 32 bits.
-   Matriz de pares indicadores de tipo de propriedade/valor.

Deslocamentos são a distância do início da seção até o início do par de propriedades (tipo, valor). Isso permite que uma seção seja copiada como uma matriz de bytes sem nenhuma tradução da estrutura interna.

As pseudo-estruturas a seguir ilustram o formato de uma seção.

``` syntax
typedef struct tagPROPERTYSECTIONHEADER 
{ 
    DWORD  cbSection ;    // Size of Section 
    DWORD  cProperties ;  // Count of Properties in section 
} PROPERTYSECTIONHEADER; 
 
typedef struct tagPROPERTYIDOFFSET 
{ 
    DWORD  propid;    // Name of property 
    DWORD  dwOffset;  // Offset from start of section to property 
} PROPERTYIDOFFSET; 
 
typedef struct tagSERIALIZEDPROPERTYVALUE 
{ 
    DWORD  dwType;    // Property Type 
    BYTE   rgb[];     // Property Value 
} SERIALIZEDPROPERTYVALUE ;
```

 

 




