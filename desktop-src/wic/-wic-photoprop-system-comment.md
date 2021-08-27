---
description: A política de metadados de foto para a propriedade System. Comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Política de metadados de foto System. Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa1a62fd5afa131a714c365ed2fda2c307bc955
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883905"
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



| Order | Caminho                                | Formato de disco    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40092}            | \_bytes Unicode |
| 2     | /App1/IFD/{UShort = 37510}            | Unicode        |
| 3     | /XMP/ &lt; xmpalt &gt; EXIF: UserComment | Unicode        |



 

### <a name="write-paths"></a>Caminhos de gravação



| Order | Caminho                     | Formato de disco    |
|-------|--------------------------|----------------|
| 1     | /App1/IFD/{UShort = 40092} | \_bytes Unicode |



 

### <a name="remove-paths"></a>Remover caminhos



| Order | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/{UShort = 40092}      |
| 2     | /App1/IFD/EXIF/{UShort = 37510} |
| 3     | /XMP/EXIF: UserComment         |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Order | Caminho                                    | Formato de disco    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{UShort = 40092}                     | \_bytes Unicode |
| 2     | /IFD/{UShort = 37510}                     | Unicode        |
| 3     | /IFD/XMP/ &lt; xmpalt &gt; EXIF: UserComment | Unicode        |



 

### <a name="write-paths"></a>Caminhos de gravação



| Order | Caminho                | Formato de disco    |
|-------|---------------------|----------------|
| 1     | /IFD/{UShort = 40092} | \_bytes Unicode |



 

### <a name="remove-paths"></a>Remover caminhos



| Order | Caminho                      |
|-------|---------------------------|
| 1     | /IFD/{UShort = 40092}       |
| 2     | /IFD/{UShort = 37510}       |
| 3     | /IFD/XMP/EXIF: UserComment |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema. Comment](../properties/props-system-comment.md)
</dt> </dl>

 

 
