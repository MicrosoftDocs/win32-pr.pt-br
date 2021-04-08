---
description: A política de metadados de foto para a propriedade System. GPS. DestLongitude.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: Política de metadados de foto System. GPS. DestLongitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e0a4f56e49dfbb3397b96cf7fae35a6065b7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011542"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a>Política de metadados de foto System. GPS. DestLongitude

A política de metadados de foto para a propriedade [System. GPS. DestLongitude](../properties/props-system-gps-destlongitude.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestLongitude

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_R8 de \| VT de vetor VT \_

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

\_R8 de \| VT de vetor VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor é gerado de System. GPS. DestLongitudeNumerator e System. GPS. DestLongitudeDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                       |
|-------|----------------------------|
| 1     | /App1/IFD/GPS/{UShort = 22}  |
| 2     | /xmp/exif:gpsdestlongitude |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                           |
|-------|--------------------------------|
| 1     | /IFD/GPS/{UShort = 22}           |
| 2     | /ifd/xmp/exif:gpsdestlongitude |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. DestLongitude](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
