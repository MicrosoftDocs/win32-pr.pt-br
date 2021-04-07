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
# <a name="printablestring"></a>Imenablestring

O tipo de dados ASN. 1 **imenablestring** é codificado em um terceto TLV que começa com um byte de **marca** de 0x13. O exemplo a seguir, do [tópico \# ASN. 1 codificado em PKCS 10](pkcs--10-encoded-asn-1.md) , mostra como um nome comum de usuário de TestCN é codificado como um tipo **imprimível** . O identificador de objeto para um nome comum é 2.5.4.3.

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

Se a cadeia de caracteres contiver menos de 128 bytes, o campo de **comprimento** do TLV terceto exigirá apenas um byte para especificar o comprimento do conteúdo. Se a cadeia de caracteres tiver mais de 127 bytes, o bit 7 do campo **comprimento** será definido como 1 e os bits 6 a 0 especificarão o número de bytes adicionais usados para identificar o tamanho do conteúdo. Para obter mais informações, consulte [comprimento codificado e bytes de valor](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de tipo ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codificação DER dos tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



