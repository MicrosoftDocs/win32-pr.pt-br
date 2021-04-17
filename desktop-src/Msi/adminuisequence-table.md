---
description: A tabela AdminUISequence lista as ações que o instalador chama em sequência quando a ação de administrador de nível superior é executada e o nível da interface do usuário interna é definido como interface de usuários completa ou redução da IU.
ms.assetid: 7227846d-b755-4af9-acc3-e27742a5097a
title: Tabela AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8fb460f65d223e75ebd50a7587f5b3f4adeced8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748169"
---
# <a name="adminuisequence-table"></a>Tabela AdminUISequence

A tabela AdminUISequence lista as ações que o instalador chama em sequência quando a ação de [administrador](admin-action.md) de nível superior é executada e o nível da interface do usuário interna é definido como interface de usuários completa ou redução da IU. O instalador ignorará as ações nesta tabela se o nível da interface do usuário estiver definido como interface básica ou não. Consulte [sobre a interface do usuário](about-the-user-interface.md).

As ações de administrador na sequência de instalação até a [ação InstallValidate](installvalidate-action.md)e todas as caixas de diálogo de saída estão localizadas na tabela AdminUISequence. Todas as ações do InstallValidate até o final da sequência de instalação estão na [tabela AdminExecuteSequence](adminexecutesequence-table.md). Como a tabela AdminExecuteSequence precisa ser autônoma, ela também contém as ações de inicialização necessárias, como [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md)e [CostFinalize](costfinalize-action.md). Ele também tem a [ação ExecuteAction](executeaction-action.md).

As colunas são idênticas às da [tabela InstallUISequence](installuisequence-table.md). A tabela AdminUISequence tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| Ação    | [Identificador](identifier.md) | S   | N        |
| Condição | [Condição](condition.md)   | N   | S        |
| Sequência  | [Inteiro](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action
</dt> <dd>

Nome da ação a ser executada. Essa é uma ação padrão, um assistente de interface do usuário ou uma ação personalizada listada na [tabela CustomAction](customaction-table.md).

Chave de tabela primária.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema
</dt> <dd>

Expressão lógica. Se a expressão for avaliada como false, a ação será ignorada. Se a sintaxe da expressão for inválida, a sequência será encerrada, retornando iesBadActionData. Para obter informações sobre a sintaxe de instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem
</dt> <dd>

Um valor positivo indica a posição da sequência da ação. Os valores negativos a seguir indicam que a ação será chamada se o instalador retornar o sinalizador de término. Cada sinalizador de encerramento (valor negativo) pode ser usado com no máximo uma ação. Várias ações podem ter sinalizadores de encerramento, mas devem ser sinalizadores diferentes. Os sinalizadores de término (valores negativos) normalmente são usados com [caixas de diálogo](dialog-boxes.md).



| Sinalizador de término          | Valor | Descrição                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Conclusão bem-sucedida. Usado com as caixas de diálogo de [saída](exit-dialog.md) .               |
| msiDoActionStatusUserExit | -2    | O usuário encerra a instalação. Usado com caixas de diálogo [UserExit](userexit-dialog.md) .     |
| msiDoActionStatusFailure  | -3    | Encerramentos de saída fatais. Usado com caixas de diálogo [FatalError](fatalerror-dialog.md) . |
| msiDoActionStatusSuspend  | -4    | A instalação está suspensa.                                                                |



 

Zero, todos os outros números negativos ou um valor nulo indicam que a ação nunca é chamada.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE20](ice20.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE46](ice46.md)  
[ICE75](ice75.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICE96](ice96.md)  
[ICEM04](icem04.md)  
</dl>

 

 



