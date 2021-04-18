---
description: A política de metadados de foto para a propriedade System. Photo. WhiteBalance.
ms.assetid: 7b3a31e6-a929-41e4-b7f0-c5b3beac2519
title: Política de metadados de foto System. Photo. WhiteBalance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc333cedcd4665ace37033452ec3c7f0336f13e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764402"
---
# <a name="systemphotowhitebalance-photo-metadata-policy"></a>Política de metadados de foto System. Photo. WhiteBalance

A política de metadados de foto para a propriedade [System. Photo. whitebalance](../properties/props-system-photo-whitebalance.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ whitebalance

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
| 1     | /App1/IFD/EXIF/{UShort = 41987} | ushort      |
| 2     | /xmp/exif:WhiteBalance        | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41987} | ushort      |
| 2     | /xmp/exif:WhiteBalance        | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41987} |
| 2     | /xmp/exif:whitebalance        |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41987}   | ushort      |
| 2     | /ifd/xmp/exif:WhiteBalance | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41987}   | ushort      |
| 2     | /ifd/xmp/exif:WhiteBalance | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                       |
|-------|----------------------------|
| 1     | /IFD/EXIF/{UShort = 41987}   |
| 2     | /ifd/xmp/exif:whitebalance |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. WhiteBalance](../properties/props-system-photo-whitebalance.md)
</dt> </dl>

 

 
