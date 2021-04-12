---
description: A política de metadados de foto para a propriedade System. Comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Política de metadados de foto System. Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9d7526e05a72b073ac32bd8286a621b33ee62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297368"
---
# <a name="systemcomment-photo-metadata-policy"></a>Política de metadados de foto System. Comment

A política de metadados de foto para a propriedade [System. Comment](../properties/props-system-comment.md) .

### <a name="pkey"></a>PKEY

Comentário de PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

VT \_ LPWSTR ou VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                | Formato de disco    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40092}            | \_bytes Unicode |
| 2     | /App1/IFD/{UShort = 37510}            | Unicode        |
| 3     | /XMP/ <xmpalt> EXIF: UserComment | Unicode        |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco    |
|-------|--------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40092} | \_bytes Unicode |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/{UShort = 40092}      |
| 2     | /App1/IFD/EXIF/{UShort = 37510} |
| 3     | /XMP/EXIF: UserComment         |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                    | Formato de disco    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{UShort = 40092}                     | \_bytes Unicode |
| 2     | /IFD/{UShort = 37510}                     | Unicode        |
| 3     | /IFD/XMP/ <xmpalt> EXIF: UserComment | Unicode        |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                | Formato de disco    |
|-------|---------------------|----------------|
| 1     | /IFD/{UShort = 40092} | \_bytes Unicode |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /IFD/{UShort = 40092}       |
| 2     | /IFD/{UShort = 37510}       |
| 3     | /IFD/XMP/EXIF: UserComment |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema. Comment](../properties/props-system-comment.md)
</dt> </dl>

 

 
