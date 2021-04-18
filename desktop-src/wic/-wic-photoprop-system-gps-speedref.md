---
description: A política de metadados de foto para a propriedade System. GPS. SpeedRef.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: Política de metadados de foto System. GPS. SpeedRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c454a016dd77345c0a85e0ca3df1ae52694bd81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764041"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a>Política de metadados de foto System. GPS. SpeedRef

A política de metadados de foto para a propriedade [System. GPS. SpeedRef](../properties/props-system-gps-speedref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ SpeedRef

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

O ' VT \_ LPWSTR ' é preferencial, mas o ' VT \_ LPSTR ' também é aceito.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 12} |             |
| 2     | /xmp/exif:gpsspeedref     |             |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      |         |
|-------|---------------------------|---------|
| 1     | /IFD/GPS/{UShort = 12}      | ascii   |
| 2     | /ifd/xmp/exif:GPSSpeedRef | Unicode |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 12}      | ascii       |
| 2     | /ifd/xmp/exif:GPSSpeedRef | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /IFD/GPS/{UShort = 12}      |
| 2     | /ifd/xmp/exif:gpsspeedref |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. SpeedRef](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
