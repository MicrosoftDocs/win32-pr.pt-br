---
title: Funções do Gerenciador de reinicialização
description: A API do Gerenciador de reinicialização usa as funções identificadas na tabela a seguir.
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- Gerente de reinicialização do Gerenciador de reinicialização, referência, funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d628fcd5c1f6488d69152340dd76ae59ac27ea93b2ca157179a052883a26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010194"
---
# <a name="restart-manager-functions"></a>Funções do Gerenciador de reinicialização

A API do Gerenciador de reinicialização usa as funções identificadas na tabela a seguir.



| Função                                           | Descrição                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | Modifica ações de desligamento ou reinicialização.                                                                                                                                                        |
| [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | Inicia uma nova sessão do Gerenciador de reinicialização.                                                                                                                                                        |
| [**RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | Une o processo de um aplicativo a uma sessão do Gerenciador de reinicialização existente.                                                                                                                  |
| [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | Encerra a sessão do Gerenciador de reinicialização.                                                                                                                                                            |
| [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | Registra os recursos, como nomes de filenames, nomes curtos de serviço ou estruturas de [**\_ \_ processo exclusivo do RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) , em uma sessão do Gerenciador de reinicialização.                                   |
| [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | Usado por instaladores para obter uma lista de todos os aplicativos afetados por recursos registrados e seu status atual.                                                                              |
| [**RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | Consulta o status de desligamento e reinicialização de modificações que já foram aplicadas.                                                                                                     |
| [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | Inicia o desligamento de aplicativos e serviços.                                                                                                                                        |
| [**RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | Remove as modificações de desligamento e reinicialização que já foram aplicadas.                                                                                                                   |
| [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | Reinicia os aplicativos e serviços que foram desligados pela função [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) e que foram registrados para reinicializar usando **RegisterApplicationRestart**. |
| [**RmCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | Cancela a função atual [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)ou [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) .                                                            |



 

 

 




