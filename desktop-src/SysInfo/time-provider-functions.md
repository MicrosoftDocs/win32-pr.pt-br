---
description: As funções a seguir são usadas por provedores de tempo.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Funções de provedor de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c0647574aaa807788e9cf510ce9293460c0394bcdaa794e243009ad6710bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884811"
---
# <a name="time-provider-functions"></a>Funções de provedor de tempo

As funções a seguir são usadas por provedores de tempo.



| Função                                                               | Descrição                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | Notifica o sistema de que há novos exemplos disponíveis.                                              |
| [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | Recupera as informações de estado do tempo do sistema.                                                           |
| [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | Registra um evento de provedor de tempo no log de eventos.                                                           |
| [**SetProviderStatusFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | Define as informações de status do provedor de tempo.                                                           |
| [**SetProviderStatusInfoFreeFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | Libera uma estrutura [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) .                          |
| [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | Uma função de retorno de chamada que é chamada pelo Gerenciador de provedores de tempo para desligar o provedor de tempo.        |
| [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | Uma função de retorno de chamada que é chamada pelo Gerenciador de provedores de tempo para enviar comandos para o provedor de tempo. |
| [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | Uma função de retorno de chamada que é chamada pelo Gerenciador de provedores de tempo quando a DLL do provedor de tempo é carregada.  |



 

 

 



