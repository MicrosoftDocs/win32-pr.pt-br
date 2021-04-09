---
title: O atributo de cadeia de caracteres em matrizes
description: Você pode usar o atributo \ String \ para matrizes de caracteres unidimensionais, matrizes de caracteres largos e matrizes de bytes que representam cadeias de texto.
ms.assetid: 96cebb84-6123-4bf8-b70b-a4f6d48cce52
keywords:
- string
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8bd2f7234b2713b6a7df05cfb5d6ae4c08b2d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084725"
---
# <a name="the-string-attribute-in-arrays"></a><span data-ttu-id="839aa-104">O \[ atributo de cadeia \] de caracteres em matrizes</span><span class="sxs-lookup"><span data-stu-id="839aa-104">The \[string\] Attribute in Arrays</span></span>

<span data-ttu-id="839aa-105">Você pode usar o \[ [](/windows/desktop/Midl/string) \] atributo String para matrizes de caracteres unidimensionais, matrizes de caracteres largos e matrizes de bytes que representam cadeias de texto.</span><span class="sxs-lookup"><span data-stu-id="839aa-105">You can use the \[ [string](/windows/desktop/Midl/string)\] attribute for one-dimensional character arrays, wide-character arrays, and byte arrays that represent text strings.</span></span> <span data-ttu-id="839aa-106">Se você usar o atributo de **\[ cadeia de caracteres \]** , o stub do cliente usará as funções **strlen** ou **wstrlen** da biblioteca C para contar o número de caracteres na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="839aa-106">If you use the **\[string\]** attribute, the client stub uses the C-library functions **strlen** or **wstrlen** to count the number of characters in the string.</span></span> <span data-ttu-id="839aa-107">Para evitar possíveis inconsistências, MIDL não permite que você use o atributo de **\[ cadeia de caracteres \]** ao mesmo tempo que o \[ [primeiro \_ é](/windows/desktop/Midl/first-is), o \] \[ [último \_](/windows/desktop/Midl/last-is) \] , e o \[ [tamanho \_ são](/windows/desktop/Midl/size-is) \] atributos.</span><span class="sxs-lookup"><span data-stu-id="839aa-107">To avoid possible inconsistencies, MIDL does not let you use the **\[string\]** attribute at the same time as the \[ [first\_is](/windows/desktop/Midl/first-is)\], \[ [last\_is](/windows/desktop/Midl/last-is)\], and \[ [size\_is](/windows/desktop/Midl/size-is)\] attributes.</span></span>

<span data-ttu-id="839aa-108">Com cadeias de caracteres terminadas em nulo em C, você deve permitir espaço para o caractere nulo no final da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="839aa-108">With null-terminated strings in C, you must allow space for the null character at the end of the string.</span></span> <span data-ttu-id="839aa-109">Por exemplo, ao declarar uma cadeia de caracteres que irá conter até 80 caracteres, aloque 81 caracteres.</span><span class="sxs-lookup"><span data-stu-id="839aa-109">For example, when declaring a string that will hold up to 80 characters, allocate 81 characters.</span></span> <span data-ttu-id="839aa-110">O arquivo IDL de exemplo a seguir demonstra como declarar matrizes com o atributo de **\[ cadeia de caracteres \]** .</span><span class="sxs-lookup"><span data-stu-id="839aa-110">The following sample IDL file demonstrates how to declare arrays with the **\[string\]** attribute.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(8.0)
]
interface arraytest
{
  void fArray8([in, out, string] char achArray[]);
}
```

 

 