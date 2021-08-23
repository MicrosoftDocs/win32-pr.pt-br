---
description: A política de metadados de foto para a propriedade System.Photo.PeopleNames.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Política de metadados de foto System.Photo.PeopleNames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4118cc8242d6dfe8a91d0bcd2b6039095fdf180037f51205d3541b9aefa2cc0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087045"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a>Política de metadados de foto System.Photo.PeopleNames

A política de metadados de foto para a [propriedade System.Photo.PeopleNames.](../properties/props-system-photo-peoplenames.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ PeopleNames

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de saída

VT \_ VECTOR \| VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

StringMulti

### <a name="conflict-resolution-policy"></a>Política de resolução de conflitos

Valores de esquemas diferentes são reconciliados.

### <a name="jpeg-policy"></a>Política JPEG

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                                                           | Formato de disco |
|-------|----------------------------------------------------------------|-------------|
| 1     | /xmp/ <xmpstruct> MP:RegionInfo/ <xmpbag> MPRI:Regions | ushort      |



 

### <a name="write-paths"></a>Caminhos de gravação

Essa propriedade não pode ser escrita usando a política de metadados.

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                |
|-------|-------------------------------------|
| 1     | /xmp/ <xmpstruct> MP:RegionInfo |



 

### <a name="tiff-policies"></a>Políticas TIFF

### <a name="read-paths"></a>Ler caminhos



| Ordem | Caminho                                                               | Formato de disco |
|-------|--------------------------------------------------------------------|-------------|
| 1     | /ifd/xmp/ <xmpstruct> MP:RegionInfo/ <xmpbag> MPRI:Regions | ushort      |



 

### <a name="write-paths"></a>Caminhos de gravação

Essa propriedade não pode ser escrita usando a política de metadados.

### <a name="remove-paths"></a>Remover caminhos



| Ordem | Caminho                                    |
|-------|-----------------------------------------|
| 1     | /ifd/xmp/ <xmpstruct> MP:RegionInfo |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Photo.ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
