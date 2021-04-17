---
description: A política de metadados de foto para a propriedade System. GPS. AltitudeRef.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: Política de metadados de foto System. GPS. AltitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db600d218d72014c49fd3f0a8b5eb11dd4c467d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790383"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a>Política de metadados de foto System. GPS. AltitudeRef

A política de metadados de foto para a propriedade [System. GPS. AltitudeRef](../properties/props-system-gps-altituderef.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ AltitudeRef

### <a name="description"></a>Descrição

Indica a altitude usada como a altitude de referência. Um valor de 0 indica que a altitude está acima do nível do mar. Um valor de 1 indica uma altitude abaixo do nível do Sea.

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_UI1 VT

### <a name="input-type"></a>Tipo de entrada

Minuciosa.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 5} |
| 2     | /xmp/exif:gpsaltituderef |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                         |
|-------|------------------------------|
| 1     | /IFD/GPS/{UShort = 5}          |
| 2     | /ifd/xmp/exif:gpsaltituderef |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. AltitudeRef](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
