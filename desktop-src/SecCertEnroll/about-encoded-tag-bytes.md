---
description: O campo Tag em um tlv triplet identifica o tipo da estrutura de dados que está sendo enviada entre computadores.
ms.assetid: 4723cc02-8c48-488e-95b8-c646a99b6aab
title: Bytes de marca codificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27face1fe04cf52c79d6c4047f87f58e98f2bc1a7b7656109341c9ce2be59d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904314"
---
# <a name="encoded-tag-bytes"></a>Bytes de marca codificados

O *campo Tag* em um tlv triplet identifica o tipo da estrutura de dados que está sendo enviada entre computadores. Por exemplo, a marca de um inteiro é 0x02 e a marca de um identificador de objeto é 0x06. Embora vários bytes sejam permitidos, nenhum dos tipos de dados usados pela API de Registro de Certificado exige mais de um. A ilustração a seguir mostra o detalhamento de um *valor tag.* Os bits 7 e 6 identificam a classe de marcação ASN.1. Há quatro classes disponíveis, mas a API de Registro de Certificado usa tipos de dados que pertencem somente à classe UNIVERSAL. O bit 5 identifica se o formulário de codificação é primitivo ou construído. Os tipos básicos e de cadeia de caracteres são codificados usando formas primitivas, tipos construídos usando um formulário construído. Para obter mais informações, consulte [Sistema de tipos ASN.1](about-asn-1-type-system.md). Os bits 4 a 0 contêm o número da marca.

![der tlv tag byte](images/der-tlv-tagbyte.png)

A tabela a seguir lista os tipos de dados com suporte pela API de Registro de Certificado, o formulário de codificação usado e o valor da marca.

| Tipo              | Classe ASN.1 | Formulário de codificação | Valor da marca                             |
|-------------------|-------------|---------------|---------------------------------------|
| CADEIA DE CARACTERES DE BITS        | Universal   | Primitivo     | 00000011<br/> (0x03)<br/> |
| BOOLEAN           | Universal   | Primitivo     | 00000001<br/> (0x01)<br/> |
| INTEGER           | Universal   | Primitivo     | 00000010<br/> (0x02)<br/> |
| NULO              | Universal   | Primitivo     | 00000101<br/> (0x05)<br/> |
| IDENTIFICADOR DE OBJETO | Universal   | Primitivo     | 00000110<br/> (0x06)<br/> |
| CADEIA DE CARACTERES OCTETO      | Universal   | Primitivo     | 00000100<br/> (0x04)<br/> |
| BMPString         | Universal   | Primitivo     | 00011110<br/> (0x1E)<br/> |
| IA5String         | Universal   | Primitivo     | 00010110<br/> (0x16)<br/> |
| PrintableString   | Universal   | Primitivo     | 00010011<br/> (0x13)<br/> |
| TeletexString     | Universal   | Primitivo     | 00010100<br/> (0x14)<br/> |
| Utf8string        | Universal   | Primitivo     | 00001100<br/> (0x0C)<br/> |
| SEQUENCE          | Universal   | Construído   | 00110000<br/> (0x30)<br/> |
| SEQUÊNCIA DE       | Universal   | Construído   | 00110000<br/> (0x30)<br/> |
| SET               | Universal   | Construído   | 00110001<br/> (0x31)<br/> |
| SET OF            | Universal   | Construído   | 00110001<br/> (0x31)<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe de transferência de DER](about-der-transfer-syntax.md)
</dt> <dt>

[Bytes de comprimento e valor codificados](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 




