---
description: A política de metadados de foto para a propriedade System. GPS. VersionId.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: Política de metadados de foto System. GPS. VersionId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ca5bd1885f0ac5c3dc14dbb5e859de3f8a26cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797646"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a>Política de metadados de foto System. GPS. VersionId

A política de metadados de foto para a propriedade [System. GPS. VersionId](../properties/props-system-gps-versionid.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ VersionId

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

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

 

 
