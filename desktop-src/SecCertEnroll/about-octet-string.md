---
description: O tipo de dados de cadeia de caracteres ASN. 1 OCTET é codificado em um terceto TLV que começa com um byte de marca de 0x04.
ms.assetid: 9d07a6c8-a15f-4030-838c-3063e315684f
title: CADEIA DE CARACTERES DE OCTETO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed2a042312a4415ea9554b7519404097287244f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461234"
---
# <a name="octet-string"></a><span data-ttu-id="0ecb1-103">CADEIA DE CARACTERES DE OCTETO</span><span class="sxs-lookup"><span data-stu-id="0ecb1-103">OCTET STRING</span></span>

<span data-ttu-id="0ecb1-104">O tipo de dados de **cadeia de caracteres** ASN. 1 octet é codificado em um terceto TLV que começa com um byte de **marca** de 0x04.</span><span class="sxs-lookup"><span data-stu-id="0ecb1-104">The ASN.1 **OCTET STRING** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x04.</span></span> <span data-ttu-id="0ecb1-105">Os tipos de dados **String de octeto** e cadeia de [caracteres de bits](about-bit-string.md) são muito semelhantes.</span><span class="sxs-lookup"><span data-stu-id="0ecb1-105">The **OCTET STRING** and [BIT STRING](about-bit-string.md) data types are very similar.</span></span> <span data-ttu-id="0ecb1-106">Assim, os dois tipos são codificados de maneira semelhante, exceto que, como o byte à direita de uma **cadeia de caracteres de octeto** não pode ter bits não utilizados, nenhum byte à esquerda deve ser adicionado ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0ecb1-106">Thus, the two types are encoded in a similar manner except that, because the trailing byte of an **OCTET STRING** cannot have unused bits, no leading bytes must be added to the content.</span></span> <span data-ttu-id="0ecb1-107">O exemplo a seguir, adaptado do tópico [ASN codificado por CMC. 1](cmc-encoded-asn-1.md) , mostra como o nome de um modelo de certificado é codificado como uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="0ecb1-107">The following example, adapted from the [CMC Encoded ASN.1](cmc-encoded-asn-1.md) topic, shows how the name of a certificate template is encoded as a byte array.</span></span>

``` syntax
30 17                                 ; SEQUENCE (17 Bytes)
|  06 09                              ; OBJECT_ID (9 Bytes)
|  |  2b 06 01 04 01 82 37 14  02     ;   1.3.6.1.4.1.311.20.2
|  04 0a                              ; OCTET_STRING (a Bytes)
|     1e 08 00 55 00 73 00 65  00 72  ;   ...U.s.e.r
```

<span data-ttu-id="0ecb1-108">Se a matriz de bytes contiver menos de 128 bytes, o campo de **comprimento** do TLV terceto exigirá apenas um byte para especificar o comprimento do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0ecb1-108">If the byte array contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="0ecb1-109">Se for maior que 127 bytes, o bit 7 do campo **comprimento** será definido como 1 e os bits 6 a 0 especificarão o número de bytes adicionais usados para identificar o tamanho do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0ecb1-109">If it is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="0ecb1-110">Isso é mostrado no exemplo a seguir, em que o bit de ordem superior do segundo byte na primeira linha é definido como 1 e o byte indica que há um byte de **comprimento** à direita.</span><span class="sxs-lookup"><span data-stu-id="0ecb1-110">This is shown in the following example where the high order bit of the second byte on the first line is set to 1 and the byte indicates that there is a trailing **Length** byte.</span></span> <span data-ttu-id="0ecb1-111">O terceiro byte, portanto, especifica que o conteúdo tem 0x80 bytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="0ecb1-111">The third byte therefore specifies that the content is 0x80 bytes long.</span></span>

``` syntax
04 81 80                       ; OCTET_STRING (80 Bytes)
   38 10 60 e2 70 69 91 4a     ;   8.`.pi.J
   8b b5 22 57 2a 62 ef de     ;   .."W*b..
   15 7d 59 d6 4e 20 9a 45     ;   .}Y.N .E
   2b e3 fd fc 68 ba af bf     ;   +...h...
   9c 17 b0 8e 6d c4 29 1e     ;   ....m.).
   e3 21 ac bb 5a 8a c9 67     ;   .!..Z..g
   0a d4 45 93 10 c0 26 eb     ;   ..E...&.
   0a 83 c2 b1 40 87 36 f7     ;   ....@.6.
   a0 26 da b9 bb 46 73 88     ;   .&...Fs.
   7a 67 b9 e6 b3 6f ea 59     ;   zg...o.Y
   28 8a d3 92 72 f6 7b 89     ;   (...r.{.
   a0 d8 2d 9e 40 eb 1e bb     ;   ..-.@...
   6e ae f0 5a ed 16 c9 e3     ;   n..Z....
   27 59 37 8f f3 4a 98 60     ;   'Y7..J.`
   f8 fb a7 0a ee 1b 6e 91     ;   ......n.
   95 96 cf 0d 56 ac ab 35     ;   ....V..5
```

## <a name="related-topics"></a><span data-ttu-id="0ecb1-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ecb1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ecb1-113">Sistema de tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="0ecb1-113">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="0ecb1-114">Codificação DER dos tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="0ecb1-114">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



