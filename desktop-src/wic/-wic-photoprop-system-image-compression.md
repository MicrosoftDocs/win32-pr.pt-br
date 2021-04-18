---
description: A política de metadados de foto para a propriedade System. Image. Compression.
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: Política de metadados de foto System. Image. Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32fdc55e2a6a962b1a3dfd9057ef25c89d942f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813091"
---
# <a name="systemimagecompression-photo-metadata-policy"></a>Política de metadados de foto System. Image. Compression

A política de metadados de foto para a propriedade [System. Image. Compression](../properties/props-system-image-compression.md) .

### <a name="pkey"></a>PKEY

\_Compactação de imagem PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_UI2 VT

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 259} | ushort      |
| 2     | /XMP/TIFF: compactação  | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 259} | ushort      |
| 2     | /XMP/TIFF: compactação  | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                   |
|-------|------------------------|
| 1     | /App1/IFD/{UShort = 259} |
| 2     | /XMP/TIFF: compactação  |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/{UShort = 259}         | ushort      |
| 2     | /IFD/XMP/TIFF: compactação | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/{UShort = 259}         | ushort      |
| 2     | /IFD/XMP/TIFF: compactação | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /IFD/{UShort = 259}         |
| 2     | /IFD/XMP/TIFF: compactação |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Image. Compression](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
