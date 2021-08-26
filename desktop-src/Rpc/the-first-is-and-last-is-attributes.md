---
title: Os atributos first_is e last_is dados
description: Você pode determinar o número de elementos transmitidos especificando o primeiro e o último elementos.
ms.assetid: bd4dcf42-64a7-4b05-ac55-be77c381eb2e
keywords:
- first_is
- last_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16c30c2e7e6689ba2a61f7f5e694a5b29f39af5cadcf7fa2ca2f51e14e1f3457
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017136"
---
# <a name="the-first_is-and-last_is-attributes"></a>O \[ primeiro é e o último é \_ \] \[ \_ \] Atributos

Você pode determinar o número de elementos transmitidos especificando o primeiro e o último elementos. Use o \[ [**primeiro é \_ e**](/windows/desktop/Midl/first-is) \] o último \[ [**\_ é**](/windows/desktop/Midl/last-is) \] atributos, conforme mostrado:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(4.0)
]
interface arraytest
{

  void fArray4([in]               short sSize,
               [in]               short sLast,
               [in]               short sFirst,
               [in, 
                out,
                size_is(sSize),
                first_is(sFirst),
                last_is(sLast)]   char achArray[]) ;
}
```

 

 