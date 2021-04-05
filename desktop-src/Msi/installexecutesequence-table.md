---
description: A tabela InstallExecuteSequence lista as ações que são executadas quando a ação de instalação de nível superior é executada.
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: Tabela InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d110debacab19739c3da69abf3948d11bb7aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827001"
---
# <a name="installexecutesequence-table"></a>Tabela InstallExecuteSequence

A tabela InstallExecuteSequence lista as ações que são executadas quando a ação de [instalação](install-action.md) de nível superior é executada.

As ações na sequência de instalação até a [ação InstallValidate](installvalidate-action.md)e todas as caixas de diálogo de saída estão localizadas na [tabela InstallUISequence](installuisequence-table.md). Todas as ações do InstallValidate até o final da sequência de instalação estão na tabela InstallExecuteSequence. Como a tabela InstallExecuteSequence precisa ser autônoma, ela tem todas as ações de inicialização necessárias, como as ações [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [filecost](filecost-action.md)e [CostFinalize](costfinalize-action.md) .

As [ações personalizadas](custom-actions.md) que exigem uma interface do usuário devem usar [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) em vez de caixas de diálogo criadas usando a [tabela de diálogo](dialog-table.md).

A tabela InstallExecuteSequence tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| Ação    | [Identificador](identifier.md) | S   | N        |
| Condição | [Condição](condition.md)   | N   | S        |
| Sequência  | [Inteiro](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action
</dt> <dd>

Nome da ação a ser executada. Essa é uma ação interna ou uma ação personalizada.

Chave de tabela primária.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema
</dt> <dd>

Este campo contém uma expressão condicional. Se a expressão for avaliada como false, a ação será ignorada. Se a sintaxe da expressão for inválida, a sequência será encerrada, retornando iesBadActionData. Para obter informações sobre a sintaxe de instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem
</dt> <dd>

Número que determina a posição da sequência em que essa ação deve ser executada.

Um valor positivo representa a posição da sequência. Um valor nulo indica que a ação não é executada. Os valores negativos a seguir indicam que essa ação deve ser executada se o instalador retornar o sinalizador de encerramento associado. Cada sinalizador de encerramento (valor negativo) pode ser usado com no máximo uma ação. Várias ações podem ter sinalizadores de encerramento, mas devem ser sinalizadores diferentes. Os sinalizadores de término (valores negativos) normalmente são usados com [caixas de diálogo](dialog-boxes.md).



| Sinalizador de término          | Valor | Descrição                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Conclusão bem-sucedida. Usado com as caixas de diálogo de [saída](exit-dialog.md) .               |
| msiDoActionStatusUserExit | -2    | O usuário encerra a instalação. Usado com caixas de diálogo [UserExit](userexit-dialog.md) .     |
| msiDoActionStatusFailure  | -3    | Encerramentos de saída fatais. Usado com caixas de diálogo [FatalError](fatalerror-dialog.md) . |
| msiDoActionStatusSuspend  | -4    | A instalação está suspensa.                                                                |



 

Zero, todos os outros números negativos ou um valor nulo indicam que a ação nunca é executada.

</dd> </dl>

## <a name="remarks"></a>Comentários

O texto localizado para exibição de progresso ou registro em log é especificado na [tabela ActionText](actiontext-table.md).

Para obter um exemplo de uma tabela de sequência, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE46](ice46.md)  
[ICE63](ice63.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE83](ice83.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
</dl>

 

 



