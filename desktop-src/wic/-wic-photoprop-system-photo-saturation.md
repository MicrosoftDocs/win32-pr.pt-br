---
description: A política de metadados de foto para a propriedade System. Photo. saturação.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: Política de metadados de foto System. Photo. saturação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2b199458f063f2c28d7f6780a6ea907f76f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011536"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a>Política de metadados de foto System. Photo. saturação

A política de metadados de foto para a propriedade [System. Photo. saturação](../properties/props-system-photo-saturation.md) .

### <a name="pkey"></a>PKEY

\_Saturação de fotos PKEY \_

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
| 1     | /App1/IFD/EXIF/{UShort = 41993} | ushort      |
| 2     | /XMP/EXIF: saturação          | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41993} | ushort      |
| 2     | /XMP/EXIF: saturação          | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41993} |
| 2     | /XMP/EXIF: saturação          |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41993} | ushort      |
| 2     | /IFD/XMP/EXIF: saturação | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41993} | ushort      |
| 2     | /IFD/XMP/EXIF: saturação | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{UShort = 41993} |
| 2     | /IFD/XMP/EXIF: saturação |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. saturação](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
