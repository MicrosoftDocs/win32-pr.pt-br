---
description: Notifica o instalador Windows para usar o Gerenciador de Reinicialização para desligar todos os aplicativos que têm arquivos em uso e reiniciá-los no final da instalação.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: RmShutdownAndRestart ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f483e485eeefc2d3a761a3d9c9ff95989a3150dcfd8fff6a36bfb6211504e95e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625886"
---
# <a name="rmshutdownandrestart-controlevent"></a>RmShutdownAndRestart ControlEvent

Esse evento notifica o instalador Windows para usar o [Gerenciador](../rstmgr/restart-manager-portal.md) de Reinicialização para desligar todos os aplicativos que têm arquivos em uso e reiniciá-los no final da instalação.

Esse ControlEvent não terá nenhum efeito se qualquer um dos seguintes for verdadeiro.

-   O sistema operacional que executa a instalação não é Windows Vista ou Windows Server 2008.
-   As interações com [o Gerenciador](../rstmgr/restart-manager-portal.md) de Reinicialização foram desabilitadas pela [**propriedade MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) ou pela política [DisableAutomaticApplicationShutdown.](disableautomaticapplicationshutdown.md)
-   No momento, não há nenhuma sessão [aberta do Gerenciador de Reinicialização.](../rstmgr/restart-manager-portal.md)
-   Todas as chamadas do instalador Windows para o [Gerenciador de Reinicialização](../rstmgr/restart-manager-portal.md) retornam uma falha.

## <a name="typical-use"></a>Usos comum

O evento de controle RMShutdownAndRestart é publicado somente por um [controle PushButton](pushbutton-control.md) na caixa de diálogo [MsiRMFilesInUse.](msirmfilesinuse-dialog.md)

 

 
