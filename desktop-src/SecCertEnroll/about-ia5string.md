---
description: O tipo de dados ASN. 1 IA5tring é codificado em um terceto TLV que começa com um byte de marca de 0x16.
ms.assetid: c1268524-4304-4c21-8f7d-f0a2826cd74e
title: IA5String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7562fab655462455b03d35041bdb8f572b064cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169496"
---
# <a name="ia5string"></a>IA5String

O tipo de dados ASN. 1 **IA5tring** é codificado em um terceto TLV que começa com um byte de **marca** de 0x16. O exemplo a seguir, adaptado do tópico [ASN codificado por CMC. 1](cmc-encoded-asn-1.md) , mostra como o atributo **OSVersion** é codificado como um tipo **IA5tring** . O número de versão pode ser especificado usando a interface [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) . O identificador de objeto para o atributo é 1.3.6.1.4.1.311.13.2.3.

``` syntax
06 0a                                   ; OBJECT_ID (a Bytes)
|  2b 06 01 04 01 82 37 0d  02 03       ;   1.3.6.1.4.1.311.13.2.3 
31 0c                                   ; SET (c Bytes)
   16 0a                                ; IA5_STRING (a Bytes)
      36 2e 30 2e 35 33 36 31  2e 32    ;   6.0.5361.2
```

Se a cadeia de caracteres contiver menos de 128 bytes, o campo de **comprimento** do TLV terceto exigirá apenas um byte para especificar o comprimento do conteúdo. Se a cadeia de caracteres tiver mais de 127 bytes, o bit 7 do campo **comprimento** será definido como 1 e os bits 6 a 0 especificarão o número de bytes adicionais usados para identificar o tamanho do conteúdo. Para obter mais informações, consulte [comprimento codificado e bytes de valor](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de tipo ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codificação DER dos tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



