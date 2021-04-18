---
description: A política de metadados de foto para a propriedade System. GPS. ProcessingMethod.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: Política de metadados de foto System. GPS. ProcessingMethod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bf1484eb8e8a53c65a9cd43c54b076e418d4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810189"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a>Política de metadados de foto System. GPS. ProcessingMethod

A política de metadados de foto para a propriedade [System. GPS. ProcessingMethod](../properties/props-system-gps-processingmethod.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ ProcessingMethod

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



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/GPS/{UShort = 27}     |
| 2     | /xmp/exif:gpsprocessingmethod |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                              | Formato de disco |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | Unicode     |
| 2     | /IFD/GPS/{UShort = 27}              |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                              | Formato de disco |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | Unicode     |
| 2     | /IFD/GPS/{UShort = 27}              |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                              |
|-------|-----------------------------------|
| 1     | /ifd/xmp/exif:gpsprocessingmethod |
| 2     | /IFD/GPS/{UShort = 27}              |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. ProcessingMethod](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
