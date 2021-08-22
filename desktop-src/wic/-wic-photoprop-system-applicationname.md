---
description: A política de metadados de foto para a propriedade System. ApplicationName.
ms.assetid: bf4b310a-7e63-45c5-a327-2638fb31d676
title: Política de metadados de fotos do System. ApplicationName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3084f21453a82c79925d4a164f5f847c3a24968009b7b8c4236ce3a40872dad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710915"
---
# <a name="systemapplicationname-photo-metadata-policy"></a>Política de metadados de fotos do System. ApplicationName

A política de metadados de foto para a propriedade [System. ApplicationName](../properties/props-system-applicationname.md) .

### <a name="pkey"></a>PKEY

PKEY \_ ApplicationName

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-type"></a>Tipo de entrada

String

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                         | Formato de disco |
|-------|----------------------------------------------|-------------|
|       | /App1/IFD/{UShort = 305}                       | ascii       |
|       | Programa/app13/irb/8bimiptc/iptc/Originating |             |
|       | /xmp/xmp:CreatorTool                         | Unicode     |
|       | /xmp/xmp:creatortool                         | Unicode     |
|       | /XMP/TIFF: software                           | Unicode     |
|       | /XMP/TIFF: software                           | Unicode     |
|       | Programa/app13/irb/8bimiptc/iptc/Originating |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                                         | Formato de disco |
|-------|----------------------------------------------|-------------|
|       | /App1/IFD/{UShort = 305}                       | ascii       |
|       | /xmp/xmp:CreatorTool                         | Unicode     |
|       | /xmp/xmp:creatortool                         | Unicode     |
|       | /XMP/TIFF: software                           | Unicode     |
|       | /XMP/TIFF: software                           | Unicode     |
|       | Programa/app13/irb/8bimiptc/iptc/Originating |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                         |
|-------|----------------------------------------------|
|       | /App1/IFD/{UShort = 305}                       |
|       | /xmp/xmp:CreatorTool                         |
|       | /xmp/xmp:creatortool                         |
|       | /XMP/TIFF: software                           |
|       | /XMP/TIFF: software                           |
|       | Programa/app13/irb/8bimiptc/iptc/Originating |



 

### <a name="tiff-policy"></a>Política TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                       | Formato de disco |
|-------|--------------------------------------------|-------------|
|       | /IFD/{UShort = 305}                          | ascii       |
|       | Programa/ifd/iptc/Originating              |             |
|       | /ifd/xmp/xmp:CreatorTool                   | Unicode     |
|       | /ifd/xmp/xmp:creatortool                   | Unicode     |
|       | /IFD/XMP/TIFF: software                     | Unicode     |
|       | /IFD/XMP/TIFF: software                     | Unicode     |
|       | Programa/ifd/iptc/Originating              |             |
|       | Programa/ifd/irb/8bimiptc/iptc/Originating |             |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                                       | Formato de disco |
|-------|--------------------------------------------|-------------|
|       | /IFD/{UShort = 305}                          | ascii       |
|       | /ifd/xmp/xmp:CreatorTool                   | Unicode     |
|       | /ifd/xmp/xmp:creatortool                   | Unicode     |
|       | /IFD/XMP/TIFF: software                     | Unicode     |
|       | /IFD/XMP/TIFF: software                     | Unicode     |
|       | Programa/ifd/iptc/Originating              |             |
|       | Programa/ifd/irb/8bimiptc/iptc/Originating |             |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                       |
|-------|--------------------------------------------|
|       | /IFD/{UShort = 305}                          |
|       | /ifd/xmp/xmp:CreatorTool                   |
|       | /ifd/xmp/xmp:creatortool                   |
|       | /IFD/XMP/TIFF: software                     |
|       | /IFD/XMP/TIFF: software                     |
|       | Programa/ifd/iptc/Originating              |
|       | /ifd/irb/8bimiptc/iptc/Programa de origem |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.ApplicationName](../properties/props-system-applicationname.md)
</dt> </dl>

 

 
