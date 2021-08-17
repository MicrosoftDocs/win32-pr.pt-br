---
description: A política de metadados de foto para a propriedade System. Photo. MeteringMode.
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: Política de metadados de foto System. Photo. MeteringMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424b14fa6216d5c88c350512d1583b311f92ef2f487e604760b1836b296d3bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964775"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a>Política de metadados de foto System. Photo. MeteringMode

A política de metadados de foto para a propriedade [System. Photo. MeteringMode](../properties/props-system-photo-meteringmode.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ MeteringMode

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_UI2 VT

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37383} |
| 2     | /xmp/exif:meteringmode        |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                       |
|-------|----------------------------|
| 1     | /IFD/EXIF/{UShort = 37383}   |
| 2     | /ifd/xmp/exif:meteringmode |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. MeteringMode](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
