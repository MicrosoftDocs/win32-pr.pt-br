---
description: Os valores inteiros são codificados em um terceto TLV que começa com um valor de marca 0x02.
ms.assetid: a6fed62f-af59-488c-a690-be8c3413086f
title: INTEIRO (API de registro de certificado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0e8ed162d4cf4b2ac4909baf1cd7b5e94ddea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296736"
---
# <a name="integer-certificate-enrollment-api"></a>INTEIRO (API de registro de certificado)

Os valores inteiros são codificados em um terceto TLV que começa com um valor de **marca** 0x02. O campo de **valor** do TLV terceto contém o inteiro codificado, se for positivo, ou o complemento de dois, se for negativo. Se o inteiro for positivo, mas o bit de ordem superior estiver definido como 1, um 0x00 à esquerda será adicionado ao conteúdo para indicar que o número não é negativo. Por exemplo, o byte de ordem superior de 0x8F (10001111) é 1. Portanto, um byte zero à esquerda é adicionado ao conteúdo, conforme mostrado na ilustração a seguir.

![codificação der de tipo de dados booliano](images/der-tlv-integer.png)

Se o número inteiro contiver menos de 128 bytes, o campo *comprimento* exigirá apenas um byte para especificar o comprimento do conteúdo. Se o número inteiro for maior que 127 bytes, o bit 7 do campo *comprimento* será definido como 1 e os bits 6 a 0 especificarão o número de bytes adicionais usados para identificar o tamanho do conteúdo. Para obter mais informações, consulte [comprimento codificado e bytes de valor](about-encoded-length-and-value-bytes.md).

O exemplo a seguir, [de \# ASN codificado em PKCS 10](pkcs--10-encoded-asn-1.md), mostra a codificação para uma chave pública de 128 bytes. O primeiro byte contém o valor da **marca** para o tipo de dados **Integer** , 0x02. O segundo e o terceiro bytes contêm o valor de **comprimento** . O bit 7 do segundo byte é definido como 1 porque há mais de 127 bytes de conteúdo. Bits 0 a 6 do segundo byte especificam o número de bytes à direita necessários, nesse caso, para especificar com precisão o comprimento do conteúdo. O terceiro byte Especifica o número de bytes de conteúdo, 0x81. O quarto byte, 0x00, é adicionado ao conteúdo para indicar que o inteiro é realmente um valor positivo, embora o bit de sinal do byte de conteúdo à esquerda (0x8F) seja definido como 1.

``` syntax
02 81 81          ; INTEGER (81 Bytes)
|  00
|  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
```

O exemplo a seguir mostra como o valor inteiro 0x03 é codificado. O byte da **marca** contém 0x02 e o byte de **comprimento** especifica que há um byte de conteúdo.

``` syntax
02 01             ; INTEGER (1 Bytes)
|  03
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de tipo ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codificação DER dos tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



