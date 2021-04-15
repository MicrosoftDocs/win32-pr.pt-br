---
description: A política de metadados de foto para a propriedade System. Image. Imageid.
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: Política de metadados de foto System. Image. Imageid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab812a8719c905002c91d33a65cc2b570d37cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505933"
---
# <a name="systemimageimageid-photo-metadata-policy"></a>Política de metadados de foto System. Image. Imageid

A política de metadados de foto para a propriedade [System. Image. imageid](../properties/props-system-image-imageid.md) .

### <a name="pkey"></a>PKEY

\_Imageid de imagem PKEY \_

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



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 42016} | ascii       |
| 2     | /XMP/EXIF: ImageUniqueID       | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 42016} | ascii       |
| 2     | /XMP/EXIF: ImageUniqueID       | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 42016} |
| 2     | /XMP/EXIF: ImageUniqueID       |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                        | Formato de disco |
|-------|-----------------------------|-------------|
|       | /IFD/EXIF/{UShort = 42016}    | ascii       |
|       | /IFD/XMP/EXIF: ImageUniqueID | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                        | Formato de disco |
|-------|-----------------------------|-------------|
|       | /IFD/EXIF/{UShort = 42016}    | ascii       |
|       | /IFD/XMP/EXIF: ImageUniqueID | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                        |
|-------|-----------------------------|
|       | /IFD/EXIF/{UShort = 42016}    |
|       | /IFD/XMP/EXIF: ImageUniqueID |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Image. Imageid](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
