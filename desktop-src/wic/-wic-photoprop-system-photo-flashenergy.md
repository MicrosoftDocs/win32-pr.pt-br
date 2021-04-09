---
description: A política de metadados de foto para a propriedade System. Photo. FlashEnergy.
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: Política de metadados de foto System. Photo. FlashEnergy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c272b4d6d14bf2f2e81d0964a3dc4395ba62dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011678"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a>Política de metadados de foto System. Photo. FlashEnergy

A política de metadados de foto para a propriedade [System. Photo. FlashEnergy](../properties/props-system-photo-flashenergy.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FlashEnergy

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="input-type"></a>Tipo de entrada

Double

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41483} |             |
| 2     | /xmp/exif:FlashEnergy         |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 41483} |             |
| 2     | /xmp/exif:FlashEnergy         |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 41483} |
| 2     | /xmp/exif:flashenergy         |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41483}  |             |
| 2     | /ifd/xmp/exif:FlashEnergy |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 41483}  |             |
| 2     | /ifd/xmp/exif:FlashEnergy |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{UShort = 41483}  |
| 2     | /ifd/xmp/exif:flashenergy |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. FlashEnergy](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
