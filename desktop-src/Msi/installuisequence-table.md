---
description: A tabela InstallUISequence lista as ações que são executadas quando a ação de instalação de nível superior é executada e o nível de interface do usuário interno é definido como interface de usuários completa ou interface reduzida.
ms.assetid: 076d7c14-e302-4465-aed5-27a4b1f70ac8
title: Tabela InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2234ddcad587a495eceb79cc4511100f483bcfd96b388164f6e3c2d6a39eca3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013244"
---
# <a name="installuisequence-table"></a>Tabela InstallUISequence

A tabela InstallUISequence lista as ações que são executadas quando a ação de [instalação](install-action.md) de nível superior é executada e o nível de interface do usuário interno é definido como interface de usuários completa ou interface reduzida. O instalador ignorará as ações nesta tabela se o nível da interface do usuário estiver definido como interface básica ou não. Consulte [sobre a interface do usuário](about-the-user-interface.md).

As ações na sequência de instalação até a [ação InstallValidate](installvalidate-action.md)e as caixas de diálogo de saída estão localizadas na tabela InstallUISequence. Todas as ações do InstallValidate até o final da sequência de instalação estão na [tabela InstallExecuteSequence](installexecutesequence-table.md). Como a tabela InstallExecuteSequence precisa ser autônoma, ela tem todas as ações de inicialização necessárias, como a ação [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [Filecost](filecost-action.md)e [CostFinalize](costfinalize-action.md)e [ExecuteAction](executeaction-action.md).

A tabela InstallUISequence tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| Ação    | [Identificador](identifier.md) | Y   | N        |
| Condição | [Condição](condition.md)   | N   | Y        |
| Sequência  | [Inteiro](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action
</dt> <dd>

Nome da ação a ser executada. Essa é uma ação interna, uma ação personalizada ou um assistente de interface do usuário.

Chave de tabela primária.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema
</dt> <dd>

Este campo contém uma expressão condicional. Se a expressão for avaliada como false, a ação será ignorada. Se a sintaxe da expressão for inválida, a sequência será encerrada, retornando iesBadActionData. Para obter informações sobre a sintaxe de instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem
</dt> <dd>

O número nesta coluna determina a posição da sequência em que essa ação é executada.

Um valor positivo representa a posição da sequência. Um valor nulo indica que a ação nunca é executada. Os valores negativos a seguir indicam que essa ação será executada se o instalador retornar o sinalizador de encerramento associado. Cada sinalizador de encerramento (valor negativo) pode ser usado com no máximo uma ação. Várias ações podem ter sinalizadores de encerramento, mas devem ser sinalizadores diferentes. Os sinalizadores de término (valores negativos) normalmente são usados com [caixas de diálogo](dialog-boxes.md).



| Sinalizador de término          | Valor | Descrição                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Conclusão bem-sucedida. Usado com as caixas de diálogo de [saída](exit-dialog.md) .               |
| msiDoActionStatusUserExit | -2    | O usuário encerra a instalação. Usado com caixas de diálogo [UserExit](userexit-dialog.md) .     |
| msiDoActionStatusFailure  | -3    | Encerramentos de saída fatais. Usado com caixas de diálogo [FatalError](fatalerror-dialog.md) . |
| msiDoActionStatusSuspend  | -4    | A instalação está suspensa.                                                                |



 

Zero, todos os outros números negativos ou um valor nulo indicam que a ação nunca é executada.

</dd> </dl>

## <a name="remarks"></a>Comentários

O texto localizado associado para exibição de progresso ou registro em log está especificado na [tabela ActionText](actiontext-table.md).

Para obter um exemplo de uma tabela de sequência, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

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
[ICE86](ice86.md)  
</dl>

 

 



