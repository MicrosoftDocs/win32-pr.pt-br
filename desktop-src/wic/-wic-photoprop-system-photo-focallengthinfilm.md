---
description: A política de metadados de foto para a propriedade System. Photo. FocalLengthInFilm.
ms.assetid: 3ad63a7a-5ced-4e7f-a4a0-e1463f3d3fa3
title: Política de metadados de foto System. Photo. FocalLengthInFilm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df46f3e52c447cb7902fe3cce2da201dae16d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461305"
---
# <a name="systemphotofocallengthinfilm-photo-metadata-policy"></a>Política de metadados de foto System. Photo. FocalLengthInFilm

A política de metadados de foto para a propriedade [System. Photo. FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md) .

### <a name="pkey"></a>PKEY

PKEY \_ FocalLengthInFilm

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_UI4 VT

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41989}   | ushort      |
| 2     | /xmp/exif:FocalLengthIn35mmFilm | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41989}   | ushort      |
| 2     | /xmp/exif:FocalLengthIn35mmFilm | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                            |
|-------|---------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41989}   |
| 2     | /xmp/exif:focallengthin35mmfilm |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41989}            | ushort      |
| 2     | /ifd/xmp/exif:FocalLengthIn35mmFilm | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41989}            | ushort      |
| 2     | /ifd/xmp/exif:FocalLengthIn35mmFilm | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                |
|-------|-------------------------------------|
| 1     | /IFD/EXIF/{UShort = 41989}            |
| 2     | /ifd/xmp/exif:focallengthin35mmfilm |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
