---
description: A política de metadados de foto para a propriedade System. GPS. status.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: Política de metadados de foto System. GPS. status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac08139a267052f8d6dd3dc463e2a2768309a41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761835"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a>Política de metadados de foto System. GPS. status

A política de metadados de foto para a propriedade [System. GPS. status](../properties/props-system-gps-status.md) .

### <a name="pkey"></a>PKEY

\_Status de GPS PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

VT \_ LPWSTR é preferível, mas VT \_ LPSTR também é aceito.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 9} | ascii       |
| 2     | /xmp/exif:GPSStatus      | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 9} | ascii       |
| 2     | /xmp/exif:GPSStatus      | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 9} |
| 2     | /xmp/exif:gpsstatus      |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                    | Formato de disco |
|-------|-------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 9}     | ascii       |
| 2     | /ifd/xmp/exif:GPSStatus | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                    | Formato de disco |
|-------|-------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 9}     | ascii       |
| 2     | /ifd/xmp/exif:GPSStatus | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                    |
|-------|-------------------------|
| 1     | /IFD/GPS/{UShort = 9}     |
| 2     | /ifd/xmp/exif:gpsstatus |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. status](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
