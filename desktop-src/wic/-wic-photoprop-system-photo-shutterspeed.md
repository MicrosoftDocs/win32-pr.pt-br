---
description: A política de metadados de foto para a propriedade System.Photo.ShutterSpeed.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Política de metadados de foto System.Photo.ShutterSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad11550a19cd043fd5d182b2cf508aec3e26c64a0dc2ee1d1c24576ebf18f8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710095"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a>Política de metadados de foto System.Photo.ShutterSpeed

A política de metadados de foto para a [propriedade System.Photo.ShutterSpeed.](../properties/props-system-photo-shutterspeed.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ ShutterSpeed

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Sim

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ R8

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Esse valor é gerado de System.Photo.ShutterSpeedNumerator e System.Photo.ShutterSpeedDenominator. Ele não pode ser gravado diretamente. Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37377} |             |
| 2     | /xmp/exif:ShutterSpeedValue   |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37377} |             |
| 2     | /xmp/exif:ShutterSpeedValue   |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37377} |
| 2     | /xmp/exif:shutterspeedvalue   |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37377}        |             |
| 2     | /ifd/xmp/exif:ShutterSpeedValue |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37377}        |             |
| 2     | /ifd/xmp/exif:ShutterSpeedValue |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                            |
|-------|---------------------------------|
| 1     | /ifd/exif/{ushort=37377}        |
| 2     | /ifd/xmp/exif:shutterspeedvalue |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Photo.ShutterSpeed](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
