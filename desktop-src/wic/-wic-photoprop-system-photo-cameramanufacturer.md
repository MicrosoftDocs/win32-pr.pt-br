---
description: A política de metadados de foto para a propriedade System. Photo. CameraManufacturer.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: Política de metadados de foto System. Photo. CameraManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1d2765b6c787b7d7ad421300f1c3492669830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793224"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a>Política de metadados de foto System. Photo. CameraManufacturer

A política de metadados de foto para a propriedade [System. Photo. CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ CameraManufacturer

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-type"></a>Tipo de entrada

Cadeia de caracteres.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 271} | ascii       |
| 2     | /XMP/TIFF: Make         | Unicode     |
| 3     | /XMP/TIFF: Make         | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 271} | ascii       |
| 2     | /XMP/TIFF: Make         | Unicode     |
| 3     | /XMP/TIFF: Make         | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                   |
|-------|------------------------|
| 1     | /App1/IFD/{UShort = 271} |
| 2     | /XMP/TIFF: Make         |
| 3     | /XMP/TIFF: Make         |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho               | Formato de disco |
|-------|--------------------|-------------|
| 1     | /IFD/{UShort = 271}  | ascii       |
| 2     | /IFD/XMP/TIFF: Make | Unicode     |
| 3     | /IFD/XMP/TIFF: Make | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho               | Formato de disco |
|-------|--------------------|-------------|
| 1     | /IFD/{UShort = 271}  | ascii       |
| 2     | /IFD/XMP/TIFF: Make | Unicode     |
| 3     | /IFD/XMP/TIFF: Make | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho               |
|-------|--------------------|
| 1     | /IFD/{UShort = 271}  |
| 2     | /IFD/XMP/TIFF: Make |
| 3     | /IFD/XMP/TIFF: Make |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
