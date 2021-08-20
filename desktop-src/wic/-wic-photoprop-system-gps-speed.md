---
description: A política de metadados de foto para a propriedade System.GPS.Speed.
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: Política de metadados de foto System.GPS.Speed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a33150741b9194d3925184e0e736735e2321f3ce4e0388f0be8cb2d97604e84c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667883"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a>Política de metadados de foto System.GPS.Speed

A política de metadados de foto para a [propriedade System.GPS.Speed.](../properties/props-system-gps-speed.md)

### <a name="pkey"></a>Pkey

Velocidade do \_ GPS PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Sim

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ R8

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Esse valor é gerado de System.GPS.SpeedNumerator e System.GPS.SpeedDenominator. Ele não pode ser gravado diretamente. Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=13} |             |
| 2     | /xmp/exif:GPSSpeed        |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=13} |             |
| 2     | /xmp/exif:GPSSpeed        |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=13} |
| 2     | /xmp/exif:gpsspeed        |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /ifd/gps/{ushort=13}   |             |
| 2     | /ifd/xmp/exif:GPSSpeed |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /ifd/gps/{ushort=13}   |             |
| 2     | /ifd/xmp/exif:GPSSpeed |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                   |
|-------|------------------------|
| 1     | /ifd/gps/{ushort=13}   |
| 2     | /ifd/xmp/exif:gpsspeed |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.Speed](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
