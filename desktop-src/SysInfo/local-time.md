---
description: Enquanto o sistema usa o tempo baseado em UTC internamente, seus aplicativos geralmente exibem a hora local, que é a data e hora do dia para o fuso horário.
ms.assetid: a6570ec5-ac77-427a-86d9-32cbecc62e37
title: Hora local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c60eb9ca53245a12eba1bc0096b522eae97de75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827327"
---
# <a name="local-time"></a>Hora local

Enquanto o sistema usa o tempo baseado em UTC internamente, seus aplicativos geralmente exibem a **hora local**, que é a data e hora do dia para o fuso horário. Portanto, para garantir os resultados corretos, você deve estar ciente se uma função espera receber uma hora baseada em UTC ou uma hora local, e se a função retorna um horário baseado em UTC ou uma hora local.

As configurações atuais de fuso horário controlam como o sistema é convertido entre o UTC e a hora local. Você pode recuperar as configurações de fuso horário atuais usando a função [**GetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation) . A função copia o resultado para uma estrutura de [**\_ \_ informações de fuso horário**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) e retorna um valor que indica se a hora local está atualmente em horário padrão ou horário de Verão (DST). Você pode definir as configurações de fuso horário usando a função [**SetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation) . Para dar suporte a limites para o horário de verão que mudam de ano para ano, use as funções [**GetTimeZoneInformationForYear**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear), [**GetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation) e [**SetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation) .

Para recuperar a hora local, use a função [**GetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime) . **GetLocalTime** converte a hora do sistema em uma hora local com base nas configurações atuais de fuso horário e copia o resultado para uma estrutura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) . Você pode definir a hora do sistema usando a função [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime) . **SetLocalTime** pressupõe que você especificou uma hora local e se converte em UTC antes de definir a hora do sistema.

Quando você chama [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime), o sistema usa as informações de fuso horário atuais, incluindo a configuração horário de verão, para executar a conversão. Observe que o sistema usa a configuração horário de Verão da hora atual, não a nova hora que você está definindo. Portanto, para garantir o resultado correto, chame **SetLocalTime** uma segunda vez, agora que a primeira chamada atualizou a configuração do horário de verão.

Para converter uma hora baseada em UTC em uma hora local, use a função [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) . Para converter uma hora local em um horário baseado em UTC, use a função [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime) .

 

 
