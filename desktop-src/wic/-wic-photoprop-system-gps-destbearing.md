---
description: A política de metadados de foto para a propriedade System. GPS. DestBearing.
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: Política de metadados de foto System. GPS. DestBearing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a084a0633579afe646403fb4dcad0ca8a1b9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297366"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a>Política de metadados de foto System. GPS. DestBearing

A política de metadados de foto para a propriedade [System. GPS. DestBearing](../properties/props-system-gps-destbearing.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestBearing

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

R8 de VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor pode ser gravado escrevendo em System. GPS. DestBearingNumerator e System. GPS. DestBearingDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 24} |             |
| 2     | /xmp/exif:GPSDestBearing  |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 24} |             |
| 2     | /xmp/exif:GPSDestBearing  |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 24} |             |
| 2     | /xmp/exif:gpsdestbearing  |             |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 24}         |             |
| 2     | /ifd/xmp/exif:GPSDestBearing |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 24}         |             |
| 2     | /ifd/xmp/exif:GPSDestBearing |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                         |
|-------|------------------------------|
| 1     | /IFD/GPS/{UShort = 24}         |
| 2     | /ifd/xmp/exif:gpsdestbearing |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. DestBearing](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
