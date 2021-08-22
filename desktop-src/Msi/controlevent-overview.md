---
description: ControlEvents são análogos às mensagens do Microsoft Windows em aplicativos baseados no Win32.
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: Visão geral do ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2736c93a728e2419f2ac9c722be2149e6e3ac681c95428f3383570262eb583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045136"
---
# <a name="controlevent-overview"></a>Visão geral do ControlEvent,

ControlEvents são análogos às mensagens do Microsoft Windows em aplicativos baseados no Win32. no entanto, em vez de criar uma função de retorno de chamada para receber Windows mensagens e enviar Windows mensagens com a função [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) , o instalador da interface do usuário e os controles publicam [ControlEvents](control-events.md). Outros controles e o instalador podem ser especificados para assinar ControlEvents específicos que, em seguida, alterarão os atributos do controle de assinatura. Para adicionar controles de trabalho a caixas de diálogo, o autor da interface do usuário especifica a publicação de ControlEvents na [tabela ControlEvent,](controlevent-table.md) e assina os controles em ControlEvents na [tabela EventMappings](eventmapping-table.md).

O instalador publicará os seguintes eventos nos controles de assinatura listados na [tabela EventMappings](eventmapping-table.md). Um controle [ProgressBar](progressbar-control.md) ou [controle de mensagem](billboard-control.md) normalmente se inscreve em setProgress, o restante é assinado por [controles de texto](text-control.md).

[ActionData ControlEvent,](actiondata-controlevent.md)

[ActionText ControlEvent,](actiontext-controlevent.md)

[ControlEvent, de reprogress](setprogress-controlevent.md)

[ControlEvent, do timecontinueing](timeremaining-controlevent.md)

[ScriptInProgress ControlEvent,](scriptinprogress-controlevent.md)

Os eventos a seguir são publicados pelo controle quando a seleção de item é movida em um controle [SelectionTree](selectiontree-control.md) ou [directorylist](directorylist-control.md). Os controles de assinatura devem estar localizados na mesma caixa de diálogo e listados na tabela EventMappings.

[IgnoreChange ControlEvent,](ignorechange-controlevent.md)

[SelectionDescription ControlEvent,](selectiondescription-controlevent.md)

[SelectionSize ControlEvent,](selectionsize-controlevent.md)

[SelectionPath ControlEvent,](selectionpath-controlevent.md)

[ControlEvent, selectionaction](selectionaction-controlevent.md)

[SelectionNoItems ControlEvent,](selectionnoitems-controlevent.md)

Os ControlEvents a seguir podem ser publicados a critério de um usuário interagindo com um controle de [pressão](pushbutton-control.md) ou [controle de caixa de seleção](checkbox-control.md) em uma caixa de diálogo. O controle CheckBox só pode publicar os eventos ADDLOCAL, addsource, remove, DoAction e SetProperty. com as versões Windows Installer fornecidas com o Windows Server 2003 e posterior, o [controle SelectionTree](selectiontree-control.md) pode publicar o ControlEvents doaction, controlevent, e setproperty. O autor da interface do usuário deve listar o ControlEvent, na [tabela ControlEvent,](controlevent-table.md). O manipulador de interface do usuário do instalador é o assinante desses eventos.

[ControlEvent, ADDLOCAL](addlocal-controlevent.md)

[ControlEvent, addsource](addsource-controlevent.md)

[CheckExistingTargetPath ControlEvent,](checkexistingtargetpath-controlevent.md)

[CheckTargetPath ControlEvent,](checktargetpath-controlevent.md)

[ControlEvent, de doação](doaction-controlevent.md)

[EnableRollback ControlEvent,](enablerollback-controlevent.md)

[EndDialog ControlEvent,](enddialog-controlevent.md)

[NewDialog ControlEvent,](newdialog-controlevent.md)

[Reinstalar o ControlEvent,](reinstall-controlevent.md)

[Reinstalar o ControlEvent,](reinstallmode-controlevent.md)

[Remover ControlEvent,](remove-controlevent.md)

[Redefinir ControlEvent,](reset-controlevent.md)

[SetInstallLevel ControlEvent,](setinstalllevel-controlevent.md)

[ControlEvent, SetProperty](setproperty-controlevent.md)

[SetTargetPath ControlEvent,](settargetpath-controlevent.md)

[SpawnDialog ControlEvent,](spawndialog-controlevent.md)

[SpawnWaitDialog ControlEvent,](spawnwaitdialog-controlevent.md)

[ValidateProductID ControlEvent,](validateproductid-controlevent.md)

Um [controle de pressão](pushbutton-control.md) pode publicar os eventos a seguir em um controle [SelectionTree](selectiontree-control.md) ou um controle [directorylist](directorylist-control.md) da assinatura localizado na mesma caixa de diálogo. O controle de pressão deve ser listado na tabela ControlEvent, e os controles de assinatura devem ser listados na tabela EventMappings.

[SelectionBrowse ControlEvent,](selectionbrowse-controlevent.md)

[DirectoryListUp ControlEvent,](directorylistup-controlevent.md)

[DirectoryListNew ControlEvent,](directorylistnew-controlevent.md)

[DirectoryListOpen ControlEvent,](directorylistopen-controlevent.md)

Eventos de controle geralmente exigem que a interface do usuário seja executada no nível [*completo da interface do usuário*](f-gly.md) . A maioria dos ControlEvents não funcionará com uma [*interface do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md) , pois esses níveis só exibem caixas de diálogo sem janela restrita. Os eventos ActionText, addsource, setProgress, timepersisting e ScriptInProgress são exceções e funcionarão na interface do usuário reduzida ou básica. Para obter mais informações sobre níveis de IU, consulte [níveis de interface do usuário](user-interface-levels.md).

Você pode executar [ações personalizadas](custom-actions.md) publicando um ControlEvent, de um controle de [pressão](pushbutton-control.md) ou [controle de caixa de seleção](checkbox-control.md). Adicione um registro à [tabela ControlEvent,](controlevent-table.md) com os nomes da caixa de diálogo e o controle que está publicando o ControlEvent,. Esse controle deve publicar uma [doação ControlEvent,](doaction-controlevent.md) notificando o instalador para executar a ação personalizada. no Windows XP ou em sistemas anteriores, você não pode executar uma ação personalizada publicando um controlevent, de um [controle SelectionTree](selectiontree-control.md).

Para obter mais informações sobre ControlEvents específicos, consulte a lista de [ControlEvents](control-events.md) padrão na [referência da interface do usuário](user-interface-reference.md).

 

 
