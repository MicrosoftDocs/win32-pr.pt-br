---
description: O tipo de dados STRING de BIT é codificado em um terceto TLV que começa com um byte de marca de 0x03.
ms.assetid: 7464dd20-5e79-4ca1-a6ae-9b706e9cb925
title: CADEIA DE BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115ead46663b94d6db2d089f1fae2fd8c40a2ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557747"
---
# <a name="bit-string"></a>CADEIA DE BITS

O tipo de dados **String de bit** é codificado em um terceto TLV que começa com um byte de **marca** de 0x03. O campo de **valor** do TLV terceto contém um byte à esquerda que especifica o número de bits restantes não usados no byte final de conteúdo. No exemplo a seguir, o campo **comprimento** é definido como 0x03 porque três bytes de conteúdo seguem e o byte à esquerda do campo **valor** é definido como 0x04 porque há quatro bits não utilizados no último byte de conteúdo. Cada bit não utilizado é indicado pela letra x.

![codificação der de tipo de dados de cadeia de bits](images/der-tlv-bitstring.png)

O exemplo a seguir, adaptado do tópico [ \# ASN. 1 codificado em PKCS 10](pkcs--10-encoded-asn-1.md) , mostra a assinatura codificada de uma solicitação de certificado PKCS 10 de exemplo \# . O primeiro byte contém o valor da **marca** para o tipo de dados **String de bit** , 0x03. O segundo e o terceiro bytes contêm o comprimento da matriz de bytes. O bit 7 do segundo byte é definido como 1 porque há mais de 127 bytes de conteúdo. O bits 0 a 6 do segundo byte Especifica o número de bytes de **comprimento** à direita, neste caso, um. O terceiro byte Especifica o número de bytes de conteúdo, 0x81. O quarto byte, 0x00, especifica o número de bits não utilizados que existem no último byte de conteúdo. Observe que a assinatura é codificada na ordem de bytes big-endian.

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

[Sistema de tipo ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codificação DER dos tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Comprimento codificado e bytes de valor](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 



