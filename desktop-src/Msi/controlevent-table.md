---
description: A tabela ControlEvent, permite que o autor especifique os eventos de controle iniciados quando um usuário interage com um controle de pressão, controle de caixa de seleção ou controle SelectionTree.
ms.assetid: e34d17e9-cd6b-4a21-9abc-9562ee648c59
title: Tabela ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721dc7ac9a729b8df0623a2958a4d0fe32851307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837111"
---
# <a name="controlevent-table"></a>Tabela ControlEvent,

A tabela ControlEvent, permite que o autor especifique os [eventos de controle](control-events.md) iniciados quando um usuário interage com um [controle de pressão](pushbutton-control.md), controle de caixa de [seleção](checkbox-control.md)ou [controle SelectionTree](selectiontree-control.md). Esses são os únicos controles que os usuários podem usar para iniciar eventos de controle. Cada controle pode publicar vários eventos de controle. O instalador inicia cada evento na ordem especificada na coluna ordenação. Por exemplo, um controle de botão de ação pode publicar eventos para iniciar uma transição para outra caixa de diálogo, sair da sequência da caixa de diálogo e iniciar a instalação do arquivo.

A exceção a ser observada é que cada controle pode publicar um evento mais [NewDialog](newdialog-controlevent.md) ou um [SpawnDialog](spawndialog-controlevent.md) . Se você precisar criar vários eventos de controle NewDialog e SpawnDialog nesta tabela, também inclua instruções condicionais nos campos de condição que asseguram que, no máximo, um evento seja publicado. Se vários eventos de controle NewDialog e SpawnDialog forem selecionados para o mesmo controle, somente o evento com o maior valor na coluna ordenação será publicado quando o controle for ativado.

A tabela ControlEvent, tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| caixa de diálogo\_  | [Identificador](identifier.md) | S   | N        |
| controle\_ | [Identificador](identifier.md) | S   | N        |
| Evento     | [Binário](formatted.md)   | S   | N        |
| Argumento  | [Binário](formatted.md)   | S   | N        |
| Condição | [Condição](condition.md)   | S   | S        |
| Ordenando  | [Inteiro](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>'\_
</dt> <dd>

Uma chave externa para a primeira coluna da [tabela de diálogo](dialog-table.md). A combinação desse campo com o \_ campo de controle identifica um controle exclusivo.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controlo\_
</dt> <dd>

Uma chave externa para a segunda coluna da [tabela de controle](control-table.md). A combinação deste campo com o campo de caixa de diálogo \_ identifica um controle exclusivo.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Circunstância
</dt> <dd>

Um identificador que especifica o tipo de evento que deve ocorrer quando o usuário interage com o controle especificado pela caixa de diálogo \_ e controle \_ . Para obter uma lista de valores possíveis, consulte [visão geral do ControlEvent,](controlevent-overview.md).

Para definir uma propriedade com um controle, coloque \[ \_ o nome \] da propriedade nesse campo e o novo valor no campo argumento. Coloque {} no campo de argumento para inserir o valor nulo.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argumento
</dt> <dd>

Um valor usado como um modificador ao disparar um evento específico.

Por exemplo, o argumento de [NewDialog ControlEvent,](newdialog-controlevent.md) ou [SpawnDialog ControlEvent,](spawndialog-controlevent.md) é o nome da caixa de diálogo e o argumento da [ação de instalação](install-action.md) é um número que define o nível de instalação.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema
</dt> <dd>

Uma instrução condicional que determina se o instalador ativa o evento na coluna de evento. O instalador acionará o evento se a instrução condicional no campo condição for avaliada como true. Portanto, coloque um 1 nesta coluna para garantir que o instalador dispare o evento. O instalador não acionará o evento se o campo condição contiver uma instrução que seja avaliada como false. O instalador não aciona um evento com um espaço em branco no campo condição, a menos que nenhum outro evento do controle seja avaliado como true. Se nenhum dos campos de condição do controle nomeado no campo de controle \_ for avaliado como true, o instalador acionará um evento com condição em branco e, se mais de um campo de condição estiver em branco, ele acionará um evento com o maior valor no campo de ordenação. Consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordenação
</dt> <dd>

Um inteiro usado para ordenar vários eventos vinculados ao mesmo controle. Este deve ser um número não negativo. Este campo pode ser deixado em branco.

</dd> </dl>

## <a name="remarks"></a>Comentários

A [tabela EventMappings](eventmapping-table.md) lista os controles que assinam um evento de controle e lista o atributo de controle a ser alterado quando esse evento é publicado por outro controle ou o instalador.

No Windows XP ou em sistemas operacionais anteriores, os usuários podem publicar um evento de controle apenas interagindo com um [controle de caixa de seleção](checkbox-control.md) ou controle de [pressão](pushbutton-control.md). Com o Windows Server 2003, os usuários podem publicar um evento de controle apenas interagindo com um [controle de caixa de seleção](checkbox-control.md), [controle SelectionTree](selectiontree-control.md)e [controle de supressão](pushbutton-control.md). A listagem de outros controles no \_ campo de controle não tem nenhum efeito.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE32](ice32.md)  
[ICE44](ice44.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



