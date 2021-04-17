---
description: A política de metadados de foto para a propriedade System. GPS. DestDistanceRef.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: Política de metadados de foto System. GPS. DestDistanceRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105794448"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a>Política de metadados de foto System. GPS. DestDistanceRef

A política de metadados de foto para a propriedade [System. GPS. DestDistanceRef](../properties/props-system-gps-destdistanceref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ DestDistanceRef

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-type"></a>Tipo de entrada

VT \_ LPWSTR ou VT \_ LPSTR são aceitos.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                         |
|-------|------------------------------|
| 1     | /App1/IFD/GPS/{UShort = 25}    |
| 2     | /xmp/exif:gpsdestdistanceref |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{UShort = 25}             |
| 2     | /ifd/xmp/exif:gpsdestdistanceref |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. DestDistanceRef](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
