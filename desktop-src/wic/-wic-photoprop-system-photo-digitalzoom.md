---
description: A política de metadados de foto para a propriedade System. Photo. DigitalZoom.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: Política de metadados de foto System. Photo. DigitalZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf440e92243eb2102ac6abaa349ea83e58d9a2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297134"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a>Política de metadados de foto System. Photo. DigitalZoom

A política de metadados de foto para a propriedade [System. Photo. DigitalZoom](../properties/props-system-photo-digitalzoom.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ DigitalZoom

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

R8 de VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor é gerado em System. Photo. DigitalZoomNumerator e System. Photo. DigitalZoomDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41988} |             |
| 2     | /xmp/exif:DigitalZoomRatio    |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41988} |             |
| 2     | /xmp/exif:DigitalZoomRatio    |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41988} |
| 2     | /xmp/exif:digitalzoomratio    |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41988}       |             |
| 2     | /ifd/xmp/exif:DigitalZoomRatio |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41988}       |             |
| 2     | /ifd/xmp/exif:DigitalZoomRatio |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                           |
|-------|--------------------------------|
| 1     | /IFD/EXIF/{UShort = 41988}       |
| 2     | /ifd/xmp/exif:digitalzoomratio |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. DigitalZoom](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
