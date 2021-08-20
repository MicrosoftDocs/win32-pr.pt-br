---
description: A política de metadados de foto para a propriedade System.SimpleRating.
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: System.SimpleRating Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c65c9e49d7e905a4cefe890b6c5aab257250baa41171470666ba38b3fb5c96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709960"
---
# <a name="systemsimplerating-photo-metadata-policy"></a>System.SimpleRating Photo Metadata Policy

A política de metadados de foto para a [propriedade System.SimpleRating.](../properties/props-system-simplerating.md)

### <a name="pkey"></a>Pkey

PKEY \_ SimpleRating

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ UI4

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

Pode ser VT \_ UI1, VT \_ UI2 ou VT \_ UI4. O valor inteiro pode variar de 0 a 5.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/{ushort=18246} | ushort      |
| 2     | /xmp/xmp:Rating          | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/{ushort=18246} | ushort      |
| 2     | /xmp/xmp:Rating          | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /app1/ifd/{ushort=18246} |
| 2     | /xmp/xmp:rating          |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                | Formato de disco |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort=18246} | ushort      |
| 2     | /ifd/xmp/xmp:Rating | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                | Formato de disco |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort=18246} | ushort      |
| 2     | /ifd/xmp/xmp:Rating | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                |
|-------|---------------------|
| 1     | /ifd/{ushort=18246} |
| 2     | /ifd/xmp/xmp:rating |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.SimpleRating](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
