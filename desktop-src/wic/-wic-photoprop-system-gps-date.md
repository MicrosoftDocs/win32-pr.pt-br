---
description: A política de metadados de foto para a propriedade System. GPS. Date.
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: Política de metadados de foto System. GPS. Date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c736c79cd76d2d070d727dc024925717b386cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171521"
---
# <a name="systemgpsdate-photo-metadata-policy"></a>Política de metadados de foto System. GPS. Date

A política de metadados de foto para a propriedade [System. GPS. Date](../properties/props-system-gps-date.md) .

### <a name="pkey"></a>PKEY

PKEY \_ data de GPS \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="input-type"></a>Tipo de entrada

Cadeia de caracteres.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 29} | ascii       |
| 2     | /xmp/exif:GPSTimeStamp    | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 29} | ascii       |
| 2     | /xmp/exif:GPSTimeStamp    | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 29} |
| 2     | /xmp/exif:GPSTimeStamp    |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 29}       | ascii       |
| 2     | /ifd/xmp/exif:GPSTimeStamp | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 29}       | ascii       |
| 2     | /ifd/xmp/exif:GPSTimeStamp | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{UShort = 29}       |
| 2     | /ifd/xmp/exif:GPSTimeStamp |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. Date](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
