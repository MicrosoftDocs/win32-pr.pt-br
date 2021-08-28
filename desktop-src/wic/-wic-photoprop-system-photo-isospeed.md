---
description: A política de metadados de foto para a propriedade System.Photo.ISOSpeed.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Política de metadados de foto System.Photo.ISOSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6612bffdeaafb69ea1b1122a1d75c00214d366e9
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881635"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a>Política de metadados de foto System.Photo.ISOSpeed

A política de metadados de foto para a [propriedade System.Photo.ISOSpeed.](../properties/props-system-photo-focallengthinfilm.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ ISOSpeed

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ UI2

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Order | Caminho                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=34855}           | ushort      |
| 2     | /xmp/ &lt; xmpseq &gt; exif:ISOSpeedRatings | Unicode     |
| 3     | /xmp/exif:ISOSpeed                      | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Order | Caminho                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=34855}           | ushort      |
| 2     | /xmp/ &lt; xmpseq &gt; exif:ISOSpeedRatings | Unicode     |
| 3     | /xmp/exif:ISOSpeed                      | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Order | Caminho                                    |
|-------|-----------------------------------------|
| 1     | /app1/ifd/exif/{ushort=34855}           |
| 2     | /xmp/ &lt; xmpseq &gt; exif:isospeedratings |
| 3     | /xmp/exif:isospeed                      |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Order | Caminho                                        | Formato de disco |
|-------|---------------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=34855}                    | ushort      |
| 2     | /ifd/xmp/ &lt; xmpseq &gt; exif:ISOSpeedRatings | Unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Order | Caminho                                        | Formato de disco |
|-------|---------------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=34855}                    | ushort      |
| 2     | /ifd/xmp/ &lt; xmpseq &gt; exif:ISOSpeedRatings | Unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Order | Caminho                                        |
|-------|---------------------------------------------|
| 1     | /ifd/exif/{ushort=34855}                    |
| 2     | /ifd/xmp/ &lt; xmpseq &gt; exif:isospeedratings |
| 3     | /ifd/xmp/exif:isospeed                      |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Photo.ISOSpeed](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
