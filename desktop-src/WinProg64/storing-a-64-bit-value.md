---
title: Armazenando um valor de 64 bits
description: Para armazenar um valor de ponteiro de 64 bits, use ULONG \_ PTR. Um valor do ULONG \_ ptr é 32 bits quando compilado com um compilador de 32 bits e 64 bits quando compilado com um compilador de 64 bits.
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- Armazenando valores de 64 bits programação do Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cee4826caf93dbd464957fb5fb76f024bd9f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292197"
---
# <a name="storing-a-64-bit-value"></a><span data-ttu-id="d0f94-105">Armazenando um valor de 64 bits</span><span class="sxs-lookup"><span data-stu-id="d0f94-105">Storing a 64-bit Value</span></span>

<span data-ttu-id="d0f94-106">Para armazenar um valor de ponteiro de 64 bits, use **ULONG \_ PTR**.</span><span class="sxs-lookup"><span data-stu-id="d0f94-106">To store a 64-bit pointer value, use **ULONG\_PTR**.</span></span> <span data-ttu-id="d0f94-107">Um valor do **ULONG \_ PTR** é 32 bits quando compilado com um compilador de 32 bits e 64 bits quando compilado com um compilador de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d0f94-107">A **ULONG\_PTR** value is 32 bits when compiled with a 32-bit compiler and 64 bits when compiled with a 64-bit compiler.</span></span>

<span data-ttu-id="d0f94-108">Os exemplos a seguir usam o código do mundo real que foi movido para o Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d0f94-108">The following examples use real-world code that has been ported to 64-bit Windows.</span></span> <span data-ttu-id="d0f94-109">Comentários sobre as etapas para tornar o código compatível com 64 bits é incluído.</span><span class="sxs-lookup"><span data-stu-id="d0f94-109">Commentary on the steps to make the code 64-bit compatible is included.</span></span>

## <a name="example-1-getting-an-address"></a><span data-ttu-id="d0f94-110">Exemplo 1: obtendo um endereço</span><span class="sxs-lookup"><span data-stu-id="d0f94-110">Example 1: Getting an Address</span></span>

<span data-ttu-id="d0f94-111">O código a seguir ilustra uma maneira portátil de obter um endereço.</span><span class="sxs-lookup"><span data-stu-id="d0f94-111">The following code illustrates a portable way to get an address.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d0f94-112">Usando o ULONG (um método somente de 32 bits)</span><span class="sxs-lookup"><span data-stu-id="d0f94-112">Using ULONG (a 32-bit-only method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )
Int *somePointer
Return( (ULONG) somePointer );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0f94-113">Usando ULONG_PTR (o método portátil)</span><span class="sxs-lookup"><span data-stu-id="d0f94-113">Using ULONG_PTR (the portable method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )
Int *somePointer
Return( (ULONG_PTR) somePointer );</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="example-2-calculating-an-address"></a><span data-ttu-id="d0f94-114">Exemplo 2: calculando um endereço</span><span class="sxs-lookup"><span data-stu-id="d0f94-114">Example 2: Calculating an Address</span></span>

<span data-ttu-id="d0f94-115">O código a seguir ilustra uma maneira portátil de calcular um endereço.</span><span class="sxs-lookup"><span data-stu-id="d0f94-115">The following code illustrates a portable way to calculate an address.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d0f94-116">Usando o ULONG (um método somente de 32 bits)</span><span class="sxs-lookup"><span data-stu-id="d0f94-116">Using ULONG (a 32-bit-only method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0f94-117">Usando ULONG_PTR (o método portátil)</span><span class="sxs-lookup"><span data-stu-id="d0f94-117">Using ULONG_PTR (the portable method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre></td>
</tr>
</tbody>
</table>



 

 

 




