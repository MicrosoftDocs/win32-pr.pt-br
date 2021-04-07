---
description: O tipo de dados ASN. 1 imenablestring é codificado em um terceto TLV que começa com um byte de marca de 0x13.
ms.assetid: 998fef66-7a24-462f-96f2-92c739bbefa2
title: Imenablestring
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ebc95f1a58e8d7beb4a1d3bbb037788252349a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828342"
---
# <a name="printablestring"></a><span data-ttu-id="32ea8-103">Imenablestring</span><span class="sxs-lookup"><span data-stu-id="32ea8-103">PrintableString</span></span>

<span data-ttu-id="32ea8-104">O tipo de dados ASN. 1 **imenablestring** é codificado em um terceto TLV que começa com um byte de **marca** de 0x13.</span><span class="sxs-lookup"><span data-stu-id="32ea8-104">The ASN.1 **PrintableString** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x13.</span></span> <span data-ttu-id="32ea8-105">O exemplo a seguir, do [tópico \# ASN. 1 codificado em PKCS 10](pkcs--10-encoded-asn-1.md) , mostra como um nome comum de usuário de TestCN é codificado como um tipo **imprimível** .</span><span class="sxs-lookup"><span data-stu-id="32ea8-105">The following example, from the [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md) topic, shows how a user common name of TestCN is encoded as a **PrintableString** type.</span></span> <span data-ttu-id="32ea8-106">O identificador de objeto para um nome comum é 2.5.4.3.</span><span class="sxs-lookup"><span data-stu-id="32ea8-106">The object identifier for a common name is 2.5.4.3.</span></span>

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

<span data-ttu-id="32ea8-107">Se a cadeia de caracteres contiver menos de 128 bytes, o campo de **comprimento** do TLV terceto exigirá apenas um byte para especificar o comprimento do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="32ea8-107">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="32ea8-108">Se a cadeia de caracteres tiver mais de 127 bytes, o bit 7 do campo **comprimento** será definido como 1 e os bits 6 a 0 especificarão o número de bytes adicionais usados para identificar o tamanho do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="32ea8-108">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="32ea8-109">Para obter mais informações, consulte [comprimento codificado e bytes de valor](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="32ea8-109">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="32ea8-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32ea8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32ea8-111">Sistema de tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="32ea8-111">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="32ea8-112">Codificação DER dos tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="32ea8-112">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



