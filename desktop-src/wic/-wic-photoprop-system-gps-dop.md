---
description: A política de metadados de foto para a propriedade System. GPS. DOP.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: Política de metadados de foto System. GPS. DOP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922641"
---
# <a name="systemgpsdop-photo-metadata-policy"></a>Política de metadados de foto System. GPS. DOP

A política de metadados de foto para a propriedade [System. GPS. DOP](../properties/props-system-gps-dop.md) .

### <a name="pkey"></a>PKEY

\_DOP de GPS PKEY \_

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Yes

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

R8 de VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Esse valor pode ser gravado escrevendo em System. GPS. DOPNumerator e System. GPS. DOPDenominator. Ele não pode ser gravado diretamente. Os valores de esquemas diferentes são reconciliados.

### <a name="precedence-of-paths-jpeg"></a>Precedência de caminhos (JPEG)

Se o arquivo estiver no formato JPEG, o manipulador lerá, gravará e removerá os dados na seguinte ordem:



| Ordem | Caminho                          | Formato de disco   | Obrigatório |
|-------|-------------------------------|---------------|----------|
| 1     | /xmp/exif:GPSDOP              | Racional de XMP  | Yes      |
| 2     | /App1/IFD/GPS/ \\ {UShort = 11 \\ } | Racional de EXIF | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador lerá, gravará e removerá os dados na seguinte ordem:



| Ordem | Caminho                     | Formato de disco   | Obrigatório |
|-------|--------------------------|---------------|----------|
| 1     | /ifd/xmp/exif:GPSDop     | Racional de XMP  | Yes      |
| 2     | /IFD/GPS/ \\ {UShort = 11 \\ } | Racional de EXIF | Não       |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. DOP](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
