---
description: Os valores inteiros são codificados em um tríplice TLV que começa com um valor tag de 0x02.
ms.assetid: a6fed62f-af59-488c-a690-be8c3413086f
title: INTEGER (API de Registro de Certificado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85151947653a66c98b7a030ade7b9ff7b4f5ee87fd84edc4cc52679be296a1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904334"
---
# <a name="integer-certificate-enrollment-api"></a>INTEGER (API de Registro de Certificado)

Os valores inteiros são codificados em um tríplice TLV que começa com um **valor tag** de 0x02. O **campo** Valor do tripleto TLV conterá o inteiro codificado se ele for positivo ou seu complemento de dois se for negativo. Se o inteiro for positivo, mas o bit de ordem alta estiver definido como 1, uma 0x00 à frente será adicionada ao conteúdo para indicar que o número não é negativo. Por exemplo, o byte de ordem alta 0x8F (10001111) é 1. Portanto, um byte zero à esquerda é adicionado ao conteúdo, conforme mostrado na ilustração a seguir.

![codificação der do tipo de dados booliana](images/der-tlv-integer.png)

Se o inteiro contiver menos de  128 bytes, o campo Comprimento exigirá apenas um byte para especificar o comprimento do conteúdo. Se o inteiro for maior que 127  bytes, o bit 7 do campo Comprimento será definido como 1 e os bits 6 a 0 especificarão o número de bytes adicionais usados para identificar o comprimento do conteúdo. Para obter mais informações, consulte [Bytes de comprimento e valor codificados.](about-encoded-length-and-value-bytes.md)

O exemplo a seguir, do [PKCS \# 10 ASN.1](pkcs--10-encoded-asn-1.md)codificado, mostra a codificação para uma chave pública de 128 byte. O primeiro byte contém o **valor Tag** para o tipo de dados **INTEGER,** 0x02. O segundo e o terceiro bytes contêm o **valor Length.** O bit 7 do segundo byte é definido como 1 porque há mais de 127 bytes de conteúdo. Os bits 0 a 6 do segundo byte especificam o número de bytes à frente necessários, nesse caso, um para especificar com precisão o comprimento do conteúdo. O terceiro byte especifica o número de bytes de conteúdo, 0x81. O quarto byte, 0x00, é adicionado ao conteúdo para indicar que o inteiro é realmente um valor positivo, mesmo que o bit de sinal do byte de conteúdo à frente (0x8F) seja definido como 1.

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

O exemplo a seguir mostra como o valor inteiro 0x03 é codificado. O **byte** Tag contém 0x02 e o byte **Length** especifica que há um byte de conteúdo.

``` syntax
02 01             ; INTEGER (1 Bytes)
|  03
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de tipos ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificação DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



