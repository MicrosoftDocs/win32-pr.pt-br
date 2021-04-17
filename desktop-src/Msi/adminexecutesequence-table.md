---
description: A tabela AdminExecuteSequence lista as ações que o instalador chama em sequência quando a ação de administrador de nível superior é executada.
ms.assetid: 33a2ef50-519b-424e-b510-55c21c5706a3
title: Tabela AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c62ae43f8436ab210765e5402751c5722b78b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770387"
---
# <a name="adminexecutesequence-table"></a>Tabela AdminExecuteSequence

A tabela AdminExecuteSequence lista as ações que o instalador chama em sequência quando a ação de [administrador](admin-action.md) de nível superior é executada.

As ações de administrador na sequência de instalação, até a [ação InstallValidate](installvalidate-action.md) e todas as caixas de diálogo de saída, estão localizadas na [tabela AdminUISequence](adminuisequence-table.md).

As ações de administrador da ação InstallValidate até o final da sequência de instalação estão na tabela AdminExecuteSequence. Como a tabela AdminExecuteSequence precisa ser autônoma, ela também contém as ações de inicialização necessárias, como [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md)e [CostFinalize](costfinalize-action.md).

As [ações personalizadas](custom-actions.md) que exigem uma interface do usuário devem usar [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) em vez de caixas de diálogo criadas usando a [tabela de diálogo](dialog-table.md).

As colunas são idênticas às da [tabela InstallExecuteSequence](installexecutesequence-table.md). A tabela AdminExecuteSequence tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| Ação    | [Identificador](identifier.md) | S   | N        |
| Condição | [Condição](condition.md)   | N   | S        |
| Sequência  | [Inteiro](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action
</dt> <dd>

Nome da ação a ser executada. Essa é uma ação padrão ou uma ação personalizada listada na [tabela CustomAction](customaction-table.md).

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
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICEM04](icem04.md)  
</dl>

 

 



