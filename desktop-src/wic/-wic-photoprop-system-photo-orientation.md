---
description: A política de metadados de foto para a propriedade System. Photo. Orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Política de metadados de foto System. Photo. Orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f4f350cd1a4c24d71ec737b4679aea2f7cab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011537"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a>Política de metadados de foto System. Photo. Orientation

A política de metadados de foto para a propriedade [System. Photo. Orientation](../properties/props-system-photo-meteringmode.md) .

### <a name="pkey"></a>PKEY

PKEY \_ a \_ orientação da foto

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

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
| 1     | /App1/IFD/{UShort = 274} | ushort      |
| 2     | /XMP/TIFF: orientação  | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 274} | ushort      |
| 2     | /XMP/TIFF: orientação  | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                   |
|-------|------------------------|
| 1     | /App1/IFD/{UShort = 274} |
| 2     | /XMP/TIFF: orientação  |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/{UShort = 274}         | ushort      |
| 2     | /IFD/XMP/TIFF: orientação | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/{UShort = 274}         | ushort      |
| 2     | /IFD/XMP/TIFF: orientação | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /IFD/{UShort = 274}         |
| 2     | /IFD/XMP/TIFF: orientação |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. Orientation](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
