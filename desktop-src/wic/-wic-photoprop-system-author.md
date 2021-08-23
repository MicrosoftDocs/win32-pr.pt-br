---
description: A política de metadados de foto para a propriedade System.Author.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: Política de metadados de foto System.Author
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b898f450fe1d370f94a9be2922eb650db47ac8c2e414c27d9eede23f0dada276
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087998"
---
# <a name="systemauthor-photo-metadata-policy"></a>Política de metadados de foto System.Author

A política de metadados de foto para a [propriedade System.Author.](../properties/props-system-author.md)

### <a name="pkey"></a>Pkey

Autor \_ de PKEY

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ VECTOR \| VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

O VT \_ VECTOR \| VT \_ LPWSTR é preferencial, mas o VT \_ LPWSTR também é aceito.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                             | Formato de disco    |
|-------|----------------------------------|----------------|
| 1     | /app1/ifd/{ushort=315}           | ascii          |
| 2     | /app13/irb/8bimiptc/iptc/by-line |                |
| 3     | /xmp/ <xmpseq> dc:creator    | Unicode        |
| 4     | /app13/irb/8bimiptc/iptc/by-line |                |
| 5     | /app1/ifd/{ushort=40093}         | Bytes \_ unicode |
| 6     | /xmp/tiff:artist                 | Unicode        |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                             | Formato de disco    |
|-------|----------------------------------|----------------|
| 1     | /xmp/ <xmpseq> dc:creator    | Unicode        |
| 2     | /xmp/tiff:artist                 | Unicode        |
| 3     | /app13/irb/8bimiptc/iptc/by-line |                |
| 4     | /app1/ifd/{ushort=315}           | ascii          |
| 5     | /app1/ifd/{ushort=40093}         | Bytes \_ unicode |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                             |
|-------|----------------------------------|
| 1     | /xmp/dc:creator                  |
| 2     | /xmp/tiff:artist                 |
| 3     | /app13/irb/8bimiptc/iptc/by-line |
| 4     | /app1/ifd/{ushort=315}           |
| 5     | /app1/ifd/{ushort=40093}         |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /ifd/{ushort=315}                 | ascii          |
| 2     | /ifd/iptc/by-line                 |                |
| 3     | /ifd/xmp/ <xmpseq> dc:creator | Unicode        |
| 4     | /ifd/iptc/by-line                 |                |
| 5     | /ifd/{ushort=40093}               | Bytes \_ unicode |
| 6     | /ifd/irb/8bimiptc/iptc/by-line    |                |
| 7     | /ifd/xmp/tiff:artist              | Unicode        |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /ifd/xmp/ <xmpseq> dc:creator | Unicode        |
| 2     | /ifd/xmp/tiff:artist              | Unicode        |
| 3     | /ifd/iptc/by-line                 |                |
| 4     | /ifd/{ushort=315}                 | vetor \_ ascii  |
| 5     | /ifd/{ushort=40093}               | Bytes \_ unicode |
| 6     | /ifd/iptc/by-line                 |                |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                           |
|-------|--------------------------------|
| 1     | /ifd/xmp/dc:creator            |
| 2     | /ifd/xmp/tiff:artist           |
| 3     | /ifd/iptc/by-line              |
| 4     | /ifd/irb/8bimiptc/iptc/by-line |
| 5     | /ifd/{ushort=315}              |
| 6     | /ifd/{ushort=40093}            |



 

### <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Author](../properties/props-system-author.md)
</dt> </dl>

 

 
