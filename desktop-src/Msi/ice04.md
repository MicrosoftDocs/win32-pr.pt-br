---
description: ICE04 valida que o número de sequência de cada arquivo na tabela Arquivo é menor ou igual ao maior número de sequência na coluna LastSequence da tabela Mídia.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b77bf11d26d694a25f62db8da005139566b2c92310e2bb2dded4eecbca79719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635658"
---
# <a name="ice04"></a>ICE04

ICE04 valida que o número de [](file-table.md) sequência de cada arquivo na tabela Arquivo é menor ou igual ao maior número de sequência na coluna LastSequence da tabela [Mídia](media-table.md).

Cada registro na tabela Mídia representa um disco na mídia de origem que contém todos os arquivos com um número de sequência menor ou igual ao valor na coluna LastSequence e maior que o valor LastSequence no registro do disco anterior.

## <a name="result"></a>Resultado

ICE04 posta uma mensagem de erro se houver um arquivo com um número de sequência maior que o maior número LastSequence para a mídia de origem.

## <a name="example"></a>Exemplo

ICE04 relataria o seguinte erro para o exemplo mostrado:

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo   | Sequência |
|--------|----------|
| Myfile | 210      |



 

[Tabela de mídia](media-table.md) (parcial)



| DiskId | LastSequence |
|--------|--------------|
| 1      | 100          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



