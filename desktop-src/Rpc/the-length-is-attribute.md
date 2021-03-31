---
title: O atributo length_is
description: O atributo \ Size \_ is \ permite que você especifique o tamanho máximo da matriz.
ms.assetid: 577a1efd-2d16-40d6-99bb-998d81ee2f8c
keywords:
- length_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f49ad63b2546d39dcc00d251f39143b7eec354c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641722"
---
# <a name="the-length_is-attribute"></a>O \[ comprimento \_ é o \] atributo

O \[ atributo [**Size \_ is**](/windows/desktop/Midl/size-is) \] permite que você especifique o tamanho máximo da matriz. Quando esse for o único atributo, todos os elementos da matriz serão transmitidos. Em vez de enviar todos os elementos da matriz, você pode especificar os elementos transmitidos usando o \[ [**comprimento \_ é**](/windows/desktop/Midl/length-is) o \] atributo, da seguinte maneira:

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

Tamanho descreve a alocação enquanto o comprimento descreve a transmissão. O número de elementos transmitidos deve ser sempre menor ou igual ao número de elementos alocados. O valor associado ao **comprimento \_** é sempre menor ou igual ao **tamanho \_**.

 

 