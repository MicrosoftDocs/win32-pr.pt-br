---
description: A política de metadados de foto para a propriedade System. Photo. Obturation.
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: Política de metadados de foto System. Photo. Obturation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc02826b0602d0052f129640901ac3564a0eadb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813090"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a>Política de metadados de foto System. Photo. Obturation

A política de metadados de foto para a propriedade [System. Photo. Obturation](../properties/props-system-photo-aperture.md) .

### <a name="pkey"></a>PKEY

\_Abertura de foto PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

R8 de VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor é gerado em System. Photo. ApertureNumerator e System. Photo. ApertureDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37378} |             |
| 2     | /XMP/EXIF: Obturavalue       |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 37378} |             |
| 2     | /XMP/EXIF: Obturavalue       |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 37378} |
| 2     | /XMP/EXIF: obturavalue       |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37378}    |             |
| 2     | /IFD/XMP/EXIF: Obturavalue |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 37378}    |             |
| 2     | /IFD/XMP/EXIF: Obturavalue |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                        |
|-------|-----------------------------|
| 1     | /IFD/EXIF/{UShort = 37378}    |
| 2     | /IFD/XMP/EXIF: obturavalue |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. Obturation](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
