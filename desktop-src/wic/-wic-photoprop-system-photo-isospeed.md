---
description: A política de metadados de foto para a propriedade System. Photo. ISOSpeed.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Política de metadados de foto System. Photo. ISOSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c01cb8c3e8e4c80c63985b49e8eda49ebe16d47982dde4cd051f555b8c93d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964795"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a>Política de metadados de foto System. Photo. ISOSpeed

A política de metadados de foto para a propriedade [System. Photo. ISOSpeed](../properties/props-system-photo-focallengthinfilm.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ ISOSpeed

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_UI2 VT

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 34855}           | ushort      |
| 2     | /XMP/ <xmpseq> EXIF: ISOSpeedRatings | Unicode     |
| 3     | /xmp/exif:ISOSpeed                      | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 34855}           | ushort      |
| 2     | /XMP/ <xmpseq> EXIF: ISOSpeedRatings | Unicode     |
| 3     | /xmp/exif:ISOSpeed                      | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                    |
|-------|-----------------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 34855}           |
| 2     | /XMP/ <xmpseq> EXIF: isospeedratings |
| 3     | /xmp/exif:isospeed                      |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                        | Formato de disco |
|-------|---------------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 34855}                    | ushort      |
| 2     | /IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings | Unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                                        | Formato de disco |
|-------|---------------------------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 34855}                    | ushort      |
| 2     | /IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings | Unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                        |
|-------|---------------------------------------------|
| 1     | /IFD/EXIF/{UShort = 34855}                    |
| 2     | /IFD/XMP/ <xmpseq> EXIF: isospeedratings |
| 3     | /ifd/xmp/exif:isospeed                      |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. ISOSpeed](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
