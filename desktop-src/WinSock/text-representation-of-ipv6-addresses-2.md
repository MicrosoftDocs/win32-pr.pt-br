---
description: Esta seção é copiada de &\# 0034; arquitetura de endereçamento IPv6&\# 0034; por R.
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: Representação de texto de endereços IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df97c1c8933f3708fee56e34e05f918d531d2a13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815472"
---
# <a name="text-representation-of-ipv6-addresses"></a>Representação de texto de endereços IPv6

Esta seção é copiada de "arquitetura de endereçamento IPv6" em R. Hinden e S. Deering. Há três formulários convencionais para representar endereços IPv6 como cadeias de caracteres de texto:

-   A forma preferida é x:x: x:x: x:x: x:x, onde os ' x ' são os valores hexadecimais das partes de 8 16 bits do endereço.

    Exemplos:

    <dl> FEDC:BA98:7654:3210:FEDC:BA98:7654:3210  
    1080:0: 0:0: 8:800:200C: 417A  
    </dl>

> [!Note]  
> Não é necessário gravar os zeros à esquerda em um campo individual, mas deve haver pelo menos um numeral em cada campo (exceto pelo caso descrito no segundo formulário).

 

-   Devido ao método de alocar determinados estilos de endereços IPv6, é comum que os endereços contenham cadeias de caracteres longas de zero bits. Para tornar a gravação de endereços com zero bits mais fácil, uma sintaxe especial está disponível para compactar os zeros. O uso de dois-pontos duplos ("::") indica vários grupos de 16 bits de zeros.

    Por exemplo, o endereço de multicast

    <dl> FF01:0: 0:0: 0:0: 0:43  
    </dl>

    pode ser representado como:

    <dl> FF01:: 43  
    </dl>

    As aspas duplas ("::") só podem aparecer uma vez em um endereço. Eles podem ser usados para compactar zeros à esquerda ou à direita em um endereço.

-   Uma forma alternativa que pode ser mais conveniente ao lidar com um ambiente misto de nós IPv4 e IPv6 é o x:x: x:x: x:x: d. d. d. d, em que os "x" são os valores hexadecimais das seis partes de 16 bits de ordem superior do endereço, e os valores decimais das quatro partes de 8 bits de ordem inferior do endereço (representação IPv4 padrão).

    Exemplos:

    <dl> 0:0: 0:0: 0:0: 13.1.68.3  
    0:0: 0:0: 0: FFFF: 129.144.52.38  
    </dl>

    ou em formato compactado:

    <dl> ::13.1.68.3  
    :: FFFF: 129.144.52.38  
    </dl>

 

 



