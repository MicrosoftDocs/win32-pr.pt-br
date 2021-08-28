---
description: A política de metadados de foto para a propriedade System.Photo.Flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Política de metadados de foto System.Photo.Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7798e88c40193cac5c577f1960eee96fc2d868
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880079"
---
# <a name="systemphotoflash-photo-metadata-policy"></a>Política de metadados de foto System.Photo.Flash

A política de metadados de foto para a [propriedade System.Photo.Flash.](../properties/props-system-photo-exposuretime.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ Flash

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT UI1 (se o esquema de origem \_ fosse XMP) ou VT UI2 (se o esquema \_ de origem fosse EXIF)

\\lang1036

### <a name="input-type"></a>Tipo de entrada

VT \_ UI1, VTUI2, VT \_ UI4

\\lang1033

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Order | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37385}    | ushort      |
| 2     | /xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Order | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37385}    | ushort      |
| 2     | /xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Order | Caminho                             |
|-------|----------------------------------|
| 1     | /app1/ifd/exif/{ushort=37385}    |
| 2     | /xmp/ &lt; xmpstruct &gt; exif:flash |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Order | Caminho                                 | Formato de disco |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37385}             | ushort      |
| 2     | /ifd/xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Order | Caminho                                 | Formato de disco |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37385}             | ushort      |
| 2     | /ifd/xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Order | Caminho                                 |
|-------|--------------------------------------|
| 1     | /ifd/exif/{ushort=37385}             |
| 2     | /ifd/xmp/ &lt; xmpstruct &gt; exif:flash |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Photo.Flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
