---
description: A política de metadados de foto para a propriedade System. GPS. diferencial.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: Política de metadados de foto System. GPS. diferencial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc3f114683d324a067fe4ce4034e2de5cfc88da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297364"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a>Política de metadados de foto System. GPS. diferencial

A política de metadados de foto para a propriedade [System. GPS. diferencial](../properties/props-system-gps-differential.md) .

### <a name="pkey"></a>PKEY

\_Diferencial do GPS PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_UI2 VT

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

VT \_ UI1, VT \_ UI2 e VT \_ UI4 são todos aceitos.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 30} | ushort      |
| 2     | /xmp/exif:GPSDifferential | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 30} | ushort      |
| 2     | /xmp/exif:GPSDifferential | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 30} |
| 2     | /xmp/exif:gpsdifferential |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 30}          | ushort      |
| 2     | /ifd/xmp/exif:GPSDifferential | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 30}          | ushort      |
| 2     | /ifd/xmp/exif:GPSDifferential | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                          |
|-------|-------------------------------|
| 1     | /IFD/GPS/{UShort = 30}          |
| 2     | /ifd/xmp/exif:gpsdifferential |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. diferencial](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
