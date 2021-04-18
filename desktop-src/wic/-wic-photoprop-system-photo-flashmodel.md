---
description: A política de metadados de foto para a propriedade System. Photo. FlashModel.
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: Política de metadados de foto System. Photo. FlashModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ade3769cb0d852239af84b769b85d5b3849589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763123"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a>Política de metadados de foto System. Photo. FlashModel

A política de metadados de foto para a propriedade [System. Photo. FlashModel](../properties/props-system-photo-flashmodel.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FlashModel

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

LPWStr do VT \_

### <a name="input-type"></a>Tipo de entrada

Cadeia de caracteres.

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="precedence-of-paths-jpeg"></a>Precedência de caminhos (JPEG)

Se o arquivo estiver no formato JPEG, o manipulador usará o caminho a seguir ao ler ou gravar os dados.



| Ordem | Caminho                           | Formato de disco | Formato de Dados | Obrigatório |
|-------|--------------------------------|-------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Yes      |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador usará a ordem de precedência a seguir ao ler ou gravar os dados.



| Ordem | Caminho                               | Formato de disco | Formato de Dados | Obrigatório |
|-------|------------------------------------|-------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Yes      |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. FlashModel](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
