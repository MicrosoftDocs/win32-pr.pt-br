---
title: Funções de agendamento
description: As funções de serviço de agendamento de gerenciamento de rede enviam e gerenciam trabalhos que são executados em um computador específico em um determinado momento (ou horários) no futuro.
ms.assetid: 1ddc9b95-fdbc-4e39-9b55-2a5bc570b95d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3421ae46de8e8152356f64d3855b4fe95c228878
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105778540"
---
# <a name="schedule-functions"></a>Funções de agendamento

As funções de serviço de agendamento de gerenciamento de rede enviam e gerenciam trabalhos que são executados em um computador específico em um determinado momento (ou horários) no futuro. Os trabalhos podem incluir comandos e programas. As funções gerenciam trabalhos em computadores remotos e locais, desde que o serviço de agendamento esteja em execução no computador.

As funções do serviço de agendamento são listadas a seguir.



| Função                                                                     | Descrição                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | Envia um trabalho para ser executado em uma data e hora futuras especificadas.        |
| [**NetScheduleJobDel**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | Cancela um intervalo de trabalhos na fila para execução em um computador.             |
| [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | Lista os trabalhos em fila em um computador especificado.                   |
| [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | Retorna informações sobre um trabalho específico na fila em um computador. |
| [**GetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | Recupera o nome da conta de serviço AT.                           |
| [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | Define o nome e a senha da conta de serviço AT.                   |



 

Para que as funções de agendamento de gerenciamento de rede tenham sucesso, um chamador deve ter o privilégio do administrador no computador em que o serviço de agendamento está sendo executado. As funções de serviço de agendamento também são conhecidas como funções "trabalho" e "no comando". Para obter mais informações sobre como chamar funções que exigem privilégios de administrador, consulte [executando com privilégios especiais](/windows/desktop/SecBP/running-with-special-privileges).

A estrutura de [**\_ informações de at**](/windows/desktop/api/Lmat/ns-lmat-at_info) é usada pela função [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd) para especificar informações ao enviar um trabalho e pela função [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo) para recuperar informações sobre um trabalho que foi enviado. A estrutura [**em \_ enum**](/windows/desktop/api/Lmat/ns-lmat-at_enum) é usada pelo [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum) para enumerar e retornar informações sobre uma fila inteira de trabalhos enviados.

 

 