---
title: Ponteiros completos
description: Ao contrário de ponteiros exclusivos, os ponteiros completos dão suporte a aliases.
ms.assetid: 38023942-a4c2-4de7-b7d5-10d508cf083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18687b496ddd28dca9e70afca8deafb18774500a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917408"
---
# <a name="full-pointers"></a><span data-ttu-id="fcbe1-103">Ponteiros completos</span><span class="sxs-lookup"><span data-stu-id="fcbe1-103">Full Pointers</span></span>

<span data-ttu-id="fcbe1-104">Ao contrário de ponteiros [exclusivos](unique-pointers.md) , os ponteiros completos dão suporte a aliases.</span><span class="sxs-lookup"><span data-stu-id="fcbe1-104">Unlike [unique](unique-pointers.md) pointers, full pointers support aliasing.</span></span> <span data-ttu-id="fcbe1-105">Isso significa que vários ponteiros podem se referir aos mesmos dados, conforme mostrado na figura a seguir:</span><span class="sxs-lookup"><span data-stu-id="fcbe1-105">This means that multiple pointers can refer to the same data, as shown in the following figure:</span></span>

![dois ponteiros fazendo referência aos mesmos dados](images/prog-a02.png)

<span data-ttu-id="fcbe1-107">Um ponteiro completo tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="fcbe1-107">A full pointer has the following characteristics:</span></span>

-   <span data-ttu-id="fcbe1-108">Ele pode ter o valor NULL.</span><span class="sxs-lookup"><span data-stu-id="fcbe1-108">It can have the value null.</span></span>
-   <span data-ttu-id="fcbe1-109">Ele pode mudar de nulo para não nulo durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="fcbe1-109">It can change from null to non-null during the call.</span></span> <span data-ttu-id="fcbe1-110">Quando o valor muda para não nulo, o stub do cliente aloca uma nova memória alocado no retorno.</span><span class="sxs-lookup"><span data-stu-id="fcbe1-110">When the value changes to non-null, the client stub allocates new memory allocated on return.</span></span> <span data-ttu-id="fcbe1-111">O programa cliente deve liberar essa memória antes de ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="fcbe1-111">The client program should free this memory before it terminates.</span></span>
-   <span data-ttu-id="fcbe1-112">Ele pode mudar de não nulo para nulo durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="fcbe1-112">It can change from non-null to null during the call.</span></span> <span data-ttu-id="fcbe1-113">Quando o valor é alterado para NULL, o aplicativo é responsável por liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="fcbe1-113">When the value changes to null, the application is responsible for freeing the memory.</span></span>
-   <span data-ttu-id="fcbe1-114">O valor pode ser alterado de um valor não nulo para outro.</span><span class="sxs-lookup"><span data-stu-id="fcbe1-114">The value can change from one non-null value to another.</span></span>
-   <span data-ttu-id="fcbe1-115">O armazenamento que um ponteiro completo aponta para pode ser acessado por outro ponteiro ou nome na operação.</span><span class="sxs-lookup"><span data-stu-id="fcbe1-115">The storage that a full pointer points to may be accessed by another pointer or name in the operation.</span></span>
-   <span data-ttu-id="fcbe1-116">Os dados de retorno são gravados no armazenamento existente se o ponteiro não tiver o valor NULL.</span><span class="sxs-lookup"><span data-stu-id="fcbe1-116">Return data is written into existing storage if the pointer does not have the value null.</span></span>

<span data-ttu-id="fcbe1-117">Use o \[ atributo [**PTR**](/windows/desktop/Midl/ptr) \] para especificar um ponteiro completo, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="fcbe1-117">Use the \[ [**ptr**](/windows/desktop/Midl/ptr) \] attribute to specify a full pointer, as shown in the following example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface FullPtrInterface
{
  void RemoteFn([in,ptr,string]) char *ptrName1,
                [in,ptr,string]  char *ptrName2);
}
```

<span data-ttu-id="fcbe1-118">Neste exemplo, os parâmetros *ptrName1* e *ptrName2* são definidos como ponteiros completos para uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fcbe1-118">In this example the parameters *ptrName1* and *ptrName2* are defined as full pointers to a string.</span></span> <span data-ttu-id="fcbe1-119">É possível que ambos os ponteiros apontem para o mesmo endereço de memória que contém uma única cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fcbe1-119">It is possible for both pointers to point to the same memory address containing a single string.</span></span>

<span data-ttu-id="fcbe1-120">\[**PTR** \] é necessário ao fornecer suporte a alias.</span><span class="sxs-lookup"><span data-stu-id="fcbe1-120">\[**ptr**\] is required when providing aliasing support.</span></span> <span data-ttu-id="fcbe1-121">No entanto, como ela requer o processamento máximo de todos os ponteiros disponíveis no RPC, ela não é recomendada para a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fcbe1-121">However, since it requires the most processing of all the pointers available in RPC, it is not recommended for most applications.</span></span>

 

 