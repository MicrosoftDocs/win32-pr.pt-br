---
description: Esta seção é copiada do &0034;Arquitetura de Endereçamento \# IPv6&\# 0034; por R.
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: Representação de texto de endereços IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d71ad1f98652a0f00e4f14f957bcedc27316444ceabc3e5c35ee2bcf81b5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733346"
---
# <a name="text-representation-of-ipv6-addresses"></a>Representação de texto de endereços IPv6

Esta seção é copiada da "Arquitetura de Endereçamento IPv6" por R. Deering e S. Há três formas convencionais para representar endereços IPv6 como cadeias de caracteres de texto:

-   O formulário preferencial é x:x:x:x:x:x:x:x, em que 'x's são os valores hexadecimais das oito partes de 16 bits do endereço.

    Exemplos:

    <dl> FEDC:BA98:7654:3210:FEDC:BA98:7654:3210  
    1080:0:0:0:8:800:200C:417A  
    </dl>

> [!Note]  
> Não é necessário gravar os zeros à esquerda em um campo individual, mas deve haver pelo menos um numeral em cada campo (exceto pelo caso descrito no segundo formulário).

 

-   Devido ao método de alocação de determinados estilos de endereços IPv6, é comum que os endereços contenham cadeias de caracteres longas de zero bits. Para facilitar a escrita de endereços que contêm zero bits, uma sintaxe especial está disponível para compactar os zeros. O uso de dois-pontos duplos ("::") indica vários grupos de 16 bits de zeros.

    Por exemplo, o endereço multicast

    <dl> FF01:0:0:0:0:0:0:43  
    </dl>

    pode ser representado como:

    <dl> FF01::43  
    </dl>

    As aspas duplas ("::") só podem aparecer uma vez em um endereço. Eles podem ser usados para compactar zeros à esquerda ou à esquerda em um endereço.

-   Uma forma alternativa que pode ser mais conveniente ao lidar com um ambiente misto de nós IPv4 e IPv6 é x:x:x:x:x:x:x:d.d.d.d.d, em que os 'xs são os valores hexadecimais das seis partes de 16 bits de ordem alta do endereço e os 'd's são os valores decimais das quatro partes de 8 bits de ordem baixa do endereço (representação IPv4 padrão).

    Exemplos:

    <dl> 0:0:0:0:0:0:13.1.68.3  
    0:0:0:0:0:FFFF:129.144.52.38  
    </dl>

    ou em formato compactado:

    <dl> ::13.1.68.3  
    ::FFFF:129.144.52.38  
    </dl>

 

 



