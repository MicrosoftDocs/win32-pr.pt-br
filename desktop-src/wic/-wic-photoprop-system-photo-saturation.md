---
description: A política de metadados de foto para a propriedade System.Photo.Saturation.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: Política de metadados de foto System.Photo.S saturação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be1c5be7a0663d5f57823dcb704b843f56e6076713de3682e4b12d6b533ff48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087009"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a>Política de metadados de foto System.Photo.S saturação

A política de metadados de foto para a [propriedade System.Photo.Saturation.](../properties/props-system-photo-saturation.md)

### <a name="pkey"></a>Pkey

Saturação da \_ foto \_ PKEY

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
| 1     | /app1/ifd/exif/{ushort=41993} | ushort      |
| 2     | /xmp/exif:Saturação          | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41993} | ushort      |
| 2     | /xmp/exif:Saturação          | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=41993} |
| 2     | /xmp/exif:s saturação          |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41993} | ushort      |
| 2     | /ifd/xmp/exif:S saturação | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41993} | ushort      |
| 2     | /ifd/xmp/exif:S saturação | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=41993} |
| 2     | /ifd/xmp/exif:s saturação |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Photo.S saturação](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
