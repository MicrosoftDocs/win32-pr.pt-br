---
description: Um ControlEvent especifica uma ação a ser tomada pelo instalador ou uma alteração nos atributos de um ou mais controles em uma caixa de diálogo. Para obter mais informações sobre ControlEvents, consulte Visão geral do ControlEvent.
ms.assetid: 8768acaa-884b-428f-a14e-3f39f8ea4ad5
title: Eventos de controle (Windows Instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd72e93da7ed84c845b5993b2a021119c861b682ab5eb4645c69c723b17a404
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075086"
---
# <a name="control-events-windows-installer"></a>Eventos de controle (Windows Instalador)

Um ControlEvent especifica uma ação a ser tomada pelo instalador ou uma alteração nos atributos de um ou mais controles em uma caixa de diálogo. Para obter mais informações sobre ControlEvents, consulte [Visão geral do ControlEvent.](controlevent-overview.md)

A tabela a seguir fornece links para obter mais informações sobre ControlEvents específicos.



| Evento de controle                                                       | Breve descrição de ControlEvent                                                                                                                                                                             |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ActionData](actiondata-controlevent.md)                           | Publica dados na ação mais recente.                                                                                                                                                                          |
| [ActionText](actiontext-controlevent.md)                           | Publica o nome da ação atual.                                                                                                                                                                     |
| [AddLocal](addlocal-controlevent.md)                               | Notifica o instalador para executar recursos localmente.                                                                                                                                                               |
| [AddSource](addsource-controlevent.md)                             | Notifica o instalador para executar recursos de sua origem.                                                                                                                                                     |
| [CheckExistingTargetPath](checkexistingtargetpath-controlevent.md) | Notifica o instalador para verificar se o caminho pode ser gravado.                                                                                                                                                |
| [CheckTargetPath](checktargetpath-controlevent.md)                 | Notifica o instalador para verificar se o caminho é válido.                                                                                                                                                      |
| [DirectoryListNew](directorylistnew-controlevent.md)               | Notifica o controle DirectoryList para criar uma nova pasta.                                                                                                                                                    |
| [DirectoryListOpen](directorylistopen-controlevent.md)             | Seleciona o diretório no controle DirectoryList.                                                                                                                                                           |
| [DirectoryListUp](directorylistup-controlevent.md)                 | Notifica o controle DirectoryList para selecionar o pai do diretório atual.                                                                                                                             |
| [Doaction](doaction-controlevent.md)                               | A caixa de diálogo notifica o instalador para executar uma ação personalizada.                                                                                                                                                 |
| [EnableRollback](enablerollback-controlevent.md)                   | Usado para ativar e desativar as funcionalidades de reação.                                                                                                                                                                |
| [EndDialog](enddialog-controlevent.md)                             | Notifica o instalador para remover uma caixa de diálogo modal.                                                                                                                                                          |
| [IgnoreChange](ignorechange-controlevent.md)                       | Publicado pelo controle DirectoryList quando uma pasta é realçada, mas não aberta.                                                                                                                           |
| [MsiLaunchApp](msilaunchapp-controlevent.md)                       | Esse evento de controle executa um arquivo especificado. **[Windows Instalador 4.5 e anteriores:](not-supported-in-windows-installer-4-5.md)** Sem suporte.<br/>                                                       |
| [MsiPrint](msiprint-controlevent.md)                               | Permite que o usuário imprima o conteúdo do [Controle ScrollableText.](scrollabletext-control.md) **[Windows Instalador 4.5 e anteriores:](not-supported-in-windows-installer-4-5.md)** Sem suporte.<br/> |
| [NewDialog](newdialog-controlevent.md)                             | Notifica o instalador para alterar uma caixa de diálogo modal para outra caixa de diálogo.                                                                                                                                  |
| [Reinstalar](reinstall-controlevent.md)                             | Inicia uma reinstalação de recursos.                                                                                                                                                                       |
| [ReinstallMode](reinstallmode-controlevent.md)                     | Especifica o modo de validação durante uma reinstalação.                                                                                                                                                        |
| [Removerr](remove-controlevent.md)                                   | Notifica o instalador quando os recursos são selecionados para remoção.                                                                                                                                                |
| [Redefinir](reset-controlevent.md)                                     | Redefine todos os valores de propriedade para os valores padrão usados quando a caixa de diálogo foi criada.                                                                                                                    |
| [RmShutdownAndRestart](rmshutdownandrestart-controlevent.md)       | Use o [Gerenciador de Reinicialização](/windows/desktop/RstMgr/restart-manager-portal) para desligar todos os aplicativos que têm arquivos em uso e reiniciá-los no final da instalação.                                                              |
| [ScriptInProgress](scriptinprogress-controlevent.md)               | Exibe uma cadeia de caracteres enquanto o script de execução é compilado.                                                                                                                                                     |
| [SelectionAction](selectionaction-controlevent.md)                 | Publicado por SelectionTree para descrever um item.                                                                                                                                                               |
| [SelectionBrowse](selectionbrowse-controlevent.md)                 | Publicado por SelectionTree para gerar uma caixa de diálogo.                                                                                                                                                             |
| [SelectionDescription](selectiondescription-controlevent.md)       | Publicado por SelectionTree para fornecer uma cadeia de caracteres no campo Descrição da Tabela de Recursos.                                                                                                                 |
| [SelectionNoItems](selectionnoitems-controlevent.md)               | Usado por SelectionTree para excluir texto ou desabilitar botões.                                                                                                                                                      |
| [SelectionPath](selectionpath-controlevent.md)                     | Publicado por SelectionTree para fornecer o caminho de um item.                                                                                                                                                    |
| [SelectionPathOn](selectionpathon-controlevent.md)                 | Publicado por SelectionTree para indicar se há um caminho associado a um recurso.                                                                                                                     |
| [SelectionSize](selectionsize-controlevent.md)                     | Publicado pelo controle SelectionTree para fornecer o tamanho de um item.                                                                                                                                            |
| [SetInstallLevel](setinstalllevel-controlevent.md)                 | O instalador altera o nível de instalação para um valor especificado.                                                                                                                                                |
| [SetProgress](setprogress-controlevent.md)                         | Publicado pelo instalador para fornecer o progresso da instalação.                                                                                                                                                  |
| [SetProperty](setproperty-controlevent.md)                         | Define uma propriedade especificada.                                                                                                                                                                                    |
| [SetTargetPath](settargetpath-controlevent.md)                     | Notifica o instalador para verificar e definir um caminho.                                                                                                                                                               |
| [SpawnDialog](spawndialog-controlevent.md)                         | Notifica o instalador para criar um filho de uma caixa modal.                                                                                                                                                      |
| [SpawnWaitDialog](spawnwaitdialog-controlevent.md)                 | Dispara uma caixa de diálogo especificada.                                                                                                                                                                              |
| [TimeRemaining](timeremaining-controlevent.md)                     | Publicado pelo instalador para fornecer o tempo restante na sequência de progresso.                                                                                                                            |
| [ValidateProductID](validateproductid-controlevent.md)             | Define ProductID como a ID completa do produto.                                                                                                                                                                        |



 

 

