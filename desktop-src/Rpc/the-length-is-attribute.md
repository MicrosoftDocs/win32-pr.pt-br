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
# <a name="the-length_is-attribute"></a><span data-ttu-id="5e17d-104">O \[ comprimento \_ é o \] atributo</span><span class="sxs-lookup"><span data-stu-id="5e17d-104">The \[length\_is\] Attribute</span></span>

<span data-ttu-id="5e17d-105">O \[ atributo [**Size \_ is**](/windows/desktop/Midl/size-is) \] permite que você especifique o tamanho máximo da matriz.</span><span class="sxs-lookup"><span data-stu-id="5e17d-105">The \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute lets you specify the maximum size of the array.</span></span> <span data-ttu-id="5e17d-106">Quando esse for o único atributo, todos os elementos da matriz serão transmitidos.</span><span class="sxs-lookup"><span data-stu-id="5e17d-106">When this is the only attribute, all elements of the array are transmitted.</span></span> <span data-ttu-id="5e17d-107">Em vez de enviar todos os elementos da matriz, você pode especificar os elementos transmitidos usando o \[ [**comprimento \_ é**](/windows/desktop/Midl/length-is) o \] atributo, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5e17d-107">Instead of sending all elements of the array, you can specify the transmitted elements using the \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute, as follows:</span></span>

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

<span data-ttu-id="5e17d-108">Tamanho descreve a alocação enquanto o comprimento descreve a transmissão.</span><span class="sxs-lookup"><span data-stu-id="5e17d-108">Size describes allocation while length describes transmission.</span></span> <span data-ttu-id="5e17d-109">O número de elementos transmitidos deve ser sempre menor ou igual ao número de elementos alocados.</span><span class="sxs-lookup"><span data-stu-id="5e17d-109">The number of elements transmitted must always be less than or equal to the number of elements allocated.</span></span> <span data-ttu-id="5e17d-110">O valor associado ao **comprimento \_** é sempre menor ou igual ao **tamanho \_**.</span><span class="sxs-lookup"><span data-stu-id="5e17d-110">The value associated with **length\_is** is always less than or equal to **size\_is**.</span></span>

 

 