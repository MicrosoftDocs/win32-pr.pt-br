---
description: A tabela AdvtExecuteSequence lista as ações que o instalador chama quando a ação ADVERTISE de nível superior é executada.
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: Tabela AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed9a566b721be1065e825cbf7cd6650a52c83ace653dc2730f1fcf7785d125c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381585"
---
# <a name="advtexecutesequence-table"></a>Tabela AdvtExecuteSequence

A tabela AdvtExecuteSequence lista as ações que o instalador chama quando a ação [ADVERTISE](advertise-action.md) de nível superior é executada.

Somente as ações a seguir podem ser usadas na tabela AdvtExecuteSequence. Ações personalizadas não podem ser usadas nesta tabela.

[CostFinalize](costfinalize-action.md)

[CostInitialize](costinitialize-action.md)

[CreateShortcuts](createshortcuts-action.md)

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
| Ação    | [Identificador](identifier.md) | Y   | N        |
| Condição | [Condição](condition.md)   | N   | Y        |
| Sequência  | [Inteiro](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Ação
</dt> <dd>

Nome da [ação padrão que](standard-actions.md) o instalador deve executar. Essa é a chave primária da tabela.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condição
</dt> <dd>

Expressão lógica. Se a expressão for avaliada como false, a ação será ignorada. Se a sintaxe de expressão for inválida, a sequência será encerrada, retornando iesBadActionData. Para obter informações sobre a sintaxe de instruções condicionais, consulte [Sintaxe de instrução condicional](conditional-statement-syntax.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Seqüência
</dt> <dd>

Um valor positivo indica a posição da sequência da ação. Os valores negativos a seguir indicam que a ação será chamada se o instalador retornar o sinalizador de encerramento. Cada sinalizador de terminação (valor negativo) pode ser usado com no máximo uma ação. Várias ações podem ter sinalizadores de término, mas devem ser sinalizadores diferentes. Sinalizadores de terminação (valores negativos) normalmente são usados com caixas [de diálogo](dialog-boxes.md).



| Sinalizador de término          | Valor | Descrição                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | Conclusão bem-sucedida. Usado com [caixas de diálogo](exit-dialog.md) Sair.               |
| msiDoActionStatusUserExit | -2    | O usuário encerra a instalação. Usado com [caixas de diálogo UserExit.](userexit-dialog.md)     |
| msiDoActionStatusFailure  | -3    | A saída fatal é encerrada. Usado com caixas [de diálogo FatalError.](fatalerror-dialog.md) |
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

 

 



