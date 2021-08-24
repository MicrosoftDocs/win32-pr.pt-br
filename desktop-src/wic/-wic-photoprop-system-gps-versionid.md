---
description: A política de metadados de foto para a propriedade System. GPS. VersionId.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: Política de metadados de foto System. GPS. VersionId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857ecb6b172dafa2a771d9e81f8b570a89f458c79b7630a2f231ce84dbec4f9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706356"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a>Política de metadados de foto System. GPS. VersionId

A política de metadados de foto para a propriedade [System. GPS. VersionId](../properties/props-system-gps-versionid.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ VersionId

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_ \| \_ interface do usuário VT de vetor VT

### <a name="input-type"></a>Tipo de entrada

Buffer

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policies"></a>Políticas JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 0} |             |
| 2     | /xmp/exif:GPSVersionID   | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 0} |             |
| 2     | /xmp/exif:GPSVersionID   | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{UShort = 0} |
| 2     | /xmp/exif:gpsversionid   |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{UShort = 0}        |
| 2     | /ifd/xmp/exif:gpsversionid |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. VersionId](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
