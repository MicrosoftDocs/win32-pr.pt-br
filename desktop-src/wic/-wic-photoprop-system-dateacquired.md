---
description: A política de metadados de foto para a propriedade System. DateAcquired.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: Política de metadados de foto System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f126ccb4424d1489f671f61f719a505559a78c8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171522"
---
# <a name="systemdateacquired-photo-metadata-policy"></a>Política de metadados de foto System. DateAcquired

A política de metadados de foto para a propriedade [System. DateAcquired](../properties/props-system-dateacquired.md) .

### <a name="pkey"></a>PKEY

PKEY \_ DateAcquired

### <a name="containers"></a>Contêineres

JPEG, TIFF

### <a name="read-only"></a>Somente leitura

No

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
| 1     | /xmp/MicrosoftPhoto:DateAcquired | Cadeia de caracteres Unicode no formato de data XMP. | Yes      |



 

### <a name="precedence-of-paths-tiff"></a>Precedência de caminhos (TIFF)

Se o arquivo estiver no formato TIFF, o manipulador pesquisará os dados na seguinte ordem:



| Ordem | Caminho                                 | Formato de disco                        | Obrigatório |
|-------|--------------------------------------|------------------------------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:DateAcquired | Cadeia de caracteres Unicode no formato de data XMP. | Yes      |



 

## <a name="remarks"></a>Comentários

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. DateAcquired](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
