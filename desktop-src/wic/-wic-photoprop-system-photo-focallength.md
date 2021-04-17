---
description: A política de metadados de foto para a propriedade System. Photo. FocalLength.
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: Política de metadados de foto System. Photo. FocalLength
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7b36240713782c98d52e4fbf4dae5c0c06082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812212"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a>Política de metadados de foto System. Photo. FocalLength

A política de metadados de foto para a propriedade [System. Photo. FocalLength](../properties/props-system-photo-focallength.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FocalLength

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

R8 de VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor é gerado em System. Photo. FocalLengthNumerator e System. Photo. FocalLengthDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37386} |             |
| 2     | /xmp/exif:FocalLength         |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37386} |             |
| 2     | /xmp/exif:FocalLength         |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37386} |
| 2     | /xmp/exif:focallength         |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37386}  |             |
| 2     | /ifd/xmp/exif:FocalLength |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37386}  |             |
| 2     | /ifd/xmp/exif:FocalLength |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{UShort = 37386}  |
| 2     | /ifd/xmp/exif:focallength |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. FocalLength](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
