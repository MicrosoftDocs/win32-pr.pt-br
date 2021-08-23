---
description: A política de metadados de foto para a propriedade System.GPS.DOP.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: Política de metadados de foto system.GPS.DOP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c414b7cb8648210175953e4c7b5f51a66f026cb45a06fd4d62918f2f8ac369
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087784"
---
# <a name="systemgpsdop-photo-metadata-policy"></a>Política de metadados de foto system.GPS.DOP

A política de metadados de foto para a [propriedade System.GPS.DOP.](../properties/props-system-gps-dop.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ DOP

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Sim

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ R8

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Esse valor pode ser escrito escrevendo em System.GPS.DOPNumerator e System.GPS.DOPDenominator. Ele não pode ser gravado diretamente. Valores de esquemas diferentes são reconciliados.

### <a name="precedence-of-paths-jpeg"></a>Precedência de caminhos (JPEG)

Se o arquivo estiver no formato JPEG, o manipulador lerá, gravará e removerá os dados na seguinte ordem:



| Ordem | Caminho                          | Formato de disco   | Obrigatório |
|-------|-------------------------------|---------------|----------|
| 1     | /xmp/exif:GPSDOP              | XMP racional  | Sim      |
| 2     | /app1/ifd/gps/ \\ {ushort=11 \\ } | EXIF racional | Não       |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador lerá, gravará e removerá os dados na seguinte ordem:



| Ordem | Caminho                     | Formato de disco   | Obrigatório |
|-------|--------------------------|---------------|----------|
| 1     | /ifd/xmp/exif:GPSDop     | XMP racional  | Sim      |
| 2     | /ifd/gps/ \\ {ushort=11 \\ } | EXIF racional | Não       |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.GPS.DOP](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
