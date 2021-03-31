---
title: Política de metadados de foto System. Image. HorizontalResolution
description: A política de metadados de foto para a propriedade System. Image. HorizontalResolution.
ms.assetid: 1fe73c50-4179-4ea4-be1c-9e103fb65d59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade406e644524fea84ef6baf957aed661d2adf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662294"
---
# <a name="systemimagehorizontalresolution-photo-metadata-policy"></a>Política de metadados de foto System. Image. HorizontalResolution

A política de metadados de foto para a propriedade [System. Image. HorizontalResolution](../properties/props-system-image-horizontalresolution.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Image \_ HorizontalResolution

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Sim.

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

R8 de VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor é gerado pelo sistema e não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{UShort = 282} |             |
| 2     | /xmp/tiff:XResolution  |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /App1/IFD/EXIF/{UShort = 282} |             |
| 2     | /xmp/tiff:xresolution       |             |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 282}    |             |
| 2     | /ifd/xmp/tiff:XResolution |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 282}    |             |
| 2     | /ifd/xmp/tiff:xresolution |             |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Image. HorizontalResolution](../properties/props-system-image-horizontalresolution.md)
</dt> </dl>

 

 
