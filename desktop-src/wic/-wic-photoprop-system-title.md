---
description: A política de metadados de foto para a propriedade System.Title.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: Política de metadados de foto System.Title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa43b31595928fa3c2c936de8710131c20f17b1a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880690"
---
# <a name="systemtitle-photo-metadata-policy"></a>Política de metadados de foto System.Title

A política de metadados de foto para a [propriedade System.Title.](../properties/props-system-title.md)

### <a name="pkey"></a>PKEY

Título \_ de PKEY

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

VT \_ LPWSTR ou VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Order | Caminho                                | Formato de disco    |
|-------|-------------------------------------|----------------|
| 1     | /app1/ifd/{ushort=40091}            | Bytes \_ unicode |
| 2     | /xmp/ &lt; xmpalt &gt; dc:title         | Unicode        |
| 3     | /xmp/dc:title                       | Unicode        |
| 4     | /app1/ifd/exif/{ushort=37510}       | Unicode        |
| 5     | /app1/ifd/{ushort=270}              | ascii          |
| 6     | /app13/irb/8bimiptc/iptc/caption    |                |
| 7     | /xmp/ &lt; xmpalt &gt; dc:description   | Unicode        |
| 8     | /xmp/dc:description                 | Unicode        |
| 9     | /app13/irb/8bimiptc/iptc/caption    |                |
| 10    | /xmp/ &lt; xmpalt &gt; exif:UserComment | Unicode        |



 

### <a name="write-paths"></a>Caminhos de gravação



| Order | Caminho                                | Formato de disco    |
|-------|-------------------------------------|----------------|
| 1     | /app1/ifd/{ushort=40091}            | Bytes \_ unicode |
| 2     | /xmp/dc:title                       | Unicode        |
| 3     | /xmp/ &lt; xmpalt &gt; dc:title         | Unicode        |
| 4     | /app1/ifd/exif/{ushort=37510}       | Unicode        |
| 5     | /xmp/ &lt; xmpalt &gt; exif:UserComment | Unicode        |
| 6     | /app1/ifd/{ushort=270}              | ascii          |
| 7     | /app13/irb/8bimiptc/iptc/caption    |                |
| 8     | /xmp/dc:description                 | Unicode        |
| 9     | /xmp/ &lt; xmpalt &gt; dc:description   | Unicode        |



 

### <a name="remove-paths"></a>Remover caminhos



| Order | Caminho                                |
|-------|-------------------------------------|
| 1     | /app1/ifd/{ushort=40091}            |
| 2     | /xmp/dc:title                       |
| 3     | /app1/ifd/exif/{ushort=37510}       |
| 4     | /xmp/ &lt; xmpalt &gt; exif:UserComment |
| 5     | /app1/ifd/{ushort=270}              |
| 6     | /app13/irb/8bimiptc/iptc/caption    |
| 7     | /xmp/dc:description                 |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Ler caminhos



| Order | Caminho                                    | Formato de disco    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{UShort = 40091}                     | \_bytes Unicode |
| 2     | /IFD/XMP/ &lt; xmpalt &gt; DC: title         | Unicode        |
| 3     | /IFD/XMP/DC: título                       | Unicode        |
| 4     | /IFD/EXIF/{UShort = 37510}                | Unicode        |
| 5     | /IFD/{UShort = 270}                       | ascii          |
| 6     | /ifd/iptc/caption                       |                |
| 7     | /IFD/XMP/ &lt; xmpalt &gt; DC: Descrição   | Unicode        |
| 8     | /IFD/XMP/DC: Descrição                 | Unicode        |
| 9     | /ifd/iptc/caption                       |                |
| 10    | /ifd/irb/8bimiptc/iptc/caption          |                |
| 11    | /IFD/XMP/ &lt; xmpalt &gt; EXIF: UserComment | Unicode        |



 

### <a name="write-paths"></a>Caminhos de gravação



| Order | Caminho                                    | Formato de disco    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{UShort = 40091}                     | \_bytes Unicode |
| 2     | /IFD/XMP/DC: título                       | Unicode        |
| 3     | /IFD/XMP/ &lt; xmpalt &gt; DC: title         | Unicode        |
| 4     | /IFD/EXIF/{UShort = 37510}                | Unicode        |
| 5     | /IFD/XMP/ &lt; xmpalt &gt; EXIF: UserComment | Unicode        |
| 6     | /IFD/{UShort = 270}                       | ascii          |
| 7     | /ifd/iptc/caption                       |                |
| 8     | /ifd/irb/8bimiptc/iptc/caption          |                |
| 9     | /IFD/XMP/DC: Descrição                 | Unicode        |
| 10    | /IFD/XMP/ &lt; xmpalt &gt; DC: Descrição   | Unicode        |



 

### <a name="remove-paths"></a>Remover caminhos



| Order | Caminho                                    |
|-------|-----------------------------------------|
| 1     | /IFD/{UShort = 40091}                     |
| 2     | /IFD/XMP/DC: título                       |
| 3     | /IFD/EXIF/{UShort = 37510}                |
| 4     | /IFD/XMP/ &lt; xmpalt &gt; EXIF: UserComment |
| 5     | /IFD/{UShort = 270}                       |
| 6     | /ifd/iptc/caption                       |
| 7     | /ifd/irb/8bimiptc/iptc/caption          |
| 8     | /IFD/XMP/DC: Descrição                 |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Title](../properties/props-system-title.md)
</dt> </dl>

 

 
