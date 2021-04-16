---
description: A política de metadados de foto para a propriedade System. Photo. Peoplenames.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Política de metadados de foto System. Photo. Peoplenames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3de9f5adda67fcd0e555194500f109df078bdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754228"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a>Política de metadados de foto System. Photo. Peoplenames

A política de metadados de foto para a propriedade [System. Photo. peoplenames](../properties/props-system-photo-peoplenames.md) .

### <a name="pkey"></a>PKEY

PKEY \_ fotos de \_ pessoas

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

\_LPWStr do vetor VT VT \| \_

### <a name="input-type"></a>Tipo de entrada

StringMulti

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                                           | Formato de disco |
|-------|----------------------------------------------------------------|-------------|
| 1     | /XMP/ <xmpstruct> MP: RegionInfo/ <xmpbag> MPRI: regiões | ushort      |



 

### <a name="write-paths"></a>Caminhos de gravação

Esta propriedade não pode ser gravada usando a política de metadados.

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                |
|-------|-------------------------------------|
| 1     | /XMP/ <xmpstruct> MP: RegionInfo |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Caminhos de leitura



| Ordem | Caminho                                                               | Formato de disco |
|-------|--------------------------------------------------------------------|-------------|
| 1     | /IFD/XMP/ <xmpstruct> MP: RegionInfo/ <xmpbag> MPRI: regiões | ushort      |



 

### <a name="write-paths"></a>Caminhos de gravação

Esta propriedade não pode ser gravada usando a política de metadados.

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                    |
|-------|-----------------------------------------|
| 1     | /IFD/XMP/ <xmpstruct> MP: RegionInfo |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. programmode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
