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
# <a name="format-identifieroffset-pair"></a>Identificador de formato/par de deslocamento

A segunda parte do fluxo do conjunto de propriedades contém um par de identificador/deslocamento de formato. O FMTID é o nome do conjunto de propriedades; Ele identifica exclusivamente como interpretar o conteúdo da seção a seguir. O deslocamento é a distância, em bytes, desde o início do fluxo inteiro até o início da seção.

A estrutura a seguir é útil para lidar com o identificador de formato/pares de deslocamento.

``` syntax
typedef struct tagFORMATIDOFFSET 
{ 
    FMTID  fmtid ;     // Name of the section. 
    DWORD  dwOffset ;  // Offset for the section. 
} FORMATIDOFFSET;
```

 

 




