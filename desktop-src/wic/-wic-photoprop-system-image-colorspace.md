---
description: A política de metadados de foto para a propriedade System. Image. ColorSpace.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: Política de metadados de foto System. Image. ColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c7d7c9134a8bd93a12ba6cfb6bd8605e228cb6b745ad4401a94f91a2ba9ff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710416"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a>Política de metadados de foto System. Image. ColorSpace

A política de metadados de foto para a propriedade [System. Image. colorspace](../properties/props-system-image-colorspace.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Image \_ colorspace

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Sim

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

 

 
