---
title: Usando o Gerenciador de reinicialização com um instalador primário
description: O procedimento a seguir descreve como usar o Gerenciador de reinicialização para desligar e reiniciar aplicativos e serviços. Ao usar o Gerenciador de reinicialização com um único instalador, esse instalador também é o principal instalador que controla a interface do usuário.
ms.assetid: 8d2b4129-c595-4b11-9771-6dc953f4db40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764086166fc895d44f1a555f453d2941487c5d999adfa8d38581a12f07c9c45c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010004"
---
# <a name="using-restart-manager-with-a-primary-installer"></a>Usando o Gerenciador de reinicialização com um instalador primário

O procedimento a seguir descreve como usar o Gerenciador de reinicialização para desligar e reiniciar aplicativos e serviços. Ao usar o Gerenciador de reinicialização com um único instalador, esse instalador também é o principal instalador que controla a interface do usuário.

**Para usar o Gerenciador de reinicialização com um instalador primário**

1.  O instalador chama a função [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) para iniciar a sessão do Gerenciador de reinicialização e obter um identificador de sessão e uma chave.
2.  O instalador chama a função [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) para registrar recursos. O Gerenciador de reinicialização só pode usar recursos registrados para determinar quais aplicativos e serviços devem ser desligados e reiniciados. Todos os recursos que podem ser afetados pela instalação devem ser registrados com a sessão. Os recursos podem ser identificados por nome de arquivo, nome curto do serviço ou uma estrutura de [**\_ \_ processo exclusiva do RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) .
3.  O instalador chama a função [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) para obter uma matriz de estruturas de [**\_ \_ informações de processo do RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) que lista todos os aplicativos e serviços que devem ser desligados e reiniciados.

    Se o valor do parâmetro *lpdwRebootReason* retornado pela função [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) for diferente de zero, o Gerenciador de reinicialização não poderá liberar um recurso registrado pelo desligamento de um aplicativo ou serviço. Nesse caso, um desligamento e reinicialização do sistema é necessário para continuar a instalação. O instalador deve solicitar uma ação ao usuário, parar programas ou serviços ou agendar um desligamento e reinicialização do sistema.

    Se o valor do parâmetro *lpdwRebootReason* retornado pela função [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) for zero, o instalador deverá chamar a função [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) . Isso desliga os serviços e aplicativos que estão usando recursos registrados. O instalador deve executar as modificações do sistema necessárias para concluir a instalação. Por fim, o instalador deve chamar a função [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) para que o Gerenciador de reinicialização possa reiniciar os aplicativos que ele foi desligado e que foram registrados para uma reinicialização.

4.  O instalador pode usar a função [**RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter) para impedir que aplicativos e serviços especificados sejam desligados ou reiniciados por operações do Gerenciador de reinicialização. A função [**RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist) retorna uma lista de aplicativos e serviços a serem filtrados do desligamento e reinicialização. A função [**RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter) remove um filtro.
5.  O instalador chama a função [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) para fechar a sessão do Gerenciador de reinicialização.

Para obter um exemplo de trecho de código que mostra como iniciar e usar uma sessão do Gerenciador de reinicialização usando um instalador primário e, em seguida, unindo um instalador secundário à sessão existente, consulte [usando o Gerenciador de reinicialização com um instalador secundário](using-restart-manager-with-a-secondary-installer.md).

 

 




