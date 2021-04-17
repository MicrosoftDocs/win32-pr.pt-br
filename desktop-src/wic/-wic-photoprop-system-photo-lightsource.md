---
description: A política de metadados de foto para a propriedade System. Photo. claridade.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: Política de metadados de foto System. Photo. Lightexception
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9b3d31f01cdd2bea8d3fabbbc730a41f1fb0da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506155"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a>Política de metadados de foto System. Photo. Lightexception

A política de metadados de foto para a propriedade [System. Photo. claridade](../properties/props-system-photo-lightsource.md) .

### <a name="pkey"></a>PKEY

\_Claridade da foto PKEY \_

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
| 1     | /App1/IFD/EXIF/{UShort = 37384} | ushort      |
| 2     | /XMP/EXIF: claridade         | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37384} | ushort      |
| 2     | /XMP/EXIF: claridade         | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37384} |
| 2     | /XMP/EXIF: claridade         |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37384}  | ushort      |
| 2     | /IFD/XMP/EXIF: claridade | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37384}  | ushort      |
| 2     | /IFD/XMP/EXIF: claridade | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{UShort = 37384}  |
| 2     | /IFD/XMP/EXIF: claridade |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema. foto. Lightname](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
