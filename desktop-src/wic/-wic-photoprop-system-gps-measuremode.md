---
description: A política de metadados de foto para a propriedade System. GPS. Measuremode.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: Política de metadados de foto System. GPS. Measuremode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9449ca9a7d1ee5ef213c37562392be2842a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921864"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a>Política de metadados de foto System. GPS. Measuremode

A política de metadados de foto para a propriedade [System. GPS. measuremode](../properties/props-system-gps-measuremode.md) .

### <a name="pkey"></a>PKEY

PKEY \_ de \_ medida de GPS

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

VT \_ LPWSTR é preferível, mas VT \_ LPSTR também é aceito.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 10} | ascii       |
| 2     | /xmp/exif:GPSMeasureMode  | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 10} | ascii       |
| 2     | /xmp/exif:GPSMeasureMode  | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 10} |
| 2     | /xmp/exif:gpsmeasuremode  |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 10}         | ascii       |
| 2     | /ifd/xmp/exif:GPSMeasureMode | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 10}         | ascii       |
| 2     | /ifd/xmp/exif:GPSMeasureMode | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                         |
|-------|------------------------------|
| 1     | /IFD/GPS/{UShort = 10}         |
| 2     | /ifd/xmp/exif:gpsmeasuremode |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. Measuremode](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
