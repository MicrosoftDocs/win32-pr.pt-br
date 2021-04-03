---
title: Serviços críticos do sistema
description: Serviços críticos do sistema não podem ser interrompidos e reiniciados pelo Gerenciador de reinicialização sem a reinicialização do sistema. As atualizações em qualquer arquivo ou recurso em uso por um desses serviços exigem uma reinicialização do sistema.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a8fcc921d065dda0670e27e240c93515bc8cb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006211"
---
# <a name="critical-system-services"></a>Serviços críticos do sistema

Serviços críticos do sistema não podem ser interrompidos e reiniciados pelo Gerenciador de reinicialização sem a reinicialização do sistema. As atualizações em qualquer arquivo ou recurso em uso por um desses serviços exigem uma reinicialização do sistema.

**Para determinar se um processo é um serviço de sistema crítico.**

1.  Registre o processo usando a função [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) .
2.  Chame a função [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) para obter a estrutura de [**\_ \_ informações do processo do RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) .
3.  O membro **ApplicationType** da estrutura de [**\_ \_ informações do processo RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) retornado contém um valor de enumeração de [**\_ \_ tipo de aplicativo RM**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) . Esse valor é definido como **RmCriticial** para um processo crítico do sistema.

Os serviços críticos do sistema incluem smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, sistema, svchost.exe com RPCSs e svchost.exe com DCOM/PnP.

 

 




