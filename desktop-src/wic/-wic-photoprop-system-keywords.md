---
description: A política de metadados de foto para a propriedade System. Keywords.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: Política de metadados de foto System. Keywords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5d25e7f1919527d474395397d6df62863f7b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171318"
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



| Ordem | Caminho                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /XMP/ <xmpbag> DC: subject     | Unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords |                |
| 3     | /App1/IFD/{UShort = 18247}          | \_bytes Unicode |
| 4     | /App1/IFD/{UShort = 40094}          | \_bytes Unicode |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                                              | Formato de disco    |
|-------|---------------------------------------------------|----------------|
| 1     | /XMP/ <xmpbag> DC: subject                     | Unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |                |
| 3     | /App1/IFD/{UShort = 18247}                          | \_bytes Unicode |
| 4     | /App1/IFD/{UShort = 40094}                          | \_bytes Unicode |
| 5     | /XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP  | Unicode        |
| 6     | /XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC | Unicode        |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                              |
|-------|---------------------------------------------------|
| 1     | /XMP/DC: assunto                                   |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |
| 3     | /App1/IFD/{UShort = 18247}                          |
| 4     | /App1/IFD/{UShort = 40094}                          |
| 5     | /XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP  |
| 6     | /XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/XMP/ <xmpbag> DC: subject | Unicode        |
| 2     | /ifd/iptc/keywords                |                |
| 3     | /IFD/{UShort = 18247}               | \_bytes Unicode |
| 4     | /IFD/{UShort = 40094}               | \_bytes Unicode |
| 5     | /ifd/irb/8bimiptc/iptc/keywords   |                |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                                                             | Formato de disco    |
|-------|------------------------------------------------------------------|----------------|
| 1     | /IFD/XMP/ <xmpbag> DC: subject                                | Unicode        |
| 2     | /ifd/iptc/keywords                                               |                |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |                |
| 4     | /IFD/{UShort = 18247}                                              | \_bytes Unicode |
| 5     | /IFD/{UShort = 40094}                                              | \_bytes Unicode |
| 6     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP             | Unicode        |
| 7     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC            | Unicode        |
| 8     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC \_ TIFF \_ IRB | Unicode        |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                                             |
|-------|------------------------------------------------------------------|
| 1     | /IFD/XMP/DC: assunto                                              |
| 2     | /ifd/iptc/keywords                                               |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |
| 4     | /IFD/{UShort = 18247}                                              |
| 5     | /IFD/{UShort = 40094}                                              |
| 6     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP             |
| 7     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC            |
| 8     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC \_ TIFF \_ IRB |



 

### <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Keywords](../properties/props-system-keywords.md)
</dt> </dl>

 

 
