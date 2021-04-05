---
description: ICE04 valida que o número de sequência de cada arquivo na tabela de arquivos é menor ou igual ao maior número de sequência na coluna LastSequence da tabela de mídia.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da25a23a26f8a2c49e224ad334791a6081b697b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922026"
---
# <a name="ice04"></a>ICE04

ICE04 valida que o número de sequência de cada arquivo na [tabela de arquivos](file-table.md) é menor ou igual ao maior número de sequência na coluna LastSequence da [tabela de mídia](media-table.md).

Cada registro na tabela de mídia representa um disco na mídia de origem que contém todos os arquivos com um número de sequência menor ou igual ao valor na coluna LastSequence e maior que o valor de LastSequence no registro do disco anterior.

## <a name="result"></a>Resultado

ICE04 posta uma mensagem de erro se houver um arquivo com um número de sequência maior que o maior número de LastSequence para a mídia de origem.

## <a name="example"></a>Exemplo

ICE04 relataria o seguinte erro para o exemplo mostrado:

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo   | Sequência |
|--------|----------|
| MyFile | 210      |



 

[Tabela de mídia](media-table.md) (parcial)



| DiskId | LastSequence |
|--------|--------------|
| 1      | 100          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



