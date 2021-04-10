---
description: A política de metadados de foto para a propriedade System. GPS. TrackRef.
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: Política de metadados de foto System. GPS. TrackRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95fc63de6eaffd697798c08ff74a46c3d15c7818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172057"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a>Política de metadados de foto System. GPS. TrackRef

A política de metadados de foto para a propriedade [System. GPS. TrackRef](../properties/props-system-gps-trackref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ TrackRef

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-type"></a>Tipo de entrada

String

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 14} | ascii       |
| 2     | /xmp/exif:GPSTrackRef     | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 14} | ascii       |
| 2     | /xmp/exif:GPSTrackRef     | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 14} |
| 2     | /xmp/exif:gpstrackref     |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 14}      | ascii       |
| 2     | /ifd/xmp/exif:GPSTrackRef | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 14}      | ascii       |
| 2     | /ifd/xmp/exif:GPSTrackRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /IFD/GPS/{UShort = 14}      |
| 2     | /ifd/xmp/exif:gpstrackref |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. TrackRef](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
