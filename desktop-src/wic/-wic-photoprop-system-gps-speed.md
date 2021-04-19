---
description: A política de metadados de foto para a propriedade System. GPS. Speed.
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: Política de metadados de foto System. GPS. Speed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d89f755114a73ab17388a1718d5ad0cbdf5a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763845"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a>Política de metadados de foto System. GPS. Speed

A política de metadados de foto para a propriedade [System. GPS. Speed](../properties/props-system-gps-speed.md) .

### <a name="pkey"></a>PKEY

\_Velocidade de GPS PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

R8 de VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor é gerado de System. GPS. SpeedNumerator e System. GPS. SpeedDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 13} |             |
| 2     | /xmp/exif:GPSSpeed        |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{UShort = 13} |             |
| 2     | /xmp/exif:GPSSpeed        |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{UShort = 13} |
| 2     | /xmp/exif:gpsspeed        |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 13}   |             |
| 2     | /ifd/xmp/exif:GPSSpeed |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{UShort = 13}   |             |
| 2     | /ifd/xmp/exif:GPSSpeed |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                   |
|-------|------------------------|
| 1     | /IFD/GPS/{UShort = 13}   |
| 2     | /ifd/xmp/exif:gpsspeed |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema. GPS. Speed](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
