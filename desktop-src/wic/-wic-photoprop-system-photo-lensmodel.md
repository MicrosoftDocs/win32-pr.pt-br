---
description: A política de metadados de foto para a propriedade System. Photo. LensModel.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: Política de metadados de foto System. Photo. LensModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a5249136346407ab9fcd1e4802d6910d3e514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011538"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a>Política de metadados de foto System. Photo. LensModel

A política de metadados de foto para a propriedade [System. Photo. LensModel](../properties/props-system-photo-lensmodel.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ LensModel

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



| Ordem | Caminho                          | Formato de disco | Obrigatório |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensModel | Unicode     | Yes      |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador usará a ordem de precedência a seguir ao ler ou gravar os dados.



| Ordem | Caminho                              | Formato de disco | Obrigatório |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensModel | Unicode     | Yes      |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. LensModel](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
