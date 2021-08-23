---
description: A política de metadados de foto para a propriedade System. Photo. LensModel.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: Política de metadados de foto System. Photo. LensModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07fff44e14a04dab220f8dbce243a638710f30db253c43c1ff79a240bb32f3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441866"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a>Política de metadados de foto System. Photo. LensModel

A política de metadados de foto para a propriedade [System. Photo. LensModel](../properties/props-system-photo-lensmodel.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ LensModel

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

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
| 1     | /xmp/MicrosoftPhoto:LensModel | Unicode     | Sim      |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador usará a ordem de precedência a seguir ao ler ou gravar os dados.



| Ordem | Caminho                              | Formato de disco | Obrigatório |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensModel | Unicode     | Sim      |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. LensModel](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
