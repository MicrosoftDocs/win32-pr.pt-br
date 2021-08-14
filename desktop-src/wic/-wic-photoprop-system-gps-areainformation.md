---
description: A política de metadados de foto para a propriedade System. GPS. AreaInformation.
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: Política de metadados de foto System. GPS. AreaInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4eee2cf4234902049241c833d1077814f5daf88187323c43bc1cb00f6f44aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205517"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a>Política de metadados de foto System. GPS. AreaInformation

A política de metadados de foto para a propriedade [System. GPS. AreaInformation](../properties/props-system-gps-areainformation.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ AreaInformation

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

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 28}    |             |
| 2     | /xmp/exif:GPSAreaInformation | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 28}    |             |
| 2     | /xmp/exif:GPSAreaInformation | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                         |
|-------|------------------------------|
| 1     | /App1/IFD/GPS/{UShort = 28}    |
| 2     | /xmp/exif:GPSAreaInformation |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 28}             |             |
| 2     | /ifd/xmp/exif:GPSAreaInformation | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 28}             |             |
| 2     | /ifd/xmp/exif:GPSAreaInformation | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{UShort = 28}             |
| 2     | /ifd/xmp/exif:GPSAreaInformation |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. AreaInformation](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
