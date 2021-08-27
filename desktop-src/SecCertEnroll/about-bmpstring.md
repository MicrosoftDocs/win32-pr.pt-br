---
description: O tipo de dados BMPString ASN.1, chamado DE CADEIA DE CARACTERES UNICODE na API de Registro de Certificado, é codificado em um tripleto TLV que começa com um byte tag de \_ 0x1E.
ms.assetid: 66e4a6d8-2401-4346-9361-e145735cbe19
title: BMPString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 496715d380739dd68dab4266422876ecca174b9caffd3895e9c465f446d32cf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904835"
---
# <a name="bmpstring"></a>BMPString

O tipo de dados ASN.1 **BMPString,** chamado cadeia de caracteres **UNICODE \_** na API de Registro de Certificado, é codificado em um tripleto TLV que começa com um **byte** tag de 0x1E. O exemplo a seguir, adaptado do tópico [ASN.1](cmc-encoded-asn-1.md) codificado em CMC, mostra a codificação para uma **extensão TemplateName.** O nome pode ser especificado usando a interface [**IX509ExtensionTemplateName.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename) O identificador de objeto para a extensão é 1.3.6.1.4.1.311.13.2.1.

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

Se a cadeia de caracteres contiver menos de 128 bytes, o campo Comprimento do tlv triplet exigirá apenas um byte para especificar o comprimento do conteúdo.  Se a cadeia de caracteres for maior que  127 bytes, o bit 7 do campo Comprimento será definido como 1 e os bits 6 a 0 especificarão o número de bytes adicionais usados para identificar o comprimento do conteúdo. Para obter mais informações, consulte [Bytes de comprimento e valor codificados.](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de tipos ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificação DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



