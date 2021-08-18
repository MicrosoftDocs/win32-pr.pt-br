---
title: O length_is atributo
description: O atributo \ size \_ is\ permite que você especifique o tamanho máximo da matriz.
ms.assetid: 577a1efd-2d16-40d6-99bb-998d81ee2f8c
keywords:
- length_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436559961d815adb417d83de5ffa8c06d8497fa0899644411d252c84d6e34ea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924255"
---
# <a name="the-length_is-attribute"></a>O \[ comprimento \_ é \] Attribute

O \[ [**atributo size \_ is**](/windows/desktop/Midl/size-is) \] permite que você especifique o tamanho máximo da matriz. Quando esse é o único atributo, todos os elementos da matriz são transmitidos. Em vez de enviar todos os elementos da matriz, você pode especificar os elementos transmitidos usando \[ [**o atributo \_ length,**](/windows/desktop/Midl/length-is) \] da seguinte forma:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(3.0)
]
interface arraytest
{
  void fArray3([in] short sSize,
               [in] short sLength
               [in, out, size_is(sSize), 
                 length_is(sLength)] char achArray[*]);
}
```

Tamanho descreve a alocação enquanto o comprimento descreve a transmissão. O número de elementos transmitidos sempre deve ser menor ou igual ao número de elementos alocados. O valor associado ao **comprimento \_ é sempre** menor ou igual ao tamanho **\_ é**.

 

 