---
title: Combinando atributos de matriz
description: Os atributos de campo podem ser fornecidos em várias combinações, contanto que o stub possa usar as informações para determinar o tamanho da matriz e o número de bytes a serem transmitidos para o servidor.
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc60777caeb3950e37fe167fe09ecc181d88b8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105759345"
---
# <a name="combining-array-attributes"></a><span data-ttu-id="7fe28-103">Combinando atributos de matriz</span><span class="sxs-lookup"><span data-stu-id="7fe28-103">Combining Array Attributes</span></span>

<span data-ttu-id="7fe28-104">Os atributos de campo podem ser fornecidos em várias combinações, contanto que o stub possa usar as informações para determinar o tamanho da matriz e o número de bytes a serem transmitidos para o servidor.</span><span class="sxs-lookup"><span data-stu-id="7fe28-104">Field attributes can be supplied in various combinations as long as the stub can use the information to determine the size of the array and the number of bytes to transmit to the server.</span></span> <span data-ttu-id="7fe28-105">As relações entre os atributos são definidas usando as seguintes fórmulas:</span><span class="sxs-lookup"><span data-stu-id="7fe28-105">The relationships between the attributes are defined using the following formulas:</span></span>

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

<span data-ttu-id="7fe28-106">Os valores associados aos atributos devem obedecer a várias regras de senso comum com base nessas fórmulas.</span><span class="sxs-lookup"><span data-stu-id="7fe28-106">The values associated with the attributes must obey several common-sense rules based on those formulas.</span></span> <span data-ttu-id="7fe28-107">Essas regras são:</span><span class="sxs-lookup"><span data-stu-id="7fe28-107">These rules are:</span></span>

-   <span data-ttu-id="7fe28-108">Não especifique um \[ [**primeiro \_**](/windows/desktop/Midl/first-is) \] valor de índice menor que zero ou um \[ [**último \_**](/windows/desktop/Midl/last-is) \] valor maior que o \[ [**máximo \_ é**](/windows/desktop/Midl/max-is) \] .</span><span class="sxs-lookup"><span data-stu-id="7fe28-108">Do not specify a \[[**first\_is**](/windows/desktop/Midl/first-is)\] index value smaller than zero or a \[[**last\_is**](/windows/desktop/Midl/last-is)\] value greater than \[[**max\_is**](/windows/desktop/Midl/max-is)\].</span></span>
-   <span data-ttu-id="7fe28-109">Não especifique um tamanho negativo para uma matriz.</span><span class="sxs-lookup"><span data-stu-id="7fe28-109">Do not specify a negative size for an array.</span></span> <span data-ttu-id="7fe28-110">Defina o primeiro e o último elementos para que eles resultem em um valor de comprimento igual ou maior que zero.</span><span class="sxs-lookup"><span data-stu-id="7fe28-110">Define the first and last elements so that they result in a length value of zero or greater.</span></span> <span data-ttu-id="7fe28-111">Defina o \[ [**valor \_ máximo**](/windows/desktop/Midl/max-is) \] para que o tamanho seja zero ou maior.</span><span class="sxs-lookup"><span data-stu-id="7fe28-111">Define the \[[**max\_is**](/windows/desktop/Midl/max-is)\] value so that the size is zero or greater.</span></span> <span data-ttu-id="7fe28-112">Se MIDL foi invocado com a opção de verificação de limites [**/Error**](/windows/desktop/Midl/-error) \_ , o stub gerará uma exceção quando o tamanho for menor que zero ou o comprimento transmitido for menor que zero.</span><span class="sxs-lookup"><span data-stu-id="7fe28-112">If MIDL was invoked with the [**/error**](/windows/desktop/Midl/-error) bounds\_check option, then the stub raises an exception when the size is less than zero, or the transmitted length is less than zero.</span></span>
-   <span data-ttu-id="7fe28-113">Não use o \[ [**\_ comprimento**](/windows/desktop/Midl/length-is) \] e o \[ [**último \_ são**](/windows/desktop/Midl/last-is) \] atributos ao mesmo tempo, nem o \[ **tamanho \_** \] e o \[ **último \_ são** \] atributos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="7fe28-113">Do not use the \[[**length\_is**](/windows/desktop/Midl/length-is)\] and \[[**last\_is**](/windows/desktop/Midl/last-is)\] attributes at the same time, nor the \[**size\_is**\] and \[**last\_is**\] attributes at the same time.</span></span>

<span data-ttu-id="7fe28-114">Devido à relação de fechamento em C entre matrizes e ponteiros, MIDL também permite declarar matrizes em listas de parâmetros usando a notação de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="7fe28-114">Because of the close relationship in C between arrays and pointers, MIDL also lets you declare arrays in parameter lists using pointer notation.</span></span> <span data-ttu-id="7fe28-115">MIDL trata um parâmetro que é um ponteiro para um tipo como uma matriz desse tipo se o parâmetro tiver qualquer um dos atributos normalmente associados a matrizes.</span><span class="sxs-lookup"><span data-stu-id="7fe28-115">MIDL treats a parameter that is a pointer to a type as an array of that type if the parameter has any of the attributes commonly associated with arrays.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45)
  version(6.0) 
]
interface arraytest
{
  void fArray6([in] short sSize, 
               [in, out, size_is(sSize)] char * p1);
  void fArray7([in] short sSize, 
               [in, out, size_is(sSize)] char achArray[]);
}
```

<span data-ttu-id="7fe28-116">No exemplo anterior, os parâmetros de ponteiro e de matriz nas funções fArray6 e fArray7 são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="7fe28-116">In the preceding example, the array and pointer parameters in the functions fArray6 and fArray7 are equivalent.</span></span>

 

 