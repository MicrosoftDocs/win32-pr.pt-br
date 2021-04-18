---
description: A política de metadados de foto para a propriedade System. GPS. MapDatum.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: Política de metadados de foto System. GPS. MapDatum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7a279c79da3d2b1dd20563af35bd34233a1a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759517"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a>Política de metadados de foto System. GPS. MapDatum

A política de metadados de foto para a propriedade [System. GPS. MapDatum](../properties/props-system-gps-mapdatum.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ MapDatum

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-type"></a>Tipo de entrada

VT \_ LPWSTR é preferível, mas VT \_ LPSTR também é aceito

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="precedence-of-paths-jpeg"></a>Precedência de caminhos (JPEG)

Se o arquivo estiver no formato JPEG, o manipulador lerá, gravará e removerá os dados na seguinte ordem:



| Ordem | Caminho                          | Formato de disco | Obrigatório |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSMapDatum         | Unicode     | Yes      |
| 2     | /App1/IFD/GPS/ \\ {UShort = 18 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador lerá, gravará e removerá os dados na seguinte ordem:



| Ordem | Caminho                      | Formato de disco | Obrigatório |
|-------|---------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSMapDatum | Unicode     | Yes      |
| 2     | /IFD/GPS/ \\ {UShort = 18 \\ }  | ASCII       | Não       |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. GPS. MapDatum](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
