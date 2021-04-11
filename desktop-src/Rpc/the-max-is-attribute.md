---
title: O atributo max_is
description: Você pode especificar os limites válidos dos números de índice de uma matriz usando o atributo \ Max \_ is \.
ms.assetid: b629e3cf-544d-47ee-8f8f-b049f693897c
keywords:
- max_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8901f952a55de6b81143b0e615c878d8599fb354
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162389"
---
# <a name="the-max_is-attribute"></a><span data-ttu-id="1245f-104">O \[ \_ atributo Max é \]</span><span class="sxs-lookup"><span data-stu-id="1245f-104">The \[max\_is\] Attribute</span></span>

<span data-ttu-id="1245f-105">Você pode especificar os limites válidos dos números de índice de uma matriz usando o atributo \[ [**Max \_ is**](/windows/desktop/Midl/max-is) \] .</span><span class="sxs-lookup"><span data-stu-id="1245f-105">You can specify the valid bounds of the index numbers of an array using the \[[**max\_is**](/windows/desktop/Midl/max-is)\] attribute.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(5.0)
]
interface arraytest
{
  void fArray5([in] short sMax,
               [in, out, max_is(sMax)]  char achArray[]);
}
```

 

 