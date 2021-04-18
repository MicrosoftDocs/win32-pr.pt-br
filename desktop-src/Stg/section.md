---
title: Seção
description: A seção é a terceira parte do fluxo do conjunto de propriedades e contém os valores reais do conjunto de propriedades.
ms.assetid: cb392072-116e-4dca-bd70-5f82f86d8c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f51891d14a9690e295379b7bcf619fe0fbe19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105769177"
---
# <a name="section"></a>Seção

A seção é a terceira parte do fluxo do conjunto de propriedades e contém os valores reais do conjunto de propriedades.

Uma seção contém:

-   Contagem de bytes para a seção que é inclusiva da contagem de bytes em si.
-   Matriz de pares de ID/deslocamento de propriedade de 32 bits.
-   Matriz de pares de valores/indicadores de tipo de propriedade.

Os deslocamentos são a distância desde o início da seção até o início do par de propriedade (tipo, valor). Isso permite que uma seção seja copiada como uma matriz de bytes sem qualquer tradução da estrutura interna.

As pseudovariáveis a seguir ilustram o formato de uma seção.

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

 

 




