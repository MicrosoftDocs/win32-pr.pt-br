---
description: A política de metadados de foto para a propriedade System.GPS.LongitudeRef.
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: Política de metadados de foto System.GPS.LongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00908f0c76305c745e1146677f32bee7b9724c08510f273c1627ed56e139d02b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931726"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a>Política de metadados de foto System.GPS.LongitudeRef

A política de metadados de foto para a [propriedade System.GPS.LongitudeRef.](../properties/props-system-gps-longituderef.md)

### <a name="pkey"></a>Pkey

\_LongitudeRef do GPS \_ PKEY

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

Cadeia de caracteres.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="precedence-of-paths-jpeg"></a>Precedência de caminhos (JPEG)

Se o arquivo estiver no formato JPEG, o manipulador lerá, gravará e removerá os dados na seguinte ordem:



| Ordem | Caminho                         | Formato de disco | Obrigatório |
|-------|------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSLongitudeRef    | Unicode     | Sim      |
| 2     | /app1/ifd/gps/ \\ {ushort=3 \\ } | ASCII       | Não       |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador lerá, gravará e removerá os dados na seguinte ordem:



| Ordem | Caminho                          | Formato de disco | Obrigatório |
|-------|-------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSLongitudeRef | Unicode     | Sim      |
| 2     | /ifd/gps/ \\ {ushort=3 \\ }       | ASCII       | Não       |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.LongitudeRef](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
