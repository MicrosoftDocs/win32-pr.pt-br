---
description: A política de metadados de foto para a propriedade System.Photo.FlashModel.
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: Política de metadados de foto System.Photo.FlashModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c9e45e1ef759f2bee0d383cde3bcdabe8be67dc55a463ab6c9f7e6e05889a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204877"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a>Política de metadados de foto System.Photo.FlashModel

A política de metadados de foto para a [propriedade System.Photo.FlashModel.](../properties/props-system-photo-flashmodel.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ FlashModel

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



| Ordem | Caminho                           | Formato de disco | Formato de Dados | Obrigatório |
|-------|--------------------------------|-------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Sim      |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador usará a seguinte ordem de precedência ao ler ou escrever os dados.



| Ordem | Caminho                               | Formato de disco | Formato de Dados | Obrigatório |
|-------|------------------------------------|-------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Sim      |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Photo.FlashModel](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
