---
description: A política de metadados de foto para a propriedade System. Keywords.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: Política de metadados de foto System. Keywords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa5387bfb8cca7fffe83f7615a979d8e23ae890
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886645"
---
# <a name="systemkeywords-photo-metadata-policy"></a>Política de metadados de foto System. Keywords

A política de metadados de foto para a propriedade [System. Keywords](../properties/props-system-keywords.md) .

### <a name="pkey"></a>PKEY

\_Palavras-chave PKEY

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_LPWStr do vetor VT VT \| \_

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

O \_ LPWSTR de vetor \| VT VT \_ é preferencial. Um \_ LPWSTR VT contendo uma cadeia de caracteres delimitada por ponto e vírgula também é aceito.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Valores de esquemas diferentes são mesclados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Order | Caminho                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /XMP/ &lt; xmpbag &gt; DC: subject     | Unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords |                |
| 3     | /App1/IFD/{UShort = 18247}          | \_bytes Unicode |
| 4     | /App1/IFD/{UShort = 40094}          | \_bytes Unicode |



 

### <a name="write-paths"></a>Caminhos de gravação



| Order | Caminho                                              | Formato de disco    |
|-------|---------------------------------------------------|----------------|
| 1     | /XMP/ &lt; xmpbag &gt; DC: subject                     | Unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |                |
| 3     | /App1/IFD/{UShort = 18247}                          | \_bytes Unicode |
| 4     | /App1/IFD/{UShort = 40094}                          | \_bytes Unicode |
| 5     | /XMP/ &lt; xmpbag &gt; MicrosoftPhoto: LastKeywordXMP  | Unicode        |
| 6     | /XMP/ &lt; xmpbag &gt; MicrosoftPhoto: LastKeywordIPTC | Unicode        |



 

### <a name="remove-paths"></a>Remover caminhos



| Order | Caminho                                              |
|-------|---------------------------------------------------|
| 1     | /XMP/DC: assunto                                   |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |
| 3     | /App1/IFD/{UShort = 18247}                          |
| 4     | /App1/IFD/{UShort = 40094}                          |
| 5     | /XMP/ &lt; xmpbag &gt; MicrosoftPhoto: LastKeywordXMP  |
| 6     | /XMP/ &lt; xmpbag &gt; MicrosoftPhoto: LastKeywordIPTC |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Order | Caminho                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/XMP/ &lt; xmpbag &gt; DC: subject | Unicode        |
| 2     | /ifd/iptc/keywords                |                |
| 3     | /IFD/{UShort = 18247}               | \_bytes Unicode |
| 4     | /IFD/{UShort = 40094}               | \_bytes Unicode |
| 5     | /ifd/irb/8bimiptc/iptc/keywords   |                |



 

### <a name="write-paths"></a>Caminhos de gravação



| Order | Caminho                                                             | Formato de disco    |
|-------|------------------------------------------------------------------|----------------|
| 1     | /IFD/XMP/ &lt; xmpbag &gt; DC: subject                                | Unicode        |
| 2     | /ifd/iptc/keywords                                               |                |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |                |
| 4     | /IFD/{UShort = 18247}                                              | Bytes \_ unicode |
| 5     | /ifd/{ushort=40094}                                              | Bytes \_ unicode |
| 6     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordXMP             | Unicode        |
| 7     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC            | Unicode        |
| 8     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC \_ TIFF \_ IRB | Unicode        |



 

### <a name="remove-paths"></a>Remover caminhos



| Order | Caminho                                                             |
|-------|------------------------------------------------------------------|
| 1     | /ifd/xmp/dc:subject                                              |
| 2     | /ifd/iptc/keywords                                               |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |
| 4     | /ifd/{ushort=18247}                                              |
| 5     | /ifd/{ushort=40094}                                              |
| 6     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordXMP             |
| 7     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC            |
| 8     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC \_ TIFF \_ IRB |



 

### <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Keywords](../properties/props-system-keywords.md)
</dt> </dl>

 

 
