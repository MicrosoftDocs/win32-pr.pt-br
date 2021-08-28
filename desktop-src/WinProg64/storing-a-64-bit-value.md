---
title: Armazenar um valor de 64 bits
description: Para armazenar um valor de ponteiro de 64 bits, use ULONG \_ PTR. Um valor PTR ULONG é de 32 bits quando compilado com um compilador de 32 bits e 64 bits quando compilado com um compilador de \_ 64 bits.
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- armazenar valores de 64 bits com programação Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6be70aba73af9640a69aa60055afcfb03ade7a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469063"
---
# <a name="storing-a-64-bit-value"></a>Armazenar um valor de 64 bits

Para armazenar um valor de ponteiro de 64 bits, use **ULONG \_ PTR**. Um **valor \_ PTR ULONG** é de 32 bits quando compilado com um compilador de 32 bits e 64 bits quando compilado com um compilador de 64 bits.

Os exemplos a seguir usam o código do mundo real que foi portado para 64 bits Windows. Os comentários sobre as etapas para tornar o código compatível de 64 bits estão incluídos.

## <a name="example-1-getting-an-address"></a>Exemplo 1: Obter um endereço

O código a seguir ilustra uma maneira portátil de obter um endereço.




| | | Usando ULONG (um método somente de 32 bits) | <pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )Int *somePointerReturn( (ULONG) somePointer );</code></pre> | | Usando ULONG_PTR (o método portátil) | <pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )Int *somePointerReturn( (ULONG_PTR) somePointer );</code></pre> | 




 

## <a name="example-2-calculating-an-address"></a>Exemplo 2: Calculando um endereço

O código a seguir ilustra uma maneira portátil de calcular um endereço.




| | | Usando ULONG (um método somente de 32 bits) | <pre class="syntax" data-space="preserve"><code>Int *somePointer;Int *someOtherPointer;somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre> | | Usando ULONG_PTR (o método portátil) | <pre class="syntax" data-space="preserve"><code>Int *somePointer;Int *someOtherPointer;somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre> | 




 

 

 




