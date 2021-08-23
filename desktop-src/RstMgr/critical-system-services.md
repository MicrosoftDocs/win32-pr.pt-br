---
title: Serviços críticos do sistema
description: Os serviços críticos do sistema não podem ser interrompidos e reiniciados pelo Gerenciador de Reinicialização sem uma reinicialização do sistema. As atualizações para qualquer arquivo ou recurso em uso por um desses serviços exigem uma reinicialização do sistema.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8a50eca43a62d24e0ab6363844bef7457aaf05b34251f5d804dacabaead5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010224"
---
# <a name="critical-system-services"></a>Serviços críticos do sistema

Os serviços críticos do sistema não podem ser interrompidos e reiniciados pelo Gerenciador de Reinicialização sem uma reinicialização do sistema. As atualizações para qualquer arquivo ou recurso em uso por um desses serviços exigem uma reinicialização do sistema.

**Para determinar se um processo é um serviço crítico do sistema.**

1.  Registre o processo usando a [**função RmRegisterResources.**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources)
2.  Chame a [**função RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) para obter a estrutura [**RM PROCESS \_ \_ INFO.**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info)
3.  O **membro ApplicationType** da estrutura [**RM PROCESS INFO \_ \_ retornada**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) contém um valor de [**enumeração RM APP \_ \_ TYPE.**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) Esse valor é definido como **RmCriticial para** um processo crítico do sistema.

Os serviços críticos do sistema incluem smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, Sistema, svchost.exe com RPCSS e svchost.exe com Dcom/PnP.

 

 




