---
description: A política de metadados de foto para a propriedade System. Author.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: Política de metadados de fotos do System. Author
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90345257ef1623f7cda1ce4318af7a9f472df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105795467"
---
# <a name="systemauthor-photo-metadata-policy"></a>Política de metadados de fotos do System. Author

A política de metadados de foto para a propriedade [System. Author](../properties/props-system-author.md) .

### <a name="pkey"></a>PKEY

Autor do PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_LPWStr do vetor VT VT \| \_

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

O \_ \| LPWSTR de vetor VT do VT \_ é preferencial, mas o o LPWStr do VT \_ também é aceito.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                             | Formato de disco    |
|-------|----------------------------------|----------------|
| 1     | /App1/IFD/{UShort = 315}           | ascii          |
| 2     | /app13/irb/8bimiptc/iptc/by-line |                |
| 3     | /XMP/ <xmpseq> DC: Creator    | Unicode        |
| 4     | /app13/irb/8bimiptc/iptc/by-line |                |
| 5     | /App1/IFD/{UShort = 40093}         | \_bytes Unicode |
| 6     | /XMP/TIFF: artista                 | Unicode        |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                             | Formato de disco    |
|-------|----------------------------------|----------------|
| 1     | /XMP/ <xmpseq> DC: Creator    | Unicode        |
| 2     | /XMP/TIFF: artista                 | Unicode        |
| 3     | /app13/irb/8bimiptc/iptc/by-line |                |
| 4     | /App1/IFD/{UShort = 315}           | ascii          |
| 5     | /App1/IFD/{UShort = 40093}         | \_bytes Unicode |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                             |
|-------|----------------------------------|
| 1     | /XMP/DC: criador                  |
| 2     | /XMP/TIFF: artista                 |
| 3     | /app13/irb/8bimiptc/iptc/by-line |
| 4     | /App1/IFD/{UShort = 315}           |
| 5     | /App1/IFD/{UShort = 40093}         |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/{UShort = 315}                 | ascii          |
| 2     | /ifd/iptc/by-line                 |                |
| 3     | /IFD/XMP/ <xmpseq> DC: Creator | Unicode        |
| 4     | /ifd/iptc/by-line                 |                |
| 5     | /IFD/{UShort = 40093}               | \_bytes Unicode |
| 6     | /ifd/irb/8bimiptc/iptc/by-line    |                |
| 7     | /IFD/XMP/TIFF: artista              | Unicode        |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/XMP/ <xmpseq> DC: Creator | Unicode        |
| 2     | /IFD/XMP/TIFF: artista              | Unicode        |
| 3     | /ifd/iptc/by-line                 |                |
| 4     | /IFD/{UShort = 315}                 | \_vetor ASCII  |
| 5     | /IFD/{UShort = 40093}               | \_bytes Unicode |
| 6     | /ifd/iptc/by-line                 |                |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                           |
|-------|--------------------------------|
| 1     | /IFD/XMP/DC: criador            |
| 2     | /IFD/XMP/TIFF: artista           |
| 3     | /ifd/iptc/by-line              |
| 4     | /ifd/irb/8bimiptc/iptc/by-line |
| 5     | /IFD/{UShort = 315}              |
| 6     | /IFD/{UShort = 40093}            |



 

### <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Author](../properties/props-system-author.md)
</dt> </dl>

 

 
