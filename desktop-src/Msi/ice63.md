---
description: ICE63 verifica se há sequenciamento adequado da ação RemoveExistingProducts.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f0de847a3b79c87b8ddc7dbaf3be64f88b9ef34df80d92737b6d9005ffdad24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142490"
---
# <a name="ice63"></a>ICE63

ICE63 verifica se há sequenciamento adequado da [ação RemoveExistingProducts](removeexistingproducts-action.md). A ação RemoveExistingProducts pode ser colocada:

1.  Entre InstallValidate e InstallInitialize
2.  Imediatamente após InstallInitialize ou depois de InstallInitialize se as ações entre InstallInitialize e RemoveExistingProducts não gerarem nenhuma ação de script.
3.  Imediatamente após InstallExecute ou InstallExecuteAgain e antes de InstallFinalize (a mesma restrição que acima se aplica).
4.  Após InstallFinalize.

A falha na correção de um aviso ou erro relatado pelo ICE63 leva à falha da atualização.

## <a name="result"></a>Resultado

ICE63 postará um aviso ou erro se o sequenciamento da ação RemoveExistingProducts não estiver correto.

## <a name="example"></a>Exemplo

ICE63 relata o seguinte erro para o exemplo mostrado.

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

A ação 'MyCustomAction' ocorre entre InstallInitialize e RemoveExistingProducts. Se MyCustomAction gerar qualquer ação no script, isso causará problemas na instalação.

Para corrigir esse erro, verifique se MyCustomAction não gera nenhuma ação de script nem sequencia as ações.

[Tabela InstallExecuteSequence](installexecutesequence-table.md)



| Ação                 | Condição | Sequência |
|------------------------|-----------|----------|
| InstallInitialize      |           | 1000     |
| MyCustomAction         |           | 1010     |
| RemoveExistingProducts |           | 1020     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



