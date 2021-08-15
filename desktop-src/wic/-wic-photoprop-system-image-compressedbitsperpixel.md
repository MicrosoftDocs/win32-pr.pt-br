---
description: A política de metadados de foto para a propriedade System.Image.CompressedBitsPerPixel.
ms.assetid: e97a5c68-6d4a-44af-8096-22680f8b16b8
title: Política de metadados de foto System.Image.CompressedBitsPerPixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a18cc76e22c5c409e19e08fc5a2e667ad374348bc753ffa85cd09003a8bdaf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032705"
---
# <a name="systemimagecompressedbitsperpixel-photo-metadata-policy"></a>Política de metadados de foto System.Image.CompressedBitsPerPixel

A política de metadados de foto para a [propriedade System.Image.CompressedBitsPerPixel.](../properties/props-system-image-compressedbitsperpixel.md)

### <a name="pkey"></a>Pkey

Imagem PKEY \_ \_ CompressedBitsPerPixel

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Sim

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ R8

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Esse valor é gerado de System.Image.CompressedBitsPerPixelNumerator e System.Image.CompressedBitsPerPixelDenominator. Ele não pode ser gravado diretamente. Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37122}    |             |
| 2     | /xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                             |
|-------|----------------------------------|
| 1     | /app1/ifd/exif/{ushort=37122}    |
| 2     | /xmp/exif:compressedbitsperpixel |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                                 | Formato de disco |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37122}             |             |
| 2     | /ifd/xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                 |
|-------|--------------------------------------|
| 1     | /ifd/exif/{ushort=37122}             |
| 2     | /ifd/xmp/exif:compressedbitsperpixel |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Image.CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md)
</dt> </dl>

 

 
