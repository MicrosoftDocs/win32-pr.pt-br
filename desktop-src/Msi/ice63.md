---
description: ICE63 verifica o sequenciamento adequado da ação RemoveExistingProducts.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5faa6f2ddbcb95cdf12966c2887fe9438a5d610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829189"
---
# <a name="ice63"></a>ICE63

ICE63 verifica o sequenciamento adequado da [ação RemoveExistingProducts](removeexistingproducts-action.md). A ação RemoveExistingProducts pode ser colocada:

1.  Entre InstallValidate e InstallInitialize
2.  Imediatamente após InstallInitialize ou depois de InstallInitialize se as ações entre InstallInitialize e RemoveExistingProducts não gerarem nenhuma ação de script.
3.  Imediatamente após InstallExecute ou InstallExecuteAgain e antes de InstallFinalize (a mesma restrição que acima se aplica).
4.  Após InstallFinalize.

Falha ao corrigir um aviso ou erro relatado por ICE63 leva a uma falha da atualização.

## <a name="result"></a>Resultado

ICE63 posta um aviso ou erro se o sequenciamento da ação RemoveExistingProducts não estiver correto.

## <a name="example"></a>Exemplo

ICE63 relata o seguinte erro para o exemplo mostrado.

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

A ação ' mycustomizable ' ocorre entre InstallInitialize e RemoveExistingProducts. Se mycustomizable gerar qualquer ação no script, isso causará problemas na instalação.

Para corrigir esse erro, verifique se mycustomizable não gera nenhuma ação de script ou resequenciar as ações.

[Tabela InstallExecuteSequence](installexecutesequence-table.md)



| Ação                 | Condição | Sequência |
|------------------------|-----------|----------|
| InstallInitialize      |           | 1000     |
| Mycustomizable         |           | 1010     |
| RemoveExistingProducts |           | 1020     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



