---
description: A hora do sistema é a data atual e a hora do dia.
ms.assetid: 1a1e251e-2375-4134-bbd8-1e4670b9f9d2
title: Hora do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f505b18916bb79e19b4db67d0628bc92529b4d7372edcf041bb0265a5cd3daef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117958066"
---
# <a name="system-time"></a>Hora do sistema

A *hora do sistema* é a data atual e a hora do dia. O sistema mantém o tempo para que seus aplicativos tenham acesso imediato a um tempo preciso. O sistema baseia o tempo do sistema no UTC ( *tempo universal coordenado* ). O horário baseado em UTC é definido livremente como a data atual e a hora do dia em Greenwich, Inglaterra.

Quando o sistema é iniciado pela primeira vez, ele define a hora do sistema como um valor com base no relógio em tempo real do computador e, em seguida, atualiza regularmente a hora. Para recuperar a hora do sistema, use a função [**GetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime) . **GetSystemTime** copia o tempo para uma estrutura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) que contém membros individuais para mês, dia, ano, dia da semana, hora, minuto, segundo e milissegundos. É fácil exibir esse formato para um usuário.

Você também pode obter a hora do sistema no formato de hora do arquivo usando a função [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) . **GetSystemTimeAsFileTime** copia o tempo para uma estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

Para definir a hora do sistema, use a função [**SetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime) . **SetSystemTime** pressupõe que você especificou um horário baseado em UTC.

As funções [**GetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment) e [**SetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment) sincronizam o relógio de hora do dia com outra fonte de tempo usando um ajuste de tempo periódico aplicado a cada interrupção do relógio.

Observe que o sistema pode atualizar periodicamente o tempo sincronizando com uma fonte de tempo. Como a hora do sistema pode ser ajustada para frente ou para trás, não compare as leituras de hora do sistema para determinar o tempo decorrido. em vez disso, use um dos métodos descritos em [Windows tempo](windows-time.md).

 

 
