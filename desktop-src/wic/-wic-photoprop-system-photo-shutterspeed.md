---
description: A política de metadados de foto para a propriedade System. Photo. ShutterSpeed.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Política de metadados de foto System. Photo. ShutterSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df8c9e7fda5643fed022f67c3b6b7846e7a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759515"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a>Política de metadados de foto System. Photo. ShutterSpeed

A política de metadados de foto para a propriedade [System. Photo. ShutterSpeed](../properties/props-system-photo-shutterspeed.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ ShutterSpeed

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

R8 de VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor é gerado em System. Photo. ShutterSpeedNumerator e System. Photo. ShutterSpeedDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37377} |             |
| 2     | /xmp/exif:ShutterSpeedValue   |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37377} |             |
| 2     | /xmp/exif:ShutterSpeedValue   |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37377} |
| 2     | /xmp/exif:shutterspeedvalue   |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37377}        |             |
| 2     | /ifd/xmp/exif:ShutterSpeedValue |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37377}        |             |
| 2     | /ifd/xmp/exif:ShutterSpeedValue |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                            |
|-------|---------------------------------|
| 1     | /IFD/EXIF/{UShort = 37377}        |
| 2     | /ifd/xmp/exif:shutterspeedvalue |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. ShutterSpeed](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
