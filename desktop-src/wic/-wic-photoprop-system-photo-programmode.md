---
description: A política de metadados de foto para a propriedade System.Photo.ProgramMode.
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: Política de metadados de foto System.Photo.ProgramMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260bf4ae5ca26fa26848765a76f5fdbc36eef48e2806909f46e5ab256f5acd7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032496"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a>Política de metadados de foto System.Photo.ProgramMode

A política de metadados de foto para a [propriedade System.Photo.ProgramMode.](../properties/props-system-photo-programmode.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ ProgramMode

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ UI4

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=34850} | ushort      |
| 2     | /xmp/exif:ExposureProgram     | Unicode     |
| 3     | /xmp/exif:ProgramMode         | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=34850} | ushort      |
| 2     | /xmp/exif:ExposureProgram     | Unicode     |
| 3     | /xmp/exif:ProgramMode         | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=34850} |
| 2     | /xmp/exif:exposureprogram     |
| 3     | /xmp/exif:programmode         |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort=34850}      | ushort      |
| 2     | /ifd/xmp/exif:ExposureProgram | Unicode     |
| 3     | /ifd/xmp/exif:ProgramMode     | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort=34850}      | ushort      |
| 2     | /ifd/xmp/exif:ExposureProgram | Unicode     |
| 3     | /ifd/xmp/exif:ProgramMode     | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /ifd/exif/{ushort=34850}      |
| 2     | /ifd/xmp/exif:exposureprogram |
| 3     | /ifd/xmp/exif:programmode     |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Photo.ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
