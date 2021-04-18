---
description: A política de metadados de foto para a propriedade System. GPS. altitude.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: Política de metadados de foto System. GPS. altitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003d39d135c625a01035c023b5d7dc8d890b3b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791278"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a>Política de metadados de foto System. GPS. altitude

A política de metadados de foto para a propriedade [System. GPS. altitude](../properties/props-system-gps-altitude.md) .

### <a name="pkey"></a>PKEY

\_Altitude de GPS PKEY \_

### <a name="description"></a>Descrição

A altitude é indicada como um valor absoluto referenciado em metros.

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

R8 de VT \_

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

R8 de VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor pode ser gravado escrevendo em System. GPS. altitude. Numerator e System. GPS. altitude. denominador. Ele não pode ser gravado diretamente. Os caminhos de gravação nas tabelas a seguir indicam onde o valor pode ser salvo quando é gerado, não quando ele é gravado diretamente. Quando o valor é lido, os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 6} |
| 2     | /xmp/exif:gpsaltitude    |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |     |
|-------|---------------------------|-----|
| 1     | /IFD/GPS/{UShort = 6}       |     |
| 2     | /ifd/xmp/exif:gpsaltitude |     |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. altitude](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
