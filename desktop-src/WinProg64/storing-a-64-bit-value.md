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
# <a name="storing-a-64-bit-value"></a>Armazenando um valor de 64 bits

Para armazenar um valor de ponteiro de 64 bits, use **ULONG \_ PTR**. Um valor do **ULONG \_ PTR** é 32 bits quando compilado com um compilador de 32 bits e 64 bits quando compilado com um compilador de 64 bits.

Os exemplos a seguir usam o código do mundo real que foi movido para o Windows de 64 bits. Comentários sobre as etapas para tornar o código compatível com 64 bits é incluído.

## <a name="example-1-getting-an-address"></a>Exemplo 1: obtendo um endereço

O código a seguir ilustra uma maneira portátil de obter um endereço.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Usando o ULONG (um método somente de 32 bits)</td>
<td><pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )
Int *somePointer
Return( (ULONG) somePointer );</code></pre></td>
</tr>
<tr class="even">
<td>Usando ULONG_PTR (o método portátil)</td>
<td><pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )
Int *somePointer
Return( (ULONG_PTR) somePointer );</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="example-2-calculating-an-address"></a>Exemplo 2: calculando um endereço

O código a seguir ilustra uma maneira portátil de calcular um endereço.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Usando o ULONG (um método somente de 32 bits)</td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre></td>
</tr>
<tr class="even">
<td>Usando ULONG_PTR (o método portátil)</td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre></td>
</tr>
</tbody>
</table>



 

 

 




