---
description: A política de metadados de foto para a propriedade System. Photo. LensManufacturer.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: Política de metadados de foto System. Photo. LensManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6696e7113a14a9b5b26a26f38258f30a5ba82cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170870"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a>Política de metadados de foto System. Photo. LensManufacturer

A política de metadados de foto para a propriedade [System. Photo. LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ LensManufacturer

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



| Ordem | Caminho                                 | Formato de disco | Obrigatório |
|-------|--------------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Yes      |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador usará a ordem de precedência a seguir ao ler ou gravar os dados.



| Ordem | Caminho                                     | Formato de disco | Obrigatório |
|-------|------------------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Yes      |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. LensManufacturer](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
