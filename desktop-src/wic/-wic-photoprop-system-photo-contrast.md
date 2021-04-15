---
description: A política de metadados de foto para a propriedade System. Photo. Contrast.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: Política de metadados de foto System. Photo. Contrast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d6ed34854b525e9eaac2ff5ac7339a75ad10e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506264"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a>Política de metadados de foto System. Photo. Contrast

A política de metadados de foto para a propriedade [System. Photo. Contrast](../properties/props-system-photo-contrast.md) .

### <a name="pkey"></a>PKEY

\_Contraste de fotos PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_UI4 VT

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41992} | ushort      |
| 2     | /XMP/EXIF: contraste            | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41992} | ushort      |
| 2     | /XMP/EXIF: contraste            | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41992} |
| 2     | /XMP/EXIF: contraste            |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41992} | ushort      |
| 2     | /IFD/XMP/EXIF: contraste   | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41992} | ushort      |
| 2     | /IFD/XMP/EXIF: contraste   | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{UShort = 41992} |
| 2     | /IFD/XMP/EXIF: contraste   |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. Contrast](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
