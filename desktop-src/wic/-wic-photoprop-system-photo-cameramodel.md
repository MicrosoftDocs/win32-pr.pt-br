---
description: A política de metadados de foto para a propriedade System. Photo. CameraModel.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: Política de metadados de foto System. Photo. CameraModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e205d4d886d050e45b958f2ba0f06c6411584c4a96a717378f243e5d1dd4fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882046"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a>Política de metadados de foto System. Photo. CameraModel

A política de metadados de foto para a propriedade [System. Photo. CameraModel](../properties/props-system-photo-cameramodel.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ CameraModel

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-type"></a>Tipo de entrada

Cadeia de caracteres.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 272} | ascii       |
| 2     | /XMP/TIFF: modelo        | Unicode     |
| 3     | /XMP/TIFF: modelo        | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 272} | ascii       |
| 2     | /XMP/TIFF: modelo        | Unicode     |
| 3     | /XMP/TIFF: modelo        | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                   |
|-------|------------------------|
| 1     | /App1/IFD/{UShort = 272} |
| 2     | /XMP/TIFF: modelo        |
| 3     | /XMP/TIFF: modelo        |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                | Formato de disco |
|-------|---------------------|-------------|
| 1     | /IFD/{UShort = 272}   | ascii       |
| 2     | /IFD/XMP/TIFF: modelo | Unicode     |
| 3     | /IFD/XMP/TIFF: modelo | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                | Formato de disco |
|-------|---------------------|-------------|
| 1     | /IFD/{UShort = 272}   | ascii       |
| 2     | /IFD/XMP/TIFF: modelo | Unicode     |
| 3     | /IFD/XMP/TIFF: modelo | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                |
|-------|---------------------|
| 1     | /IFD/{UShort = 272}   |
| 2     | /IFD/XMP/TIFF: modelo |
| 3     | /IFD/XMP/TIFF: modelo |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. CameraModel](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
