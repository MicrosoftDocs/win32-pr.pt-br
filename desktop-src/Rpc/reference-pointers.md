---
title: Ponteiros de referência
description: Ponteiros de referência são os ponteiros mais simples e exigem a menor quantidade de processamento pelo stub do cliente.
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427605f330b1a73c541c95019f8ca4bdd6cc8ef4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008048"
---
# <a name="reference-pointers"></a><span data-ttu-id="289a5-103">Ponteiros de referência</span><span class="sxs-lookup"><span data-stu-id="289a5-103">Reference Pointers</span></span>

<span data-ttu-id="289a5-104">Ponteiros de referência são os ponteiros mais simples e exigem a menor quantidade de processamento pelo stub do cliente.</span><span class="sxs-lookup"><span data-stu-id="289a5-104">Reference pointers are the simplest pointers and require the least amount of processing by the client stub.</span></span> <span data-ttu-id="289a5-105">Quando um programa cliente passa um ponteiro de referência para um procedimento remoto, o ponteiro de referência sempre contém o endereço de um bloco de memória válido.</span><span class="sxs-lookup"><span data-stu-id="289a5-105">When a client program passes a reference pointer to a remote procedure, the reference pointer always contains the address of a valid block of memory.</span></span> <span data-ttu-id="289a5-106">Ele ainda estará apontando para o mesmo bloco de memória quando o procedimento remoto for concluído.</span><span class="sxs-lookup"><span data-stu-id="289a5-106">It will still be pointing to the same memory block when the remote procedure completes.</span></span> <span data-ttu-id="289a5-107">Esses ponteiros são usados principalmente para implementar semânticas de referência e para permitir \[ parâmetros de [**saída**](/windows/desktop/Midl/out-idl) \] em C.</span><span class="sxs-lookup"><span data-stu-id="289a5-107">These pointers are mainly used to implement reference semantics, and to allow for \[[**out**](/windows/desktop/Midl/out-idl)\] parameters in C.</span></span>

<span data-ttu-id="289a5-108">No exemplo a seguir, o valor do ponteiro não é alterado durante a chamada, embora o conteúdo dos dados no endereço indicado pelo ponteiro possa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="289a5-108">In the following example, the value of the pointer does not change during the call, although the contents of the data at the address indicated by the pointer can change.</span></span>

![alteração de dados em um endereço de ponteiro de referência estática](images/prog-a07.png)

<span data-ttu-id="289a5-110">Um ponteiro de referência tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="289a5-110">A reference pointer has the following characteristics:</span></span>

-   <span data-ttu-id="289a5-111">Ele sempre aponta para um armazenamento válido e nunca tem o valor **NULL**.</span><span class="sxs-lookup"><span data-stu-id="289a5-111">It always points to valid storage and never has the value **NULL**.</span></span>
-   <span data-ttu-id="289a5-112">Ele nunca muda durante uma chamada e sempre aponta para o mesmo armazenamento antes e depois da chamada.</span><span class="sxs-lookup"><span data-stu-id="289a5-112">It never changes during a call and always points to the same storage before and after the call.</span></span>
-   <span data-ttu-id="289a5-113">Os dados retornados do procedimento remoto são gravados no armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="289a5-113">Data returned from the remote procedure is written into the existing storage.</span></span>
-   <span data-ttu-id="289a5-114">O armazenamento apontado por um ponteiro de referência não pode ser acessado por nenhum outro ponteiro ou por qualquer outro nome na função.</span><span class="sxs-lookup"><span data-stu-id="289a5-114">The storage pointed to by a reference pointer cannot be accessed by any other pointer or any other name in the function.</span></span>

<span data-ttu-id="289a5-115">Use o \[ [](/windows/desktop/Midl/ref) \] atributo ref para especificar ponteiros de referência em definições de interface, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="289a5-115">Use the \[[**ref**](/windows/desktop/Midl/ref)\] attribute to specify reference pointers in interface definitions, as shown in the following example.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, out, ref] char *pChar);
}
```

<span data-ttu-id="289a5-116">Este exemplo define o parâmetro *pChar* como um ponteiro para um único caractere, não uma matriz de caracteres.</span><span class="sxs-lookup"><span data-stu-id="289a5-116">This example defines the parameter *pChar* as a pointer to a single character, not an array of characters.</span></span> <span data-ttu-id="289a5-117">É um parâmetro \[ **out** \] e um ponteiro de referência que aponta para a memória que a rotina de servidor RemoteFn preencherá com os dados.</span><span class="sxs-lookup"><span data-stu-id="289a5-117">It is an \[**out**\] parameter and a reference pointer that points to memory that the server routine RemoteFn will fill with data.</span></span>

 

 