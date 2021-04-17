---
description: As funções a seguir são usadas por provedores de tempo.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Funções de provedor de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a24f15bd67751dc09a689078a8a518224267c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755291"
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



 

 

 



