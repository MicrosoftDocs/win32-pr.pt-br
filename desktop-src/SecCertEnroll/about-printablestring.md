---
description: O tipo de dados PrintableString asN.1 é codificado em um tripleto TLV que começa com um byte tag de 0x13.
ms.assetid: 998fef66-7a24-462f-96f2-92c739bbefa2
title: PrintableString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e2714013c037e834a7c083c7ab89fcdafd59e1306226af25fcb4b6edc8b0af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903741"
---
# <a name="printablestring"></a>PrintableString

O tipo de dados **PrintableString** asN.1 é codificado em um tripleto TLV que começa com um **byte** tag de 0x13. O exemplo a seguir, do tópico [ \# ASN.1 codificado em PKCS 10,](pkcs--10-encoded-asn-1.md) mostra como um nome comum do usuário testCN é codificado como um **tipo PrintableString.** O identificador de objeto para um nome comum é 2.5.4.3.

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

Se a cadeia de caracteres contiver menos de 128 bytes, o campo Comprimento do tlv triplet exigirá apenas um byte para especificar o comprimento do conteúdo.  Se a cadeia de caracteres for maior que  127 bytes, o bit 7 do campo Comprimento será definido como 1 e os bits 6 a 0 especificarão o número de bytes adicionais usados para identificar o comprimento do conteúdo. Para obter mais informações, consulte [Bytes de comprimento e valor codificados.](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de tipos ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificação DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



