---
description: O tipo de dados ASN. 1 BMPString, chamado de \_ cadeia de caracteres Unicode na API de registro de certificado, é codificado em um TLV terceto que começa com um byte de marca de 0x1E.
ms.assetid: 66e4a6d8-2401-4346-9361-e145735cbe19
title: BMPString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c911218d852b792a333f015c825a7e4d1486b62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169495"
---
# <a name="bmpstring"></a><span data-ttu-id="392ed-103">BMPString</span><span class="sxs-lookup"><span data-stu-id="392ed-103">BMPString</span></span>

<span data-ttu-id="392ed-104">O tipo de dados ASN. 1 **BMPString** , chamado de **cadeia de \_ caracteres Unicode** na API de registro de certificado, é codificado em um TLV terceto que começa com um byte de **marca** de 0x1E.</span><span class="sxs-lookup"><span data-stu-id="392ed-104">The ASN.1 **BMPString** data type, called a **UNICODE\_STRING** in the Certificate Enrollment API, is encoded into a TLV triplet that begins with a **Tag** byte of 0x1E.</span></span> <span data-ttu-id="392ed-105">O exemplo a seguir, adaptado do tópico [ASN codificado por CMC. 1](cmc-encoded-asn-1.md) , mostra a codificação para uma extensão **TemplateName** .</span><span class="sxs-lookup"><span data-stu-id="392ed-105">The following example, adapted from the [CMC Encoded ASN.1](cmc-encoded-asn-1.md) topic, shows the encoding for a **TemplateName** extension.</span></span> <span data-ttu-id="392ed-106">O nome pode ser especificado usando a interface [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) .</span><span class="sxs-lookup"><span data-stu-id="392ed-106">The name can be specified by using the [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) interface.</span></span> <span data-ttu-id="392ed-107">O identificador de objeto para a extensão é 1.3.6.1.4.1.311.13.2.1.</span><span class="sxs-lookup"><span data-stu-id="392ed-107">The object identifier for the extension is 1.3.6.1.4.1.311.13.2.1.</span></span>

``` syntax
06 0a                              ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 01  ;   1.3.6.1.4.1.311.13.2.1 
31 34                              ; SET (34 Bytes)
   30 32                           ; SEQUENCE (32 Bytes)
      1e 26                        ; UNICODE_STRING (26 Bytes)
      |  00 43 00 65 00 72 00 74   ;   .C.e.r.t
      |  00 69 00 66 00 69 00 63   ;   .i.f.i.c
      |  00 61 00 74 00 65 00 54   ;   .a.t.e.T
      |  00 65 00 6d 00 70 00 6c   ;   .e.m.p.l
      |  00 61 00 74 00 65         ;   .a.t.e
      1e 08                        ; UNICODE_STRING (8 Bytes)
         00 55 00 73 00 65 00 72   ;   .U.s.e.r
```

<span data-ttu-id="392ed-108">Se a cadeia de caracteres contiver menos de 128 bytes, o campo de **comprimento** do TLV terceto exigirá apenas um byte para especificar o comprimento do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="392ed-108">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="392ed-109">Se a cadeia de caracteres tiver mais de 127 bytes, o bit 7 do campo **comprimento** será definido como 1 e os bits 6 a 0 especificarão o número de bytes adicionais usados para identificar o tamanho do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="392ed-109">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="392ed-110">Para obter mais informações, consulte [comprimento codificado e bytes de valor](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="392ed-110">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="392ed-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="392ed-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="392ed-112">Sistema de tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="392ed-112">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="392ed-113">Codificação DER dos tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="392ed-113">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



