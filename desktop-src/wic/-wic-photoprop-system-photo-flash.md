---
description: A política de metadados de foto para a propriedade System. Photo. flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Política de metadados de foto System. Photo. flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0302e0f310d2f9a6a4390b0d4856578cc2f43e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787011"
---
# <a name="systemphotoflash-photo-metadata-policy"></a>Política de metadados de foto System. Photo. flash

A política de metadados de foto para a propriedade [System. Photo. flash](../properties/props-system-photo-exposuretime.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ flash

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

VT \_ UI1 (se o esquema de origem era XMP) ou VT \_ UI2 (se o esquema de origem era EXIF)

\\lang1036

### <a name="input-type"></a>Tipo de entrada

VT \_ UI1, VTUI2, VT \_ UI4

\\lang1033

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37385}    | ushort      |
| 2     | /XMP/ <xmpstruct> EXIF: flash |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37385}    | ushort      |
| 2     | /XMP/ <xmpstruct> EXIF: flash |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                             |
|-------|----------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37385}    |
| 2     | /XMP/ <xmpstruct> EXIF: flash |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                 | Formato de disco |
|-------|--------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37385}             | ushort      |
| 2     | /IFD/XMP/ <xmpstruct> EXIF: flash |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                                 | Formato de disco |
|-------|--------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37385}             | ushort      |
| 2     | /IFD/XMP/ <xmpstruct> EXIF: flash |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                 |
|-------|--------------------------------------|
| 1     | /IFD/EXIF/{UShort = 37385}             |
| 2     | /IFD/XMP/ <xmpstruct> EXIF: flash |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
