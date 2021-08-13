---
description: A política de metadados de foto para a propriedade System. Image. VerticalResolution.
ms.assetid: a58b7463-3572-4ca8-8299-93d92d2f06fb
title: Política de metadados de foto System. Image. VerticalResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9962a00be34d227756d295e992174d6e80b6d058fc32af29ad9cde58a04ed07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710279"
---
# <a name="systemimageverticalresolution-photo-metadata-policy"></a>Política de metadados de foto System. Image. VerticalResolution

A política de metadados de foto para a propriedade [System. Image. VerticalResolution](../properties/props-system-image-verticalresolution.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Image \_ VerticalResolution

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
| 1     | /App1/IFD/{UShort = 283} |             |
| 2     | /xmp/tiff:YResolution  |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                        |
|-------|-----------------------------|
| 1     | /App1/IFD/EXIF/{UShort = 283} |
| 2     | /xmp/tiff:yresolution       |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{UShort = 283}    |             |
| 2     | /ifd/xmp/tiff:YResolution |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{UShort = 283}    |
| 2     | /ifd/xmp/tiff:yresolution |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Image. VerticalResolution](../properties/props-system-image-verticalresolution.md)
</dt> </dl>

 

 
