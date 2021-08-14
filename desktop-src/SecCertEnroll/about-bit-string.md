---
description: O tipo de dados BIT STRING é codificado em um tríplice TLV que começa com um byte tag de 0x03.
ms.assetid: 7464dd20-5e79-4ca1-a6ae-9b706e9cb925
title: CADEIA DE CARACTERES DE BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056616a22cf2e683e943afef9369ed4c885963174aff0e72dea6ef718ddbdf7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905052"
---
# <a name="bit-string"></a>CADEIA DE CARACTERES DE BITS

O **tipo de dados BIT STRING** é codificado em um tríplice TLV que começa com um byte tag de 0x03.  O **campo** Valor do tripleto TLV contém um byte à esquerda que especifica o número de bits deixados sem uso no byte final do conteúdo. No exemplo a  seguir, o campo Comprimento é definido como 0x03 porque três  bytes de conteúdo seguem e o byte à frente do campo Valor é definido como 0x04 porque há quatro bits nãoutilados no último byte de conteúdo. Cada bit não utilizado é anotado pela letra x.

![codificação der do tipo de dados de cadeia de caracteres de bits](images/der-tlv-bitstring.png)

O exemplo a seguir, adaptado do tópico [ \# ASN.1 codificado em PKCS 10,](pkcs--10-encoded-asn-1.md) mostra a assinatura codificada de uma solicitação de certificado PKCS \# 10 de exemplo. O primeiro byte contém o valor **Tag** para o tipo de dados **BIT STRING,** 0x03. O segundo e o terceiro bytes contêm o comprimento da matriz de bytes. O bit 7 do segundo byte é definido como 1 porque há mais de 127 bytes de conteúdo. Os bits 0 a 6 do segundo byte especificam o número de bytes **de comprimento** à frente, nesse caso, um. O terceiro byte especifica o número de bytes de conteúdo, 0x81. O quarto byte, 0x00, especifica o número de bits nãoutilados que existem no último byte de conteúdo. Observe que a assinatura é codificada em ordem de byte big-endian.

``` syntax
0299:    03 81 81           ; BIT_STRING (81 Bytes)
029c:       00
029d:       47 eb 99 5a df 9e 70 0d  fb a7 31 32 c1 5f 5c 24
02ad:       c2 e0 bf c6 24 af 15 66  0e b8 6a 2e ab 2b c4 97
02bd:       1f e3 cb dc 63 a5 25 ec  c7 b4 28 61 66 36 a1 31
02cd:       1b bf dd d0 fc bf 17 94  90 1d e5 5e c7 11 5e c9
02dd:       55 9f eb a3 3e 14 c7 99  a6 cb ba a1 46 0f 39 d4
02ed:       44 c4 c8 4b 76 0e 20 5d  6d a9 34 9e d4 d5 87 42
02fd:       eb 24 26 51 14 90 b4 0f  06 5e 52 88 32 7a 95 20
030d:       a0 fd f7 e5 7d 60 dd 72  68 9b f5 7b 05 8f 6d 1e
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de tipos ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificação DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Bytes de comprimento e valor codificados](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 



