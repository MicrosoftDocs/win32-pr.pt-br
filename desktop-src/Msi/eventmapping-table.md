---
description: a tabela eventmappings lista os controles que assinam alguns eventos de controle e lista o atributo a ser alterado quando o evento é publicado por outro controle ou pelo Windows Installer.
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: Tabela EventMappings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f17380e3e91669926ef50532c36fec71f44d61eb2ed7273d053defe45fa874e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963106"
---
# <a name="eventmapping-table"></a>Tabela EventMappings

a tabela eventmappings lista os controles que assinam alguns eventos de controle e lista o atributo a ser alterado quando o evento é publicado por outro controle ou pelo Windows Installer.

A tabela EventMappings tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| caixa de diálogo\_  | [Identificador](identifier.md) | Y   | N        |
| controle\_ | [Identificador](identifier.md) | Y   | N        |
| Evento     | [Identificador](identifier.md) | Y   | N        |
| Atributo | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>'\_
</dt> <dd>

Uma chave externa para a primeira coluna da [tabela de diálogo](dialog-table.md). Esse campo e o campo de controle, \_ juntos, identificam um controle.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Controlo\_
</dt> <dd>

Uma chave externa para a segunda coluna da [tabela de controle](control-table.md). Esse campo e o campo da caixa de diálogo \_ identificam um controle.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Circunstância
</dt> <dd>

Esse campo é um identificador que especifica o tipo de evento que é assinado pelo controle. Para obter mais informações, consulte [visão geral do ControlEvent,](controlevent-overview.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute
</dt> <dd>

O nome do atributo de controle \_ que é definido quando o evento na coluna de evento é recebido. O argumento do evento é passado como o argumento da chamada de atributo para alterar esse atributo do controle.

</dd> </dl>

## <a name="remarks"></a>Comentários

A [tabela ControlEvent,](controlevent-table.md) especifica os eventos de controle que são iniciados quando um usuário interage com um controle de [pressão](pushbutton-control.md), [controle de caixa de seleção](checkbox-control.md)ou [controle SelectionTree](selectiontree-control.md). Esses são os únicos controles que um usuário pode usar para iniciar eventos de controle.

Mais de um controle em uma caixa de diálogo pode assinar o mesmo evento.

A lista a seguir identifica os usos típicos para a tabela EventMappings:

-   para assinar um [controle de texto](text-control.md) para um [ActionText controlevent,](actiontext-controlevent.md), [ActionData controlevent,](actiondata-controlevent.md), [ScriptInProgress controlevent,](scriptinprogress-controlevent.md) ou [timecontinueing controlevent,](timeremaining-controlevent.md) publicados pelo Windows Installer.
-   Para assinar um controle [ProgressBar](progressbar-control.md) ou um [controle de mensagem](billboard-control.md) para um ControlEvent, de [reprogress](setprogress-controlevent.md).
-   Para assinar um [controle DirectoryCombo](directorycombo-control.md) para um [IgnoreChange ControlEvent,](ignorechange-controlevent.md).
-   Para desabilitar automaticamente um [controle de pressão](pushbutton-control.md) localizado na mesma caixa de diálogo com um [controle SelectionTree](selectiontree-control.md). Para desabilitar o botão de ação quando nenhum recurso estiver listado no [controle SelectionTree](selectiontree-control.md), use a tabela EventMappings para assinar o controle de pressão para um [SelectionNoItems ControlEvent,](selectionnoitems-controlevent.md). Digite **habilitar** no campo atributos da tabela EventMappings.
-   Para exibir um [controle de texto](text-control.md) que mostra o caminho para o local de instalação do recurso selecionado em um [controle SelectionTree](selectiontree-control.md) na mesma caixa de diálogo. Use a tabela EventMappings para assinar o [controle de texto](text-control.md) para um [SelectionPathOn ControlEvent,](selectionpathon-controlevent.md) e [SelectionPath ControlEvent,](selectionpath-controlevent.md) publicados pelo [controle SelectionTree](selectiontree-control.md).
-   Para exibir um [controle de texto](text-control.md) que mostra uma descrição do item realçado em um [controle SelectionTree](selectiontree-control.md) localizado na mesma caixa de diálogo, use a tabela EventMappings para inscrever o [controle de texto](text-control.md) em um [SelectionDescription ControlEvent,](selectiondescription-controlevent.md), [SelectionSize ControlEvent,](selectionsize-controlevent.md) ou [selectionaction ControlEvent,](selectionaction-controlevent.md). Insira o **texto** no campo atributo da tabela EventMappings.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



