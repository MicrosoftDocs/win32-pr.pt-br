---
description: A política de metadados de foto para a propriedade System. Photo. Exposiçãotime.
ms.assetid: 26f6ff27-b326-46f8-b4be-b091acbec575
title: Política de metadados de foto System. Photo. Exposiçãotime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9078befd0cbc26272ff14ae023b1b22cb4f0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768678"
---
# <a name="systemphotoexposuretime-photo-metadata-policy"></a>Política de metadados de foto System. Photo. Exposiçãotime

A política de metadados de foto para a propriedade [System. Photo. exposiçãotime](../properties/props-system-photo-exposuretime.md) .

### <a name="pkey"></a>PKEY

PKEY \_ fotos \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

R8 de VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor é gerado em System. Photo. ExposureTimeNumerator e System. Photo. ExposureTimeDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 33434} |             |
| 2     | /XMP/EXIF: Exposiçãotime        |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 33434} |             |
| 2     | /XMP/EXIF: Exposiçãotime        |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 33434} |
| 2     | /XMP/EXIF: exposiçãotime        |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 33434}   |             |
| 2     | /IFD/XMP/EXIF: Exposiçãotime |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 33434}   |             |
| 2     | /IFD/XMP/EXIF: Exposiçãotime |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                       |
|-------|----------------------------|
| 1     | /IFD/EXIF/{UShort = 33434}   |
| 2     | /IFD/XMP/EXIF: exposiçãotime |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema. Photo. Exposiçãotime](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
