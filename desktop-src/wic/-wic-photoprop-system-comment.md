---
description: A política de metadados de foto para a propriedade System. Comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Política de metadados de foto System. Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b3511e0a459a2b652b29828060be6f0a92a36639aef63d4fa087e54ec9d80b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205625"
---
# <a name="systemcomment-photo-metadata-policy"></a>Política de metadados de foto System. Comment

A política de metadados de foto para a propriedade [System. Comment](../properties/props-system-comment.md) .

### <a name="pkey"></a>PKEY

Comentário de PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

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

 

 
