---
description: A tabela AdvtExecuteSequence lista ações que o instalador chama quando a ação de notificação de nível superior é executada.
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: Tabela AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b68a3f69cc7473b2364f169545743941d752f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828082"
---
# <a name="advtexecutesequence-table"></a>Tabela AdvtExecuteSequence

A tabela AdvtExecuteSequence lista ações que o instalador chama quando a ação de [notificação](advertise-action.md) de nível superior é executada.

Somente as ações a seguir podem ser usadas na tabela AdvtExecuteSequence. Não é possível usar ações personalizadas nesta tabela.

[CostFinalize](costfinalize-action.md)

[CostInitialize](costinitialize-action.md)

[Createatalhos](createshortcuts-action.md)

[InstallFinalize](installfinalize-action.md)

[InstallInitialize](installinitialize-action.md)

[InstallValidate](installvalidate-action.md)

[MsiPublishAssemblies](msipublishassemblies-action.md)

[PublishComponents](publishcomponents-action.md)

[PublishFeatures](publishfeatures-action.md)

[PublishProduct](publishproduct-action.md)

[RegisterClassInfo](registerclassinfo-action.md)

[RegisterExtensionInfo](registerextensioninfo-action.md)

[RegisterMIMEInfo](registermimeinfo-action.md)

[RegisterProgIdInfo](registerprogidinfo-action.md)

As colunas são idênticas às da [tabela InstallExecuteSequence](installexecutesequence-table.md). A tabela AdvtExecuteSequence tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| Ação    | [Identificador](identifier.md) | S   | N        |
| Condição | [Condição](condition.md)   | N   | S        |
| Sequência  | [Inteiro](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action
</dt> <dd>

Nome da [ação padrão](standard-actions.md) que o instalador deve executar. Esta é a chave primária da tabela.

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
[ICE27](ice27.md)  
[ICE46](ice46.md)  
[ICE72](ice72.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE83](ice83.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICEM04](icem04.md)  
</dl>

 

 



