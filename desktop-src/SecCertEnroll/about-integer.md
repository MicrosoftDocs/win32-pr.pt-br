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
# <a name="integer-certificate-enrollment-api"></a><span data-ttu-id="a867c-103">INTEIRO (API de registro de certificado)</span><span class="sxs-lookup"><span data-stu-id="a867c-103">INTEGER (Certificate Enrollment API)</span></span>

<span data-ttu-id="a867c-104">Os valores inteiros são codificados em um terceto TLV que começa com um valor de **marca** 0x02.</span><span class="sxs-lookup"><span data-stu-id="a867c-104">Integer values are encoded into a TLV triplet that begins with a **Tag** value of 0x02.</span></span> <span data-ttu-id="a867c-105">O campo de **valor** do TLV terceto contém o inteiro codificado, se for positivo, ou o complemento de dois, se for negativo.</span><span class="sxs-lookup"><span data-stu-id="a867c-105">The **Value** field of the TLV triplet contains the encoded integer if it is positive, or its two's complement if it is negative.</span></span> <span data-ttu-id="a867c-106">Se o inteiro for positivo, mas o bit de ordem superior estiver definido como 1, um 0x00 à esquerda será adicionado ao conteúdo para indicar que o número não é negativo.</span><span class="sxs-lookup"><span data-stu-id="a867c-106">If the integer is positive but the high order bit is set to 1, a leading 0x00 is added to the content to indicate that the number is not negative.</span></span> <span data-ttu-id="a867c-107">Por exemplo, o byte de ordem superior de 0x8F (10001111) é 1.</span><span class="sxs-lookup"><span data-stu-id="a867c-107">For example, the high order byte of 0x8F (10001111) is 1.</span></span> <span data-ttu-id="a867c-108">Portanto, um byte zero à esquerda é adicionado ao conteúdo, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="a867c-108">Therefore a leading zero byte is added to the content as shown in the following illustration.</span></span>

![codificação der de tipo de dados booliano](images/der-tlv-integer.png)

<span data-ttu-id="a867c-110">Se o número inteiro contiver menos de 128 bytes, o campo *comprimento* exigirá apenas um byte para especificar o comprimento do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a867c-110">If the integer contains fewer than 128 bytes, the *Length* field requires only one byte to specify the content length.</span></span> <span data-ttu-id="a867c-111">Se o número inteiro for maior que 127 bytes, o bit 7 do campo *comprimento* será definido como 1 e os bits 6 a 0 especificarão o número de bytes adicionais usados para identificar o tamanho do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a867c-111">If the integer is more than 127 bytes, bit 7 of the *Length* field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="a867c-112">Para obter mais informações, consulte [comprimento codificado e bytes de valor](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="a867c-112">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

<span data-ttu-id="a867c-113">O exemplo a seguir, [de \# ASN codificado em PKCS 10](pkcs--10-encoded-asn-1.md), mostra a codificação para uma chave pública de 128 bytes.</span><span class="sxs-lookup"><span data-stu-id="a867c-113">The following example, from [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md), shows the encoding for a 128 byte public key.</span></span> <span data-ttu-id="a867c-114">O primeiro byte contém o valor da **marca** para o tipo de dados **Integer** , 0x02.</span><span class="sxs-lookup"><span data-stu-id="a867c-114">The first byte contains the **Tag** value for the **INTEGER** data type, 0x02.</span></span> <span data-ttu-id="a867c-115">O segundo e o terceiro bytes contêm o valor de **comprimento** .</span><span class="sxs-lookup"><span data-stu-id="a867c-115">The second and third bytes contain the **Length** value.</span></span> <span data-ttu-id="a867c-116">O bit 7 do segundo byte é definido como 1 porque há mais de 127 bytes de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a867c-116">Bit 7 of the second byte is set to 1 because there are more than 127 bytes of content.</span></span> <span data-ttu-id="a867c-117">Bits 0 a 6 do segundo byte especificam o número de bytes à direita necessários, nesse caso, para especificar com precisão o comprimento do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a867c-117">Bits 0 through 6 of the second byte specify the number of trailing bytes needed, in this case one, to accurately specify the content length.</span></span> <span data-ttu-id="a867c-118">O terceiro byte Especifica o número de bytes de conteúdo, 0x81.</span><span class="sxs-lookup"><span data-stu-id="a867c-118">The third byte specifies the number of content bytes, 0x81.</span></span> <span data-ttu-id="a867c-119">O quarto byte, 0x00, é adicionado ao conteúdo para indicar que o inteiro é realmente um valor positivo, embora o bit de sinal do byte de conteúdo à esquerda (0x8F) seja definido como 1.</span><span class="sxs-lookup"><span data-stu-id="a867c-119">The fourth byte, 0x00, is added to the content to indicate that the integer is indeed a positive value even though the sign bit of the leading content byte (0x8F) is set to 1.</span></span>

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

<span data-ttu-id="a867c-120">O exemplo a seguir mostra como o valor inteiro 0x03 é codificado.</span><span class="sxs-lookup"><span data-stu-id="a867c-120">The following example shows how the integer value 0x03 is encoded.</span></span> <span data-ttu-id="a867c-121">O byte da **marca** contém 0x02 e o byte de **comprimento** especifica que há um byte de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a867c-121">The **Tag** byte contains 0x02, and the **Length** byte specifies that there is one byte of content.</span></span>

``` syntax
02 01             ; INTEGER (1 Bytes)
|  03
```

## <a name="related-topics"></a><span data-ttu-id="a867c-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a867c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a867c-123">Sistema de tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="a867c-123">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="a867c-124">Codificação DER dos tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="a867c-124">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



