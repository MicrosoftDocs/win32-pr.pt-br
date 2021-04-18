---
description: A política de metadados de foto para a propriedade System. Title.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: Política de metadados de foto System. title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02513f3f566576999e83b09c156d36ac480c17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786154"
---
# <a name="systemtitle-photo-metadata-policy"></a>Política de metadados de foto System. title

A política de metadados de foto para a propriedade [System. title](../properties/props-system-title.md) .

### <a name="pkey"></a>PKEY

Título do PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

Um VT \_ LPWSTR ou VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                | Formato de disco    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40091}            | \_bytes Unicode |
| 2     | /XMP/ <xmpalt> DC: title         | Unicode        |
| 3     | /XMP/DC: título                       | Unicode        |
| 4     | /App1/IFD/EXIF/{UShort = 37510}       | Unicode        |
| 5     | /App1/IFD/{UShort = 270}              | ascii          |
| 6     | /app13/irb/8bimiptc/iptc/caption    |                |
| 7     | /XMP/ <xmpalt> DC: Descrição   | Unicode        |
| 8     | /XMP/DC: Descrição                 | Unicode        |
| 9     | /app13/irb/8bimiptc/iptc/caption    |                |
| 10    | /XMP/ <xmpalt> EXIF: UserComment | Unicode        |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                                | Formato de disco    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40091}            | \_bytes Unicode |
| 2     | /XMP/DC: título                       | Unicode        |
| 3     | /XMP/ <xmpalt> DC: title         | Unicode        |
| 4     | /App1/IFD/EXIF/{UShort = 37510}       | Unicode        |
| 5     | /XMP/ <xmpalt> EXIF: UserComment | Unicode        |
| 6     | /App1/IFD/{UShort = 270}              | ascii          |
| 7     | /app13/irb/8bimiptc/iptc/caption    |                |
| 8     | /XMP/DC: Descrição                 | Unicode        |
| 9     | /XMP/ <xmpalt> DC: Descrição   | Unicode        |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                |
|-------|-------------------------------------|
| 1     | /App1/IFD/{UShort = 40091}            |
| 2     | /XMP/DC: título                       |
| 3     | /App1/IFD/EXIF/{UShort = 37510}       |
| 4     | /XMP/ <xmpalt> EXIF: UserComment |
| 5     | /App1/IFD/{UShort = 270}              |
| 6     | /app13/irb/8bimiptc/iptc/caption    |
| 7     | /XMP/DC: Descrição                 |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                    | Formato de disco    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{UShort = 40091}                     | \_bytes Unicode |
| 2     | /IFD/XMP/ <xmpalt> DC: title         | Unicode        |
| 3     | /IFD/XMP/DC: título                       | Unicode        |
| 4     | /IFD/EXIF/{UShort = 37510}                | Unicode        |
| 5     | /IFD/{UShort = 270}                       | ascii          |
| 6     | /ifd/iptc/caption                       |                |
| 7     | /IFD/XMP/ <xmpalt> DC: Descrição   | Unicode        |
| 8     | /IFD/XMP/DC: Descrição                 | Unicode        |
| 9     | /ifd/iptc/caption                       |                |
| 10    | /ifd/irb/8bimiptc/iptc/caption          |                |
| 11    | /IFD/XMP/ <xmpalt> EXIF: UserComment | Unicode        |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                                    | Formato de disco    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{UShort = 40091}                     | \_bytes Unicode |
| 2     | /IFD/XMP/DC: título                       | Unicode        |
| 3     | /IFD/XMP/ <xmpalt> DC: title         | Unicode        |
| 4     | /IFD/EXIF/{UShort = 37510}                | Unicode        |
| 5     | /IFD/XMP/ <xmpalt> EXIF: UserComment | Unicode        |
| 6     | /IFD/{UShort = 270}                       | ascii          |
| 7     | /ifd/iptc/caption                       |                |
| 8     | /ifd/irb/8bimiptc/iptc/caption          |                |
| 9     | /IFD/XMP/DC: Descrição                 | Unicode        |
| 10    | /IFD/XMP/ <xmpalt> DC: Descrição   | Unicode        |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                    |
|-------|-----------------------------------------|
| 1     | /IFD/{UShort = 40091}                     |
| 2     | /IFD/XMP/DC: título                       |
| 3     | /IFD/EXIF/{UShort = 37510}                |
| 4     | /IFD/XMP/ <xmpalt> EXIF: UserComment |
| 5     | /IFD/{UShort = 270}                       |
| 6     | /ifd/iptc/caption                       |
| 7     | /ifd/irb/8bimiptc/iptc/caption          |
| 8     | /IFD/XMP/DC: Descrição                 |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Title](../properties/props-system-title.md)
</dt> </dl>

 

 
