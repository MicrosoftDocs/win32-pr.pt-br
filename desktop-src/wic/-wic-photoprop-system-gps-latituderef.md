---
description: A política de metadados de foto para a propriedade System.GPS.LatitudeRef.
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: Política de metadados de foto System.GPS.LatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04412af5359e39eaf8e033b059b1c5460e33f6d7537c4763b009b11010fbe87a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087244"
---
# <a name="systemgpslatituderef-photo-metadata-policy"></a>Política de metadados de foto System.GPS.LatitudeRef

A política de metadados de foto para a [propriedade System.GPS.LatitudeRef.](../properties/props-system-gps-latitude.md)

### <a name="pkey"></a>Pkey

LatitudeRef \_ do GPS PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

O VT \_ LPWSTR é preferencial, mas o VT \_ LPSTR também é aceito.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="precedence-of-paths-jpeg"></a>Precedência de caminhos (JPEG)

Se o arquivo estiver no formato JPEG, o manipulador lerá, gravará e removerá os dados na seguinte ordem:



| Ordem | Caminho                         | Formato de disco | Obrigatório |
|-------|------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSLatitudeRef     | Unicode     | Sim      |
| 2     | /app1/ifd/gps/ \\ {ushort=1 \\ } | ASCII       | Não       |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador lerá, gravará e removerá os dados na seguinte ordem:



| Ordem | Caminho                         | Formato de disco | Obrigatório |
|-------|------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSLatitudeRef | Unicode     | Sim      |
| 2     | /ifd/gps/ \\ {ushort=1 \\ }      | ASCII       | Não       |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.LatitudeRef](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
