---
description: A política de metadados de foto para a propriedade System. rating.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: Política de metadados de foto System. rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4f7d89b1ff1ea8326c2d26fba0d331db1eab1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297084"
---
# <a name="systemrating-photo-metadata-policy"></a>Política de metadados de foto System. rating

A política de metadados de foto para a propriedade [System. rating](../properties/props-system-rating.md) .

### <a name="pkey"></a>PKEY

Classificação de PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_UI4 VT

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

Pode ser VT \_ UI1, VT \_ UI2 ou VT \_ UI4. O valor pode variar de 0 a 99.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /App1/IFD/{UShort = 18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto: classificação | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /App1/IFD/{UShort = 18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto: classificação | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                       |
|-------|----------------------------|
| 1     | /App1/IFD/{UShort = 18249}   |
| 2     | /XMP/microsoftphoto: classificação |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/{UShort = 18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto: classificação | Unicode     |



 

### <a name="write-paths"></a>Caminhos de gravação



| Ordem | Caminho                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/{UShort = 18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto: classificação | Unicode     |



 

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                           |
|-------|--------------------------------|
| 1     | /IFD/{UShort = 18249}            |
| 2     | /IFD/XMP/microsoftphoto: classificação |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. rating](../properties/props-system-rating.md)
</dt> </dl>

 

 
