---
description: Notifica o Windows Installer para usar o Gerenciador de reinicialização para desligar todos os aplicativos que têm arquivos em uso e reiniciá-los no final da instalação.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: RmShutdownAndRestart ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc91d1de52f516c0728e8d6469fb8cddc2e50cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751633"
---
# <a name="rmshutdownandrestart-controlevent"></a>RmShutdownAndRestart ControlEvent,

Esse evento notifica a Windows Installer usar o Gerenciador de [reinicialização](../rstmgr/restart-manager-portal.md) para desligar todos os aplicativos que têm arquivos em uso e reiniciá-los no final da instalação.

Esse ControlEvent, não terá efeito se qualquer uma das seguintes opções for verdadeira.

-   O sistema operacional que executa a instalação do não é o Windows Vista ou o Windows Server 2008.
-   As interações com o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) foram desabilitadas pela propriedade [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) ou pela política [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .
-   Não há sessão do [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) aberta no momento.
-   Todas as chamadas do Windows Installer para o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) retornam uma falha.

## <a name="typical-use"></a>Usos comum

O evento de controle RMShutdownAndRestart é publicado somente por um controle de [pressão](pushbutton-control.md) na caixa de [diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) .

 

 
