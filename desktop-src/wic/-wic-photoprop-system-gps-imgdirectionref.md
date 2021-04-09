---
description: A política de metadados de foto para a propriedade System. GPS. ImgDirectionRef.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Política de metadados de foto System. GPS. ImgDirectionRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80276ca8d1981935004dbec49fef588fcde330ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171519"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a>Política de metadados de foto System. GPS. ImgDirectionRef

A política de metadados de foto para a propriedade [System. GPS. ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS. ImgDirectionRef

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-type"></a>Tipo de entrada

VT \_ LPWSTR é preferível, mas VT \_ LPSTR também é aceito.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                         |
|-------|------------------------------|
| 1     | /App1/IFD/GPS/{UShort = 16}    |
| 2     | /xmp/exif:gpsimgdirectionref |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{UShort = 16}             |
| 2     | /ifd/xmp/exif:gpsimgdirectionref |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
