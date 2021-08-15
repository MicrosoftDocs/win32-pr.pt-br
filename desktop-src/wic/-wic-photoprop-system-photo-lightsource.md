---
description: A política de metadados de foto para a propriedade System.Photo.LightSource.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: Política de metadados de foto System.Photo.LightSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195d165a6a929c8e0b4bf2dd165a5f22068a8b75e8ea4dfcddb5b8979900b035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204718"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a>Política de metadados de foto System.Photo.LightSource

A política de metadados de foto para a [propriedade System.Photo.LightSource.](../properties/props-system-photo-lightsource.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ LightSource

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ UI4

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37384} | ushort      |
| 2     | /xmp/exif:LightSource         | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37384} | ushort      |
| 2     | /xmp/exif:LightSource         | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37384} |
| 2     | /xmp/exif:lightsource         |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=37384}  | ushort      |
| 2     | /ifd/xmp/exif:LightSource | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=37384}  | ushort      |
| 2     | /ifd/xmp/exif:LightSource | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort=37384}  |
| 2     | /ifd/xmp/exif:lightsource |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Photo.LightSource](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
