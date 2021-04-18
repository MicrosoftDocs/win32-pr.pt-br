---
description: A política de metadados de foto para a propriedade System. Photo. nitidez.
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: Política de metadados de foto System. Photo. nitidez
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d635691f0b0e0801c1e37a006faa686aff0a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766288"
---
# <a name="systemphotosharpness-photo-metadata-policy"></a>Política de metadados de foto System. Photo. nitidez

A política de metadados de foto para a propriedade [System. Photo. nitidez](../properties/props-system-photo-sharpness.md) .

### <a name="pkey"></a>PKEY

\_Nitidez da foto PKEY \_

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



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41994} | ushort      |
| 2     | /XMP/EXIF: nitidez           | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41994} | ushort      |
| 2     | /XMP/EXIF: nitidez           | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41994} |
| 2     | /XMP/EXIF: nitidez           |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41994} | ushort      |
| 2     | /IFD/XMP/EXIF: nitidez  | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41994} | ushort      |
| 2     | /IFD/XMP/EXIF: nitidez  | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{UShort = 41994} |
| 2     | /IFD/XMP/EXIF: nitidez  |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. nitidez](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
