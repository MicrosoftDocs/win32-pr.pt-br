---
description: A política de metadados de foto para a propriedade System. Photo. FlashManufacturer.
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: Política de metadados de foto System. Photo. FlashManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1e785dfd00662acf065021a3c80de5c587586c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011677"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a>Política de metadados de foto System. Photo. FlashManufacturer

A política de metadados de foto para a propriedade [System. Photo. FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FlashManufacturer

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



| Ordem | Caminho                                  | Formato de disco | Formato de Dados | Obrigatório |
|-------|---------------------------------------|-------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:FlashManufacturer | Unicode     |             | Yes      |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador usará a ordem de precedência a seguir ao ler ou gravar os dados.



| Ordem | Caminho                                      | Formato de disco | Formato de Dados | Obrigatório |
|-------|-------------------------------------------|-------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:FlashManufacturer | Unicode     |             | Yes      |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
