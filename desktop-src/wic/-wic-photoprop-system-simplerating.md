---
description: A política de metadados de foto para a propriedade System. SimpleRating.
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: Política de metadados de foto System. SimpleRating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b91e41a0684c8e395992683e0a1d4fe43306a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011532"
---
# <a name="systemsimplerating-photo-metadata-policy"></a>Política de metadados de foto System. SimpleRating

A política de metadados de foto para a propriedade [System. SimpleRating](../properties/props-system-simplerating.md) .

### <a name="pkey"></a>PKEY

PKEY \_ SimpleRating

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_UI4 VT

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

Pode ser VT \_ UI1, VT \_ UI2 ou VT \_ UI4. O valor inteiro pode variar de 0 a 5.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{UShort = 18246} | ushort      |
| 2     | /XMP/XMP: classificação          | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{UShort = 18246} | ushort      |
| 2     | /XMP/XMP: classificação          | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /App1/IFD/{UShort = 18246} |
| 2     | /XMP/XMP: classificação          |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                | Formato de disco |
|-------|---------------------|-------------|
| 1     | /IFD/{UShort = 18246} | ushort      |
| 2     | /IFD/XMP/XMP: classificação | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                | Formato de disco |
|-------|---------------------|-------------|
| 1     | /IFD/{UShort = 18246} | ushort      |
| 2     | /IFD/XMP/XMP: classificação | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                |
|-------|---------------------|
| 1     | /IFD/{UShort = 18246} |
| 2     | /IFD/XMP/XMP: classificação |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. SimpleRating](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
