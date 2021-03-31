---
description: As ações personalizadas são agendadas em tabelas de sequência da mesma forma que as ações padrão.
ms.assetid: 1aea75b1-a498-405e-9208-91672455496b
title: Sequência de ações personalizadas de sequenciamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7c24fb91247a36880cb808c9b8e10437312cf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172005"
---
# <a name="sequencing-custom-actions"></a>Sequência de ações personalizadas de sequenciamento

As ações personalizadas são agendadas em tabelas de sequência da mesma forma que as ações padrão.

**Para agendar uma ação personalizada em uma tabela de sequência**

1.  Insira o nome da ação personalizada (que é a chave primária da tabela [CustomAction](customaction-table.md)) na coluna ação da tabela de [sequência](sequence-table-detailed-example.md) .
2.  Insira a sequência da ação personalizada em relação às outras ações na tabela na coluna sequência da tabela de [sequência](sequence-table-detailed-example.md) . Para obter mais informações sobre tabelas de sequência, consulte [usando uma tabela de sequência](using-a-sequence-table.md).
3.  Para ignorar condicionalmente a ação, insira uma expressão condicional na coluna condição da tabela de [sequência](sequence-table-detailed-example.md) . O instalador ignorará essa ação se a expressão for avaliada como FALSE.

Como no caso de ações padrão, as ações personalizadas que estão agendadas no [InstallUISequence](installuisequence-table.md) ou [AdminUISequence](adminuisequence-table.md) serão executadas somente se a interface do usuário interna estiver definida como o nível completo. O nível da interface do usuário é definido usando a função [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) .

As ações padrão e personalizada agendadas nas tabelas [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)ou [AdvtExecuteSequence](advtexecutesequence-table.md) não fazem alterações no sistema. Em vez disso, o instalador enfileira registros de execução em um script para execução subsequente durante o serviço de instalação. Se não houver nenhum serviço de instalação, as ações agendadas nessas tabelas serão executadas no mesmo contexto da sequência da interface do usuário.

Se o servidor do instalador não estiver registrado, as ações personalizadas serão executadas no lado do cliente. Se o servidor estiver registrado e usando o modo de interface do usuário completo, as ações personalizadas serão executadas no lado do servidor.

Se estiver usando a interface do usuário completa com o servidor, as ações iniciais anteriores à ação [InstallValidate](installvalidate-action.md) serão executadas no cliente para permitir a interação total. Em seguida, a execução é alternada para o servidor que repete essas ações e executa as ações de execução de script. Isso é seguido por um retorno ao cliente para as ações finais.

Observe que, se um produto for removido definindo seu principal recurso como ausente, a propriedade [**Remove**](remove.md) poderá não ser igual a All após a ação [InstallValidate](installvalidate-action.md) . Isso significa que qualquer ação personalizada que dependa de REMOVE = ALL deve ser sequenciada após a ação InstallValidate. Uma ação personalizada pode verificar remover para determinar se um produto foi definido para ser completamente desinstalado.

As ações personalizadas que fazem referência a um arquivo instalado como sua fonte, como o tipo de ação personalizada 17 (DLL), o tipo de ação personalizada 18 (EXE), o tipo de ação personalizada 21 (JScript) e o tipo de ação personalizada 22 (VBScript), devem aderir às seguintes restrições de sequenciamento.

-   A ação personalizada deve ser sequenciada após a ação [CostFinalize](costfinalize-action.md) para que o caminho para o arquivo referenciado possa ser resolvido.
-   Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas adiadas (em script) deverão ser sequenciadas após o [InstallFiles](installfiles-action.md).
-   Se o arquivo de origem ainda não estiver instalado no computador, as ações personalizadas do nondeferred deverão ser sequenciadas após a ação [InstallInitialize](installinitialize-action.md) .

As restrições de sequenciamento a seguir se aplicam a ações personalizadas que alteram ou atualizam um pacote de Windows Installer.

-   Se a ação personalizada alterar o pacote, como ao adicionar linhas a uma tabela, a ação deverá ser sequenciada antes da ação [InstallInitialize](installinitialize-action.md) .
-   Se a ação personalizada fizer alterações que afetem o custo, elas deverão ser sequenciadas antes da ação [CostInitialize](costfinalize-action.md) .
-   Se a ação personalizada alterar o estado de instalação de recursos ou componentes, ela deverá ser sequenciada antes da ação [InstallValidate](installvalidate-action.md) .

 

 



