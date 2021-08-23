---
description: A política de metadados de foto para a propriedade System. Photo. RelatedSoundFile.
ms.assetid: 3b212d90-7ae2-4b7c-b77a-2017490aca40
title: Política de metadados de foto System. Photo. RelatedSoundFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aae80ad39b8d3dab271aacf4815836e8b386c150ec80be63a83a4ab5937635e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549426"
---
# <a name="systemphotorelatedsoundfile-photo-metadata-policy"></a>Política de metadados de foto System. Photo. RelatedSoundFile

A política de metadados de foto para a propriedade [System. Photo. RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ RelatedSoundFile

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

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
| 1     | /App1/IFD/EXIF/{UShort = 40964} | ascii       |
| 2     | /xmp/exif:RelatedSoundFile    | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 40964} | ascii       |
| 2     | /xmp/exif:RelatedSoundFile    | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 40964} |
| 2     | /xmp/exif:RelatedSoundFile    |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 40964}       | ascii       |
| 2     | /ifd/xmp/exif:RelatedSoundFile | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 40964}       | ascii       |
| 2     | /ifd/xmp/exif:RelatedSoundFile | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                           |
|-------|--------------------------------|
| 1     | /IFD/EXIF/{UShort = 40964}       |
| 2     | /ifd/xmp/exif:RelatedSoundFile |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md)
</dt> </dl>

 

 
