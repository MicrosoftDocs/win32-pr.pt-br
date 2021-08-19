---
description: A política de metadados de foto para a propriedade System. GPS. satélites.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: Política de metadados de foto System. GPS. satélites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65bdc244324df513b5029c682e9c2cb355da58f2c95d13910fe093ce2521c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964835"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a>Política de metadados de foto System. GPS. satélites

A política de metadados de foto para a propriedade [System. GPS. satélites](../properties/props-system-gps-satellites.md) .

### <a name="pkey"></a>PKEY

\_Satélites de GPS PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-type"></a>Tipo de entrada

Cadeia de caracteres.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 8} |
| 2     | /xmp/exif:gpssatellites  |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                        |
|-------|-----------------------------|
| 1     | /IFD/GPS/{UShort = 8}         |
| 2     | /ifd/xmp/exif:gpssatellites |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. satélites](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
