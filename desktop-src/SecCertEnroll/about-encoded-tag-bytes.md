---
description: O campo de marca em um TLV terceto identifica o tipo da estrutura de dados que está sendo enviada entre computadores.
ms.assetid: 4723cc02-8c48-488e-95b8-c646a99b6aab
title: Bytes de marca codificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5994f7beea0aba6896e94cb992a1e72eb70914
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566791"
---
# <a name="encoded-tag-bytes"></a>Bytes de marca codificados

O campo de *marca* em um TLV terceto identifica o tipo da estrutura de dados que está sendo enviada entre computadores. Por exemplo, a marca de um inteiro é 0x02 e a marca para um identificador de objeto é 0x06. Embora vários bytes sejam permitidos, nenhum dos tipos de dados usados pela API de registro de certificado exigem mais de um. A ilustração a seguir mostra a divisão de um valor de *marca* . O bits 7 e 6 identificam a classe de marcação ASN. 1. Há quatro classes disponíveis, mas a API de registro de certificado usa tipos de dados que pertencem somente à classe UNIVERSAL. O bit 5 identifica se o formulário de codificação é primitivo ou construído. Os tipos básico e de cadeia de caracteres são codificados usando formulários primitivos, tipos construídos usando um formulário construído. Para obter mais informações, consulte [sistema ASN. 1 tipo](about-asn-1-type-system.md). O bits 4 a 0 contém o número da marca.

![byte de marca TLV der](images/der-tlv-tagbyte.png)

A tabela a seguir lista os tipos de dados com suporte pela API de registro de certificado, o formulário de codificação usado e o valor da marca.

| Tipo              | Classe ASN. 1 | Formulário de codificação | Valor da marca                             |
|-------------------|-------------|---------------|---------------------------------------|
| CADEIA DE BITS        | UNIVERSAL   | Primitiva     | 00000011<br/> 0x03<br/> |
| BOOLEAN           | UNIVERSAL   | Primitiva     | 00000001<br/> 0x01<br/> |
| INTEGER           | UNIVERSAL   | Primitiva     | 00000010<br/> 0x02<br/> |
| NULO              | UNIVERSAL   | Primitiva     | 00000101<br/> (0x05)<br/> |
| IDENTIFICADOR DE OBJETO | UNIVERSAL   | Primitiva     | 00000110<br/> (0x06)<br/> |
| CADEIA DE CARACTERES DE OCTETO      | UNIVERSAL   | Primitiva     | 00000100<br/> 0x04<br/> |
| BMPString         | UNIVERSAL   | Primitiva     | 00011110<br/> 0X1E<br/> |
| IA5String         | UNIVERSAL   | Primitiva     | 00010110<br/> (0x16)<br/> |
| Imenablestring   | UNIVERSAL   | Primitiva     | 00010011<br/> (0x13)<br/> |
| TeletexString     | UNIVERSAL   | Primitiva     | 00010100<br/> (0x14)<br/> |
| UTF8String        | UNIVERSAL   | Primitiva     | 00001100<br/> (0x0C)<br/> |
| SEQUENCE          | UNIVERSAL   | Construído   | 00110000<br/> (0x30)<br/> |
| SEQUÊNCIA DE       | UNIVERSAL   | Construído   | 00110000<br/> (0x30)<br/> |
| SET               | UNIVERSAL   | Construído   | 00110001<br/> 0x31<br/> |
| CONJUNTO DE            | UNIVERSAL   | Construído   | 00110001<br/> 0x31<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe de transferência de DER](about-der-transfer-syntax.md)
</dt> <dt>

[Comprimento codificado e bytes de valor](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 




