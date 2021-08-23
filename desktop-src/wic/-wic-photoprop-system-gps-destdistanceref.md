---
description: A política de metadados de foto para a propriedade System.GPS.DestDistanceRef.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: Política de metadados de foto System.GPS.DestDistanceRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d7973a3be36f9a7624ed8679f364c898d69b622de067bdd2595f3b919a964f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964975"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a>Política de metadados de foto System.GPS.DestDistanceRef

A política de metadados de foto [para a propriedade System.GPS.DestDistanceRef.](../properties/props-system-gps-destdistanceref.md)

### <a name="pkey"></a>Pkey

PKEY \_ DestDistanceRef

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

VT \_ LPWSTR ou VT \_ LPSTR são aceitos.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                         |
|-------|------------------------------|
| 1     | /app1/ifd/gps/{ushort=25}    |
| 2     | /xmp/exif:gpsdestdistanceref |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                             |
|-------|----------------------------------|
| 1     | /ifd/gps/{ushort=25}             |
| 2     | /ifd/xmp/exif:gpsdestdistanceref |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.DestDistanceRef](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
