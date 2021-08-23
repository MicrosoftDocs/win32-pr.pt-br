---
description: A política de metadados de foto para a propriedade System. Photo. FlashManufacturer.
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: Política de metadados de foto System. Photo. FlashManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d81a57967e5b3f1139b0efabd85266bec80d10e06fb18251b0a6b9ef61a1e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964796"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a>Política de metadados de foto System. Photo. FlashManufacturer

A política de metadados de foto para a propriedade [System. Photo. FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FlashManufacturer

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



| Ordem | Caminho                                  | Formato de disco | Formato de Dados | Obrigatório |
|-------|---------------------------------------|-------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:FlashManufacturer | Unicode     |             | Sim      |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador usará a ordem de precedência a seguir ao ler ou gravar os dados.



| Ordem | Caminho                                      | Formato de disco | Formato de Dados | Obrigatório |
|-------|-------------------------------------------|-------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:FlashManufacturer | Unicode     |             | Sim      |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Photo. FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
