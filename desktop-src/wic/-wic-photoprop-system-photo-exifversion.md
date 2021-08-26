---
description: A política de metadados de foto para a propriedade System. Photo. EXIFVersion.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: Política de metadados de foto System. Photo. EXIFVersion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eee0fdac7ba8e86321d4a055cb6c37c4e9c7bad3f5bcfced548cc2485b3347c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882026"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a>Política de metadados de foto System. Photo. EXIFVersion

A política de metadados de foto para a propriedade [System. Photo. EXIFVersion](../properties/props-system-photo-exifversion.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ EXIFVersion

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



| Ordem | Caminho                          | Formato de disco   |
|-------|-------------------------------|---------------|
| 1     | /App1/IFD/EXIF/{UShort = 36864} | versão do EXIF \_ |
| 2     | /xmp/exif:ExifVersion         | Unicode       |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco   |
|-------|-------------------------------|---------------|
| 1     | /App1/IFD/EXIF/{UShort = 36864} | versão do EXIF \_ |
| 2     | /xmp/exif:ExifVersion         | Unicode       |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 36864} |
| 2     | /xmp/exif:ExifVersion         |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco   |
|-------|---------------------------|---------------|
| 1     | /IFD/EXIF/{UShort = 36864}  | versão do EXIF \_ |
| 2     | /ifd/xmp/exif:ExifVersion | Unicode       |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco   |
|-------|---------------------------|---------------|
| 1     | /IFD/EXIF/{UShort = 36864}  | versão do EXIF \_ |
| 2     | /ifd/xmp/exif:ExifVersion | Unicode       |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{UShort = 36864}  |
| 2     | /ifd/xmp/exif:ExifVersion |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. EXIFVersion](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
