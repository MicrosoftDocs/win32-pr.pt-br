---
description: A política de metadados de foto para a propriedade System. Image. ColorSpace.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: Política de metadados de foto System. Image. ColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6ef2003d05fa19b958b28950f71ec2d5f73027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760580"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a>Política de metadados de foto System. Image. ColorSpace

A política de metadados de foto para a propriedade [System. Image. colorspace](../properties/props-system-image-colorspace.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Image \_ colorspace

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_UI2 VT

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 40961} | ushort      |
| 2     | /xmp/exif:ColorSpace          | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 40961} | ushort      |
| 2     | /xmp/exif:ColorSpace          | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 40961} |
| 2     | /xmp/exif:colorspace          |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 40961} | ushort      |
| 2     | /ifd/xmp/exif:ColorSpace | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 40961} | ushort      |
| 2     | /ifd/xmp/exif:ColorSpace | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{UShort = 40961} |
| 2     | /ifd/xmp/exif:colorspace |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Image. ColorSpace](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
