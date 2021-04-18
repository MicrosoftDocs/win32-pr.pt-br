---
description: Um conjunto contém uma série não ordenada de campos de um ou mais tipos.
ms.assetid: 6bbe89da-1177-4cfa-9515-03b271e5ef6b
title: SET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572114d754b5034babe81e3914599f48996867d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756864"
---
# <a name="set"></a><span data-ttu-id="f30c7-103">SET</span><span class="sxs-lookup"><span data-stu-id="f30c7-103">SET</span></span>

<span data-ttu-id="f30c7-104">Um **conjunto** contém uma série não ordenada de campos de um ou mais tipos.</span><span class="sxs-lookup"><span data-stu-id="f30c7-104">A **SET** contains an unordered series of fields of one or more types.</span></span> <span data-ttu-id="f30c7-105">Ele é codificado em um terceto TLV que começa com um byte de **marca** de 0x31.</span><span class="sxs-lookup"><span data-stu-id="f30c7-105">It is encoded into a TLV triplet that begins with a **Tag** byte of 0x31.</span></span> <span data-ttu-id="f30c7-106">O exemplo a seguir, adaptado do tópico [ASN codificado por CMC. 1](cmc-encoded-asn-1.md) , mostra como um atributo **ClientID** é codificado em uma estrutura de dados **definida** .</span><span class="sxs-lookup"><span data-stu-id="f30c7-106">The following example, adapted from the [CMC Encoded ASN.1](cmc-encoded-asn-1.md) topic, shows how a **ClientId** attribute is encoded in a **SET** data structure.</span></span> <span data-ttu-id="f30c7-107">O atributo pode ser especificado usando a interface [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) .</span><span class="sxs-lookup"><span data-stu-id="f30c7-107">The attribute can be specified by using the [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) interface.</span></span>

``` syntax
31 59                                     ; SET (59 Bytes)
   30 57                                  ; SEQUENCE (57 Bytes)
      06 09                               ; OBJECT_ID (9 Bytes)
      |  2b 06 01 04 01 82 37 15  14      ;   1.3.6.1.4.1.311.21.20 
      31 4a                               ; SET (4a Bytes)
         30 48                            ; SEQUENCE (48 Bytes)
            02 01                         ; INTEGER (1 Bytes)
            |  09
            0c 23                         ; UTF8_STRING (23 Bytes)
            |  76 69 63 68 33 64 2e 6a    ;   vich3d.j
            |  64 6f 6d 63 73 63 2e 6e    ;   domcsc.n
            |  74 74 65 73 74 2e 6d 69    ;   ttest.mi
            |  63 72 6f 73 6f 66 74 2e    ;   crosoft.
            |  63 6f 6d                   ;   com
            0c 15                         ; UTF8_STRING (15 Bytes)
            |  4a 44 4f 4d 43 53 43 5c    ;   JDOMCSC\
            |  61 64 6d 69 6e 69 73 74    ;   administ
            |  72 61 74 6f 72             ;   rator
            0c 07                         ; UTF8_STRING 
```

<span data-ttu-id="f30c7-108">Se o **conjunto** contiver menos de 128 bytes, o campo de **comprimento** do TLV terceto exigirá apenas um byte para especificar o comprimento do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f30c7-108">If the **SET** contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="f30c7-109">Se for maior que 127 bytes, o bit 7 do campo **comprimento** será definido como 1 e os bits 6 a 0 especificarão o número de bytes adicionais usados para identificar o tamanho do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f30c7-109">If it is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="f30c7-110">Para obter mais informações, consulte [comprimento codificado e bytes de valor](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="f30c7-110">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f30c7-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f30c7-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f30c7-112">Sistema de tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="f30c7-112">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="f30c7-113">Codificação DER dos tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="f30c7-113">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



