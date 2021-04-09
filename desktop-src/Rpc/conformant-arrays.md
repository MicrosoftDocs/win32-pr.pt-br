---
title: Matrizes de conformidade
description: O tamanho de uma matriz compatível pode variar ou obedecer cada vez que o cliente a transmite para um procedimento remoto no servidor.
ms.assetid: b4aaec77-b7ae-495d-8666-4702017e675f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f1491354f9cd26ef6100ab8d21f2ace3133f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007999"
---
# <a name="conformant-arrays"></a><span data-ttu-id="0cbff-103">Matrizes de conformidade</span><span class="sxs-lookup"><span data-stu-id="0cbff-103">Conformant Arrays</span></span>

<span data-ttu-id="0cbff-104">O tamanho de uma matriz compatível pode variar ou obedecer cada vez que o cliente a transmite para um procedimento remoto no servidor.</span><span class="sxs-lookup"><span data-stu-id="0cbff-104">The size of a conformant array can vary or conform each time the client passes it to a remote procedure on the server.</span></span> <span data-ttu-id="0cbff-105">A definição de interface no arquivo MIDL do aplicativo permite que o cliente especifique o tamanho da matriz cada vez que invoca o procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="0cbff-105">The interface definition in the application's MIDL file enables the client to specify the size of the array each time it invokes the remote procedure.</span></span> <span data-ttu-id="0cbff-106">Use colchetes vazios ( \[ \] ) ou um asterisco entre colchetes ( \[ \* \] ) na definição da matriz para indicar uma matriz compatível.</span><span class="sxs-lookup"><span data-stu-id="0cbff-106">Use empty square brackets (\[ \]) or an asterisk in the square brackets (\[\*\]) in the array definition to indicate a conformant array.</span></span>

<span data-ttu-id="0cbff-107">O exemplo a seguir contém a definição de um procedimento remoto em uma interface em um arquivo MIDL.</span><span class="sxs-lookup"><span data-stu-id="0cbff-107">The following sample contains the definition of a remote procedure in an interface in a MIDL file.</span></span> <span data-ttu-id="0cbff-108">O cliente especifica o tamanho da matriz que passa para o servidor pelo parâmetro *arrayize*.</span><span class="sxs-lookup"><span data-stu-id="0cbff-108">The client specifies the size of the array that it passes to the server by the parameter *arraySize*.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    MyRemoteProc(
         long lArraySize,
         [size_is(lArraySize)] char achArray[*]
    );

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="0cbff-109">A definição de interface usa o tamanho do atributo MIDL \[ [**\_ é**](/windows/desktop/Midl/size-is) \] especificar o tamanho da matriz que o cliente passa para o servidor.</span><span class="sxs-lookup"><span data-stu-id="0cbff-109">The interface definition uses the MIDL attribute \[[**size\_is**](/windows/desktop/Midl/size-is)\] to specify the size of the array that the client passes to the server.</span></span> <span data-ttu-id="0cbff-110">Se você preferir indicar o valor máximo dos números de índice da matriz, use o atributo \[ [**Max \_**](/windows/desktop/Midl/max-is) \] em vez disso.</span><span class="sxs-lookup"><span data-stu-id="0cbff-110">If you would rather indicate the maximum value of the array's index numbers, use the \[[**max\_is**](/windows/desktop/Midl/max-is)\] attribute instead.</span></span> <span data-ttu-id="0cbff-111">Para obter mais informações sobre esses atributos de MIDL, consulte [atributos de matriz](array-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0cbff-111">For more information on these MIDL attributes, see [Array Attributes](array-attributes.md).</span></span>

<span data-ttu-id="0cbff-112">O fragmento de código a seguir ilustra como um cliente pode invocar o procedimento remoto definido no arquivo MIDL anterior.</span><span class="sxs-lookup"><span data-stu-id="0cbff-112">The following code fragment illustrates how a client might invoke the remote procedure defined in the preceding MIDL file.</span></span>


```C++
long lArrayLength = 20;
char achCharArray[20], achAnotherCharArray[200];

// Code to store 20 chars in achCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achCharArray);

lArrayLength = 200;

// Code to store 200 chars in achAnotherCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achAnotherCharArray);
```



<span data-ttu-id="0cbff-113">Esse fragmento chama o procedimento remoto MyRemoteProc duas vezes.</span><span class="sxs-lookup"><span data-stu-id="0cbff-113">This fragment calls the remote procedure MyRemoteProc twice.</span></span> <span data-ttu-id="0cbff-114">Na primeira invocação, ele passa uma matriz de 20 elementos.</span><span class="sxs-lookup"><span data-stu-id="0cbff-114">On the first invocation it passes an array of 20 elements.</span></span> <span data-ttu-id="0cbff-115">Na segunda chamada, o cliente passa uma matriz de elementos 200.</span><span class="sxs-lookup"><span data-stu-id="0cbff-115">On the second call, the client passes an array of 200 elements.</span></span>

 

 