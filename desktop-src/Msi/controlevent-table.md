---
description: A tabela ControlEvent permite que o autor especifique os Eventos de Controle iniciados quando um usuário interage com um Controle PushButton, Controle CheckBox ou Controle SelectionTree.
ms.assetid: e34d17e9-cd6b-4a21-9abc-9562ee648c59
title: Tabela ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fec4837fa7d98289495bbb0773ae7260f957485cd87214dabf1999b1e1a876c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692996"
---
# <a name="controlevent-table"></a>Tabela ControlEvent

A tabela ControlEvent permite que [](control-events.md) o autor especifique os Eventos de Controle iniciados quando um usuário interage com um controle [PushButton,](pushbutton-control.md)controle [CheckBox](checkbox-control.md)ou [Controle SelectionTree](selectiontree-control.md). Esses são os únicos controles que os usuários podem usar para iniciar eventos de controle. Cada controle pode publicar vários eventos de controle. O instalador inicia cada evento na ordem especificada na coluna Ordenação. Por exemplo, um controle de botão de push pode publicar eventos para iniciar uma transição para outra caixa de diálogo, sair da sequência da caixa de diálogo e iniciar a instalação do arquivo.

A exceção a ser anotada é que cada controle pode publicar mais um [evento NewDialog](newdialog-controlevent.md) ou [spawnDialog.](spawndialog-controlevent.md) Se você precisar criar vários eventos de controle NewDialog e SpawnDialog nesta tabela, inclua também instruções condicionais nos campos Condição que garantem que no máximo um evento seja publicado. Se vários eventos de controle NewDialog e SpawnDialog forem selecionados para o mesmo controle, somente o evento com o maior valor na coluna Ordenação será publicado quando o controle for ativado.

A tabela ControlEvent tem as seguintes colunas.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| caixa de diálogo\_  | [Identificador](identifier.md) | Y   | N        |
| controle\_ | [Identificador](identifier.md) | Y   | N        |
| Evento     | [Formatado](formatted.md)   | Y   | N        |
| Argumento  | [Formatado](formatted.md)   | Y   | N        |
| Condição | [Condição](condition.md)   | Y   | Y        |
| Ordenando  | [Inteiro](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Diálogo\_
</dt> <dd>

Uma chave externa para a primeira coluna da [tabela Dialog](dialog-table.md). Combinar esse campo com o campo \_ Controle identifica um controle exclusivo.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controle\_
</dt> <dd>

Uma chave externa para a segunda coluna da [tabela Controle](control-table.md). Combinar esse campo com o campo \_ Diálogo identifica um controle exclusivo.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Um identificador que especifica o tipo de evento que deve ocorrer quando o usuário interage com o controle especificado por Dialog \_ e Control \_ . Para ver uma lista de valores possíveis, consulte [Visão geral de ControlEvent.](controlevent-overview.md)

Para definir uma propriedade com um controle, coloque \[ Nome da Propriedade neste campo e o novo valor no campo de \_ \] argumento. Coloque { } no campo de argumento para inserir o valor nulo.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argumento
</dt> <dd>

Um valor usado como um modificador ao disparar um evento específico.

Por exemplo, o argumento de [NewDialog ControlEvent](newdialog-controlevent.md) ou [SpawnDialog ControlEvent](spawndialog-controlevent.md) é o nome da caixa de diálogo e o argumento da ação [Instalar](install-action.md) é um número que define o nível de instalação.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condição
</dt> <dd>

Uma instrução condicional que determina se o instalador ativa o evento na coluna Evento. O instalador disparará o evento se a instrução condicional no campo Condição for avaliada como True. Portanto, coloque um 1 nessa coluna para garantir que o instalador acione o evento. O instalador não disparará o evento se o campo Condição contiver uma instrução que seja avaliada como False. O instalador não dispara um evento com um espaço em branco no campo Condição, a menos que nenhum outro evento do controle seja avaliada como True. Se nenhum dos campos Condição do controle nomeado no campo Controle for avaliada como True, o instalador disparará o evento que tem um campo Condição em branco e, se mais de um campo Condição estiver em branco, ele disparará o evento um deles com o maior valor no campo \_ Ordenação. Consulte [Sintaxe de instrução condicional](conditional-statement-syntax.md).

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Encomendar
</dt> <dd>

Um inteiro usado para ordenar vários eventos vinculados ao mesmo controle. Esse deve ser um número não negativo. Esse campo pode ser deixado em branco.

</dd> </dl>

## <a name="remarks"></a>Comentários

A [tabela EventMapping](eventmapping-table.md) lista os controles que assinam algum evento de controle e lista o atributo de controle a ser alterado quando esse evento é publicado por outro controle ou pelo instalador.

No Windows XP ou sistemas operacionais anteriores, os usuários podem publicar um evento de controle somente interagindo com um controle [de](checkbox-control.md) caixa de seleção ou controle [pushbutton](pushbutton-control.md). Com Windows Server 2003, os usuários podem publicar um evento de controle apenas interagindo com um Controle de Caixa de [Seleção,](checkbox-control.md) [Controle SelectionTree](selectiontree-control.md)e Controle [pushbutton](pushbutton-control.md). A listagem de outros controles no campo \_ Controle não tem nenhum efeito.

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

 

 



