---
title: Identificador de formato/par de deslocamento
description: A segunda parte do fluxo do conjunto de propriedades contém um par de identificador/deslocamento de formato.
ms.assetid: cc3a748d-e81c-45da-b04f-ea986158a4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f80a85175278b92fedbfd7b2d50d94007b7e4a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292074"
---
# <a name="format-identifieroffset-pair"></a><span data-ttu-id="422aa-103">Identificador de formato/par de deslocamento</span><span class="sxs-lookup"><span data-stu-id="422aa-103">Format Identifier/Offset Pair</span></span>

<span data-ttu-id="422aa-104">A segunda parte do fluxo do conjunto de propriedades contém um par de identificador/deslocamento de formato.</span><span class="sxs-lookup"><span data-stu-id="422aa-104">The second part of the property set stream contains one Format Identifier/Offset Pair.</span></span> <span data-ttu-id="422aa-105">O FMTID é o nome do conjunto de propriedades; Ele identifica exclusivamente como interpretar o conteúdo da seção a seguir.</span><span class="sxs-lookup"><span data-stu-id="422aa-105">The FMTID is the name of the property set; it uniquely identifies how to interpret the contents of the following section.</span></span> <span data-ttu-id="422aa-106">O deslocamento é a distância, em bytes, desde o início do fluxo inteiro até o início da seção.</span><span class="sxs-lookup"><span data-stu-id="422aa-106">The Offset is the distance, in bytes, from the start of the whole stream to where the section begins.</span></span>

<span data-ttu-id="422aa-107">A estrutura a seguir é útil para lidar com o identificador de formato/pares de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="422aa-107">The following structure is helpful in handling Format Identifier/Offset Pairs.</span></span>

``` syntax
typedef struct tagFORMATIDOFFSET 
{ 
    FMTID  fmtid ;     // Name of the section. 
    DWORD  dwOffset ;  // Offset for the section. 
} FORMATIDOFFSET;
```

 

 




