---
description: A política de metadados de foto para a propriedade System.Photo.LensManufacturer.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: Política de metadados de foto System.Photo.LensManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f6beebc06ce690b05da62c023480bec25b675a7a9ec6093cec1752ac3a0e343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881976"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a>Política de metadados de foto System.Photo.LensManufacturer

A política de metadados de foto para a [propriedade System.Photo.LensManufacturer.](../properties/props-system-photo-lensmanufacturer.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ LensManufacturer

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

Se o arquivo estiver no formato JPEG, o manipulador usará o caminho a seguir ao ler ou escrever os dados.



| Ordem | Caminho                                 | Formato de disco | Obrigatório |
|-------|--------------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Sim      |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador usará a seguinte ordem de precedência ao ler ou escrever os dados.



| Ordem | Caminho                                     | Formato de disco | Obrigatório |
|-------|------------------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Sim      |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Photo.LensManufacturer](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
