---
description: A política de metadados de foto para a propriedade System. DateAcquired.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: Política de metadados de foto System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95b8f68d99476db0832a321de1f61c6f3c4dc6be6f10d679735bd51fc92ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087877"
---
# <a name="systemdateacquired-photo-metadata-policy"></a>Política de metadados de foto System. DateAcquired

A política de metadados de foto para a propriedade [System. DateAcquired](../properties/props-system-dateacquired.md) .

### <a name="pkey"></a>PKEY

PKEY \_ DateAcquired

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

Não

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de saída

FILETIME do VT \_

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

FILETIME do VT \_

### <a name="conflict-resolution-policy"></a>Política de resolução de conflito

Os valores de esquemas diferentes são reconciliados.

### <a name="precedence-of-paths-jpeg"></a>Precedência de caminhos (JPEG)

Se o arquivo estiver no formato JPEG, o manipulador pesquisará os dados na seguinte ordem:



| Ordem | Caminho                             | Formato de disco                        | Obrigatório |
|-------|----------------------------------|------------------------------------|----------|
| 1     | /xmp/MicrosoftPhoto:DateAcquired | Cadeia de caracteres Unicode no formato de data XMP. | Sim      |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador pesquisará os dados na seguinte ordem:



| Ordem | Caminho                                 | Formato de disco                        | Obrigatório |
|-------|--------------------------------------|------------------------------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:DateAcquired | Cadeia de caracteres Unicode no formato de data XMP. | Sim      |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. DateAcquired](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
