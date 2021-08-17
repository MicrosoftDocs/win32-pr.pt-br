---
description: A política de metadados de foto para a propriedade System.Photo.Orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Política de metadados de foto System.Photo.Orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f9496942e6be971e0e047596125669fc9112cf82bce6eb02ec7e1cdbddc4de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087062"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a>Política de metadados de foto System.Photo.Orientation

A política de metadados de foto para a [propriedade System.Photo.Orientation.](../properties/props-system-photo-meteringmode.md)

### <a name="pkey"></a>Pkey

Orientação da \_ foto PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ UI2

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=274} | ushort      |
| 2     | /xmp/tiff:Orientation  | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=274} | ushort      |
| 2     | /xmp/tiff:Orientation  | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort=274} |
| 2     | /xmp/tiff:orientation  |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/{ushort=274}         | ushort      |
| 2     | /ifd/xmp/tiff:Orientation | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/{ushort=274}         | ushort      |
| 2     | /ifd/xmp/tiff:Orientation | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /ifd/{ushort=274}         |
| 2     | /ifd/xmp/tiff:orientation |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Photo.Orientation](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
