---
description: O valor NULL é codificado em um terceto TLV que começa com um valor de marca de 0x05, um comprimento de 0x00 e nenhum byte de valor, conforme mostrado na ilustração a seguir.
ms.assetid: f712f84a-c4d3-41bb-b151-62b0f86046af
title: NULO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6dec81fb2024899121ad4e2eb78aa54372a1b71
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105780480"
---
# <a name="null"></a><span data-ttu-id="bf8c7-103">NULO</span><span class="sxs-lookup"><span data-stu-id="bf8c7-103">NULL</span></span>

<span data-ttu-id="bf8c7-104">O valor **NULL** é codificado em um terceto TLV que começa com um valor de **marca** de 0x05, um **comprimento** de 0x00 e nenhum byte de **valor** , conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="bf8c7-104">The **NULL** value is encoded into a TLV triplet that begins with a **Tag** value of 0x05, a **Length** of 0x00, and no **Value** byte as shown by the following illustration.</span></span>

![codificação der de tipo de dados nulo](images/der-tlv-null.png)

<span data-ttu-id="bf8c7-106">A quinta linha do exemplo a seguir, adaptada do [tópico \# ASN. 1 codificado em PKCS 10](pkcs--10-encoded-asn-1.md) , mostra um valor **NULL** codificado.</span><span class="sxs-lookup"><span data-stu-id="bf8c7-106">The fifth line of the following example, adapted from the [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md) topic, shows an encoded **NULL** value.</span></span> <span data-ttu-id="bf8c7-107">O primeiro byte é 0x05 e o segundo byte é 0x00.</span><span class="sxs-lookup"><span data-stu-id="bf8c7-107">The first byte is 0x05, and the second byte is 0x00.</span></span> <span data-ttu-id="bf8c7-108">Não há byte de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="bf8c7-108">There is no content byte.</span></span>

``` syntax
30 81 9f                                ; SEQUENCE (9f Bytes)
|  30 0d                                ; SEQUENCE (d Bytes)
|  |  06 09                             ; OBJECT_ID (9 Bytes)
|  |  |  2a 86 48 86 f7 0d 01 01  01    ; 1.2.840.113549.1.1.1
|  |  05 00                             ; NULL (0 Bytes)
|  03 81 8d                             ; BIT_STRING (8d Bytes)
|     00
|     30 81 89                          ; SEQUENCE (89 Bytes)
|        02 81 81                       ; INTEGER (81 Bytes)
|        |  00
|        |  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|        |  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|        |  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|        |  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|        |  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|        |  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|        |  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|        |  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
|        02 03                          ; INTEGER (3 Bytes)
|           01 00 01
```

## <a name="related-topics"></a><span data-ttu-id="bf8c7-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf8c7-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf8c7-110">Sistema de tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="bf8c7-110">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="bf8c7-111">Codificação DER dos tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="bf8c7-111">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



