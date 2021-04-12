---
title: Matrizes variáveis
description: No MIDL, matrizes variadas são fixas em tamanho. Eles permitem que os clientes passem diferentes partes de matrizes de clientes para servidores. O tamanho da parte da matriz pode variar de invocação para invocação. No entanto, o tamanho da matriz geral é fixo.
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b2d79ee37f3e366bbf232b362306f78ca6ada4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454255"
---
# <a name="varying-arrays"></a><span data-ttu-id="4570b-106">Matrizes variáveis</span><span class="sxs-lookup"><span data-stu-id="4570b-106">Varying Arrays</span></span>

<span data-ttu-id="4570b-107">No MIDL, matrizes variadas são fixas em tamanho.</span><span class="sxs-lookup"><span data-stu-id="4570b-107">In MIDL, varying arrays are fixed in size.</span></span> <span data-ttu-id="4570b-108">Eles permitem que os clientes passem diferentes partes de matrizes de clientes para servidores.</span><span class="sxs-lookup"><span data-stu-id="4570b-108">They allow clients to pass different portions of arrays from clients to servers.</span></span> <span data-ttu-id="4570b-109">O tamanho da parte da matriz pode variar de invocação para invocação.</span><span class="sxs-lookup"><span data-stu-id="4570b-109">The size of the array portion can vary from invocation to invocation.</span></span> <span data-ttu-id="4570b-110">No entanto, o tamanho da matriz geral é fixo.</span><span class="sxs-lookup"><span data-stu-id="4570b-110">However, the size of the overall array is fixed.</span></span>

<span data-ttu-id="4570b-111">Por exemplo, o exemplo a seguir mostra a definição de um procedimento remoto em uma interface em um arquivo MIDL.</span><span class="sxs-lookup"><span data-stu-id="4570b-111">For instance, the following example shows the definition of a remote procedure in an interface in a MIDL file.</span></span> <span data-ttu-id="4570b-112">O tamanho da matriz que o cliente passa para o servidor é fixo pelo tamanho da matriz constante \_ .</span><span class="sxs-lookup"><span data-stu-id="4570b-112">The size of the array that the client passes to the server is fixed by the constant ARRAY\_SIZE.</span></span> <span data-ttu-id="4570b-113">A interface especifica a parte da matriz que o cliente passa para o servidor nos parâmetros firstelement e chunkSize.</span><span class="sxs-lookup"><span data-stu-id="4570b-113">The interface specifies the portion of the array that the client passes to the server in the parameters firstElement and chunkSize.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(
        [in] long lFirstElement,
        [in] long lChunkSize,
        [in, first_is(lFirstElement), 
          length_is(lChunkSize)] char achArray[ARRAY_SIZE]
    );

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="4570b-114">A definição de interface usa o atributo MIDL \[ [**primeiro \_ é**](/windows/desktop/Midl/first-is) \] especificar o número de índice do primeiro elemento na parte da matriz que o cliente passa para o servidor.</span><span class="sxs-lookup"><span data-stu-id="4570b-114">The interface definition uses the MIDL attribute \[[**first\_is**](/windows/desktop/Midl/first-is)\] to specify the index number of the first element in the portion of the array that the client passes to the server.</span></span> <span data-ttu-id="4570b-115">O \[ [**tamanho \_ é**](/windows/desktop/Midl/length-is) \] atributo especifica o número total de elementos de matriz que o cliente passa.</span><span class="sxs-lookup"><span data-stu-id="4570b-115">The \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute specifies the total number of array elements that the client passes.</span></span> <span data-ttu-id="4570b-116">Para obter mais informações sobre esses atributos de MIDL, consulte [atributos de matriz](array-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="4570b-116">For more information on these MIDL attributes, see [Array Attributes](array-attributes.md).</span></span>

<span data-ttu-id="4570b-117">O fragmento de código a seguir ilustra como um cliente pode invocar o procedimento remoto definido no arquivo MIDL anterior.</span><span class="sxs-lookup"><span data-stu-id="4570b-117">The following code fragment illustrates how a client might invoke the remote procedure defined in the preceding MIDL file.</span></span>


```C++
long lFirstArrayElementNumber = 20;
long lTotalElementsPassed = 100;
char achCharArray[ARRAY_SIZE];

// Code to store chars in the array goes here.

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);

firstArrayElementNumber = 120;
totalElementsPassed = 200;

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);
```



<span data-ttu-id="4570b-118">Esse fragmento chama o procedimento remoto MyRemoteProc duas vezes.</span><span class="sxs-lookup"><span data-stu-id="4570b-118">This fragment calls the remote procedure MyRemoteProc twice.</span></span> <span data-ttu-id="4570b-119">Na primeira invocação, ele passa os elementos de matriz numerados 20 a 119, conforme indicado pelos valores nas variáveis firstArrayElementNumber e totalElementsPassed.</span><span class="sxs-lookup"><span data-stu-id="4570b-119">On the first invocation it passes the array elements numbered 20 through 119, as indicated by the values in the variables firstArrayElementNumber and totalElementsPassed.</span></span> <span data-ttu-id="4570b-120">Na segunda chamada, o cliente passa os elementos de matriz numerados de 120 a 319.</span><span class="sxs-lookup"><span data-stu-id="4570b-120">On the second call, the client passes the array elements numbered 120 through 319.</span></span>

 

 