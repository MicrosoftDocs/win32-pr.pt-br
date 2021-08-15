---
description: A política de metadados de foto para a propriedade System.Photo.CameraManufacturer.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: System.Photo.CameraManufacturer Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37744420babedf6b398cdf3ab9007c3895c09d33b9254221b5ba4760ab917a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087082"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a>System.Photo.CameraManufacturer Photo Metadata Policy

A política de metadados de foto para a [propriedade System.Photo.CameraManufacturer.](../properties/props-system-photo-cameramanufacturer.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ CameraManufacturer

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

Cadeia de caracteres.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=271} | ascii       |
| 2     | /xmp/tiff:Make         | Unicode     |
| 3     | /xmp/tiff:make         | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=271} | ascii       |
| 2     | /xmp/tiff:Make         | Unicode     |
| 3     | /xmp/tiff:make         | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort=271} |
| 2     | /xmp/tiff:Make         |
| 3     | /xmp/tiff:make         |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho               | Formato de disco |
|-------|--------------------|-------------|
| 1     | /ifd/{ushort=271}  | ascii       |
| 2     | /ifd/xmp/tiff:Make | Unicode     |
| 3     | /ifd/xmp/tiff:make | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho               | Formato de disco |
|-------|--------------------|-------------|
| 1     | /ifd/{ushort=271}  | ascii       |
| 2     | /ifd/xmp/tiff:Make | Unicode     |
| 3     | /ifd/xmp/tiff:make | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho               |
|-------|--------------------|
| 1     | /ifd/{ushort=271}  |
| 2     | /ifd/xmp/tiff:Make |
| 3     | /ifd/xmp/tiff:make |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Photo.CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
