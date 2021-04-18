---
description: A política de metadados de foto para a propriedade System. Image. CompressedBitsPerPixel.
ms.assetid: e97a5c68-6d4a-44af-8096-22680f8b16b8
title: Política de metadados de foto System. Image. CompressedBitsPerPixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45b3b1e8b29cdf992cd3b451a2e8a43947139a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810828"
---
# <a name="systemimagecompressedbitsperpixel-photo-metadata-policy"></a>Política de metadados de foto System. Image. CompressedBitsPerPixel

A política de metadados de foto para a propriedade [System. Image. CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Image \_ CompressedBitsPerPixel

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

R8 de VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor é gerado de System. Image. CompressedBitsPerPixelNumerator e System. Image. CompressedBitsPerPixelDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37122}    |             |
| 2     | /xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                             |
|-------|----------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37122}    |
| 2     | /xmp/exif:compressedbitsperpixel |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                 | Formato de disco |
|-------|--------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37122}             |             |
| 2     | /ifd/xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                 |
|-------|--------------------------------------|
| 1     | /IFD/EXIF/{UShort = 37122}             |
| 2     | /ifd/xmp/exif:compressedbitsperpixel |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Image. CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md)
</dt> </dl>

 

 
