---
title: Os atributos first_is e last_is
description: Você pode determinar o número de elementos transmitidos especificando o primeiro e o último elementos.
ms.assetid: bd4dcf42-64a7-4b05-ac55-be77c381eb2e
keywords:
- first_is
- last_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159a2696db8e175f921b797176baaa8f3aa0263c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294453"
---
# <a name="the-first_is-and-last_is-attributes"></a>O \[ primeiro \_ é \] e o \[ último \_ são \] atributos

Você pode determinar o número de elementos transmitidos especificando o primeiro e o último elementos. Use o \[ [**primeiro \_**](/windows/desktop/Midl/first-is) \] e o \[ [**último \_ são**](/windows/desktop/Midl/last-is) \] atributos, conforme mostrado:

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

 

 