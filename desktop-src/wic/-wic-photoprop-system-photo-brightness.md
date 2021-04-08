---
description: A política de metadados de foto para a propriedade System. Photo. pobrilho.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: Política de metadados de foto System. Photo. Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7328b4d40b8d1582dcc17b317b706b2695c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922561"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a>Política de metadados de foto System. Photo. Brightness

A política de metadados de foto para a propriedade [System. Photo. pobrilho](../properties/props-system-photo-aperture.md) .

### <a name="pkey"></a>PKEY

PKEY \_ brilho da foto \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="input-type"></a>Tipo de entrada

Double

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor é gerado em System. Photo. ApertureNumerator e System. Photo. ApertureDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37379} |             |
| 2     | /XMP/EXIF: Brightness     |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37379} |             |
| 2     | /XMP/EXIF: Brightness     |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37379} |
| 2     | /XMP/EXIF: Brightness     |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37379}      |             |
| 2     | /IFD/XMP/EXIF: Brightness |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37379}      |             |
| 2     | /IFD/XMP/EXIF: Brightness |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /IFD/EXIF/{UShort = 37379}      |
| 2     | /IFD/XMP/EXIF: Brightness |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. Brightness](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
