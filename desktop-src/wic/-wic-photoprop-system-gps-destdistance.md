---
description: A política de metadados de foto para a propriedade System. GPS. DestDistance.
ms.assetid: 1bd72acb-f462-454d-aec2-72d5b4517de3
title: Política de metadados de foto System. GPS. DestDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc71c89ae6270f5babf08637f54baaf2cb57aae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760415"
---
# <a name="systemgpsdestdistance-photo-metadata-policy"></a>Política de metadados de foto System. GPS. DestDistance

A política de metadados de foto para a propriedade [System. GPS. DestDistance](../properties/props-system-gps-destdistance.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestDistance

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

R8 de VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor é gerado de System. GPS. DestDistanceNumerator e System. GPS. DestDistanceDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 26} |             |
| 2     | /xmp/exif:GPSDestDistance |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 26} |             |
| 2     | /xmp/exif:GPSDestDistance |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 26} |
| 2     | /xmp/exif:gpsdestdistance |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 26}          |             |
| 2     | /ifd/xmp/exif:GPSDestDistance |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 26}          |             |
| 2     | /ifd/xmp/exif:GPSDestDistance |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /IFD/GPS/{UShort = 26}          |
| 2     | /ifd/xmp/exif:gpsdestdistance |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. DestDistance](../properties/props-system-gps-destdistance.md)
</dt> </dl>

 

 
