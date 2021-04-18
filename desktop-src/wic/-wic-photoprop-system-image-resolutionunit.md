---
description: A política de metadados de foto para a propriedade System. Image. ResolutionUnit.
ms.assetid: b8b744bd-976b-4648-a04b-33607467d6ac
title: Política de metadados de foto System. Image. ResolutionUnit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d954df0b7efe9501cf25c33a54cd4296fb03f3c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814026"
---
# <a name="systemimageresolutionunit-photo-metadata-policy"></a>Política de metadados de foto System. Image. ResolutionUnit

A política de metadados de foto para a propriedade [System. Image. ResolutionUnit](../properties/props-system-image-resolutionunit.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Image \_ ResolutionUnit

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Sim.

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_I2 VT

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{UShort = 296}   | ushort      |
| 2     | /xmp/tiff:ResolutionUnit | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{UShort = 296}   | ushort      |
| 2     | /xmp/tiff:ResolutionUnit | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /App1/IFD/{UShort = 296}   |
| 2     | /xmp/tiff:resolutionunit |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /IFD/{UShort = 296}            | ushort      |
| 2     | /ifd/xmp/tiff:ResolutionUnit | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /IFD/{UShort = 296}            | ushort      |
| 2     | /ifd/xmp/tiff:ResolutionUnit | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                         |
|-------|------------------------------|
| 1     | /IFD/{UShort = 296}            |
| 2     | /ifd/xmp/tiff:resolutionunit |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Image. ResolutionUnit](../properties/props-system-image-resolutionunit.md)
</dt> </dl>

 

 
