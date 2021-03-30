---
title: Atributos de matriz
description: Há uma relação de fechamento entre as matrizes e os ponteiros na linguagem C.
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed669a2a81528afa84b41a1be25a0c84f70fbe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641633"
---
# <a name="array-attributes"></a><span data-ttu-id="5ce52-103">Atributos de matriz</span><span class="sxs-lookup"><span data-stu-id="5ce52-103">Array Attributes</span></span>

<span data-ttu-id="5ce52-104">Há uma relação de fechamento entre as matrizes e os ponteiros na linguagem C.</span><span class="sxs-lookup"><span data-stu-id="5ce52-104">There is a close relationship between arrays and pointers in the C language.</span></span> <span data-ttu-id="5ce52-105">Quando passado como um parâmetro para uma função, um nome de matriz é tratado como um ponteiro para o primeiro elemento da matriz, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="5ce52-105">When passed as a parameter to a function, an array name is treated as a pointer to the first element of the array, as shown in the following example:</span></span>


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



<span data-ttu-id="5ce52-106">Em uma chamada local, você pode usar o parâmetro pointer para março por meio da memória e examinar o conteúdo de outros endereços:</span><span class="sxs-lookup"><span data-stu-id="5ce52-106">In a local call, you can use the pointer parameter to march through memory and examine the contents of other addresses:</span></span>


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



<span data-ttu-id="5ce52-107">Quando um cliente passa um ponteiro para um procedimento remoto, o stub do cliente transmite o ponteiro e os dados para os quais ele aponta.</span><span class="sxs-lookup"><span data-stu-id="5ce52-107">When a client passes a pointer to a remote procedure, the client stub transmits both the pointer and the data it points to.</span></span> <span data-ttu-id="5ce52-108">A menos que o ponteiro seja restrito aos seus dados correspondentes, toda a memória do cliente deve ser transmitida a cada chamada remota.</span><span class="sxs-lookup"><span data-stu-id="5ce52-108">Unless the pointer is restricted to its corresponding data, all the client's memory must be transmitted with every remote call.</span></span> <span data-ttu-id="5ce52-109">Ao impor uma tipagem forte na definição da interface, o MIDL limita o processamento do stub do cliente aos dados que corresponde ao ponteiro especificado.</span><span class="sxs-lookup"><span data-stu-id="5ce52-109">By enforcing strong typing in the interface definition, MIDL limits client-stub processing to the data that corresponds to the specified pointer.</span></span>

<span data-ttu-id="5ce52-110">O tamanho da matriz e o intervalo de elementos de matriz transmitidos para o computador remoto podem ser constantes ou variáveis.</span><span class="sxs-lookup"><span data-stu-id="5ce52-110">The size of the array and the range of array elements transmitted to the remote computer can be constant or variable.</span></span> <span data-ttu-id="5ce52-111">Quando esses valores são variáveis e, portanto, determinados em tempo de execução, você deve usar atributos no arquivo IDL para especificar quantos elementos de matriz devem ser transmitidos.</span><span class="sxs-lookup"><span data-stu-id="5ce52-111">When these values are variable, and thus determined at run time, you must use attributes in the IDL file to specify how many array elements to transmit.</span></span> <span data-ttu-id="5ce52-112">Os seguintes atributos de MIDL dão suporte a limites de matriz.</span><span class="sxs-lookup"><span data-stu-id="5ce52-112">The following MIDL attributes support array bounds.</span></span>



| <span data-ttu-id="5ce52-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="5ce52-113">Attribute</span></span>                             | <span data-ttu-id="5ce52-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ce52-114">Description</span></span>                                             | <span data-ttu-id="5ce52-115">Padrão</span><span class="sxs-lookup"><span data-stu-id="5ce52-115">Default</span></span> |
|---------------------------------------|---------------------------------------------------------|---------|
| <span data-ttu-id="5ce52-116">\[[ **primeiro \_ é**](/windows/desktop/Midl/first-is)\]</span><span class="sxs-lookup"><span data-stu-id="5ce52-116">\[ [**first\_is**](/windows/desktop/Midl/first-is)\]</span></span>   | <span data-ttu-id="5ce52-117">Índice do primeiro elemento de matriz transmitido.</span><span class="sxs-lookup"><span data-stu-id="5ce52-117">Index of the first array element transmitted.</span></span>           | <span data-ttu-id="5ce52-118">0</span><span class="sxs-lookup"><span data-stu-id="5ce52-118">0</span></span>       |
| <span data-ttu-id="5ce52-119">\[[ **último \_ é**](/windows/desktop/Midl/last-is)\]</span><span class="sxs-lookup"><span data-stu-id="5ce52-119">\[ [**last\_is**](/windows/desktop/Midl/last-is)\]</span></span>     | <span data-ttu-id="5ce52-120">Índice do último elemento de matriz transmitido.</span><span class="sxs-lookup"><span data-stu-id="5ce52-120">Index of the last array element transmitted.</span></span>            | \-      |
| <span data-ttu-id="5ce52-121">\[[ **comprimento \_ é**](/windows/desktop/Midl/length-is)\]</span><span class="sxs-lookup"><span data-stu-id="5ce52-121">\[ [**length\_is**](/windows/desktop/Midl/length-is)\]</span></span> | <span data-ttu-id="5ce52-122">Número total de elementos de matriz transmitidos.</span><span class="sxs-lookup"><span data-stu-id="5ce52-122">Total number of array elements transmitted.</span></span>             | \-      |
| <span data-ttu-id="5ce52-123">\[[ **máximo \_ é**](/windows/desktop/Midl/max-is)\]</span><span class="sxs-lookup"><span data-stu-id="5ce52-123">\[ [**max\_is**](/windows/desktop/Midl/max-is)\]</span></span>       | <span data-ttu-id="5ce52-124">Valor de índice de matriz mais alto válido.</span><span class="sxs-lookup"><span data-stu-id="5ce52-124">Highest valid array index value.</span></span>                        | \-      |
| <span data-ttu-id="5ce52-125">\[[ **mín. \_ é**](/windows/desktop/Midl/min-is)\]</span><span class="sxs-lookup"><span data-stu-id="5ce52-125">\[ [**min\_is**](/windows/desktop/Midl/min-is)\]</span></span>       | <span data-ttu-id="5ce52-126">Menor valor de índice de matriz válido.</span><span class="sxs-lookup"><span data-stu-id="5ce52-126">Lowest valid array index value.</span></span>                         | <span data-ttu-id="5ce52-127">0</span><span class="sxs-lookup"><span data-stu-id="5ce52-127">0</span></span>       |
| <span data-ttu-id="5ce52-128">\[o [ **tamanho \_ é**](/windows/desktop/Midl/size-is)\]</span><span class="sxs-lookup"><span data-stu-id="5ce52-128">\[ [**size\_is**](/windows/desktop/Midl/size-is)\]</span></span>     | <span data-ttu-id="5ce52-129">Número total de elementos de matriz alocados para a matriz.</span><span class="sxs-lookup"><span data-stu-id="5ce52-129">Total number of array elements allocated for the array.</span></span> | \-      |



 

> [!Note]  
> <span data-ttu-id="5ce52-130">O atributo **min \_ is** não está implementado no RPC.</span><span class="sxs-lookup"><span data-stu-id="5ce52-130">The **min\_is** attribute is not implemented in RPC.</span></span> <span data-ttu-id="5ce52-131">O índice de matriz mínimo é sempre tratado como zero.</span><span class="sxs-lookup"><span data-stu-id="5ce52-131">The minimum array index is always treated as zero.</span></span>

 

 

 