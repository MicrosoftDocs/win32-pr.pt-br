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
# <a name="section"></a><span data-ttu-id="aaa10-103">Seção</span><span class="sxs-lookup"><span data-stu-id="aaa10-103">Section</span></span>

<span data-ttu-id="aaa10-104">A seção é a terceira parte do fluxo do conjunto de propriedades e contém os valores reais do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="aaa10-104">The section is the third part of the property set stream and contains the actual property set values.</span></span>

<span data-ttu-id="aaa10-105">Uma seção contém:</span><span class="sxs-lookup"><span data-stu-id="aaa10-105">A section contains:</span></span>

-   <span data-ttu-id="aaa10-106">Contagem de bytes para a seção que é inclusiva da contagem de bytes em si.</span><span class="sxs-lookup"><span data-stu-id="aaa10-106">Byte count for the section which is inclusive of the byte count itself.</span></span>
-   <span data-ttu-id="aaa10-107">Matriz de pares de ID/deslocamento de propriedade de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="aaa10-107">Array of 32-bit Property ID/Offset pairs.</span></span>
-   <span data-ttu-id="aaa10-108">Matriz de pares de valores/indicadores de tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="aaa10-108">Array of property Type Indicators/Value pairs.</span></span>

<span data-ttu-id="aaa10-109">Os deslocamentos são a distância desde o início da seção até o início do par de propriedade (tipo, valor).</span><span class="sxs-lookup"><span data-stu-id="aaa10-109">Offsets are the distance from the start of the section to the start of the property (type, value) pair.</span></span> <span data-ttu-id="aaa10-110">Isso permite que uma seção seja copiada como uma matriz de bytes sem qualquer tradução da estrutura interna.</span><span class="sxs-lookup"><span data-stu-id="aaa10-110">This allows a section to be copied as an array of bytes without any translation of internal structure.</span></span>

<span data-ttu-id="aaa10-111">As pseudovariáveis a seguir ilustram o formato de uma seção.</span><span class="sxs-lookup"><span data-stu-id="aaa10-111">The following pseudo-structures illustrate the format of a section.</span></span>

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

 

 




