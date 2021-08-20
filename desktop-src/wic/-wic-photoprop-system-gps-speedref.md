---
description: A política de metadados de foto para a propriedade System.GPS.SpeedRef.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: Política de metadados de foto System.GPS.SpeedRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c7b60a0c8decaf5ecc30f9017a0aadc61bb9fe4814240fb7ab2e022d6a2873f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549486"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a>Política de metadados de foto System.GPS.SpeedRef

A política de metadados de foto para a [propriedade System.GPS.SpeedRef.](../properties/props-system-gps-speedref.md)

### <a name="pkey"></a>Pkey

SpeedRef \_ do GPS \_ PKEY

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

O VT \_ LPWSTR é preferencial, mas o VT \_ LPSTR também é aceito..

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=12} |             |
| 2     | /xmp/exif:gpsspeedref     |             |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                      |         |
|-------|---------------------------|---------|
| 1     | /ifd/gps/{ushort=12}      | ascii   |
| 2     | /ifd/xmp/exif:GPSSpeedRef | Unicode |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=12}      | ascii       |
| 2     | /ifd/xmp/exif:GPSSpeedRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /ifd/gps/{ushort=12}      |
| 2     | /ifd/xmp/exif:gpsspeedref |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.SpeedRef](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
