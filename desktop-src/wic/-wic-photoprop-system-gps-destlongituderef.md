---
description: A política de metadados de foto para a propriedade System. GPS. DestLongitudeRef.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: Política de metadados de foto System. GPS. DestLongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8139fcf5218d9863393888d7ab7b188a53e7f55f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762517"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a>Política de metadados de foto System. GPS. DestLongitudeRef

A política de metadados de foto para a propriedade [System. GPS. DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS. DestLongitudeRef

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

VT \_ LPWSTR é preferível, mas VT \_ LPSTR também é aceito.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="precedence-of-paths-jpeg"></a>Precedência de caminhos (JPEG)

Se o arquivo estiver no formato JPEG, o manipulador lerá, gravará e removerá os dados na seguinte ordem:



| Ordem | Caminho                          | Formato de disco | Obrigatório |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSDestLongitudeRef | Unicode     | Yes      |
| 2     | /App1/IFD/GPS/ \\ {UShort = 21 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador lerá, gravará e removerá os dados na seguinte ordem:



| Ordem | Caminho                              | Formato de disco | Obrigatório |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSDestLongitudeRef | Unicode     | Yes      |
| 2     | /IFD/GPS/ \\ {UShort = 21 \\ }          | ASCII       | Não       |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. DestLongitudeRef](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
