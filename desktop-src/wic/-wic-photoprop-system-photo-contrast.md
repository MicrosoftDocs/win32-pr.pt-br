---
description: A política de metadados de foto para a propriedade System.Photo.Contrast.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: Política de metadados de foto System.Photo.Contrast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a9309ecab96a2244e08ebf05ff8896c792f7366c9db21d41072d2d94aacf47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087092"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a>Política de metadados de foto System.Photo.Contrast

A política de metadados de foto para a [propriedade System.Photo.Contrast.](../properties/props-system-photo-contrast.md)

### <a name="pkey"></a>Pkey

Contraste de \_ fotos PKEY \_

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
| 1     | /app1/ifd/exif/{ushort=41992} | ushort      |
| 2     | /xmp/exif:Contrast            | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41992} | ushort      |
| 2     | /xmp/exif:Contrast            | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=41992} |
| 2     | /xmp/exif:contrast            |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41992} | ushort      |
| 2     | /ifd/xmp/exif:Contrast   | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41992} | ushort      |
| 2     | /ifd/xmp/exif:Contrast   | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=41992} |
| 2     | /ifd/xmp/exif:contrast   |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Photo.Contrast](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
