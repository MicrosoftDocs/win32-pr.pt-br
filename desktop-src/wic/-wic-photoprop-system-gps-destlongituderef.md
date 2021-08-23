---
description: A política de metadados de foto para a propriedade System.GPS.DestLongitudeRef.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: Política de metadados de foto System.GPS.DestLongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fca1095138b35767da94e2eeed85a11892ba6edea3fa32f37ea6bd85fb76462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964945"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a>Política de metadados de foto System.GPS.DestLongitudeRef

A política de metadados de foto [para a propriedade System.GPS.DestLongitudeRef.](../properties/props-system-gps-destlongituderef.md)

### <a name="pkey"></a>Pkey

\_GPS PKEY. DestLongitudeRef

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

O VT \_ LPWSTR é preferencial, mas o VT \_ LPSTR também é aceito.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="precedence-of-paths-jpeg"></a>Precedência de caminhos (JPEG)

Se o arquivo estiver no formato JPEG, o manipulador lerá, gravará e removerá os dados na seguinte ordem:



| Ordem | Caminho                          | Formato de disco | Obrigatório |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSDestLongitudeRef | Unicode     | Sim      |
| 2     | /app1/ifd/gps/ \\ {ushort=21 \\ } | ASCII       | Não       |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador lerá, gravará e removerá os dados na seguinte ordem:



| Ordem | Caminho                              | Formato de disco | Obrigatório |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSDestLongitudeRef | Unicode     | Sim      |
| 2     | /ifd/gps/ \\ {ushort=21 \\ }          | ASCII       | Não       |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.DestLongitudeRef](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
