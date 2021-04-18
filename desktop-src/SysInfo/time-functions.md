---
description: As funções a seguir são usadas com a hora do sistema.
ms.assetid: 3733f611-c6a1-4d48-b21e-ada3490c5de1
title: Funções de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1187c029bac34411fdca28dd3b27322478de678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756349"
---
# <a name="time-functions"></a>Funções de tempo

As funções a seguir são usadas com a hora do sistema.



| Função                                                                   | Descrição                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**GetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime)                                     | Recupera a data e a hora atuais do sistema no formato UTC.                                              |
| [**GetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment)                 | Determina se o sistema está aplicando ajustes de tempo periódicos em seu relógio de hora do dia.          |
| [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata)                                    | Formata uma hora do sistema como uma cadeia de hora para uma localidade especificada.                                         |
| [**NtQuerySystemTime**](/windows/desktop/api/Winternl/nf-winternl-ntquerysystemtime)                             | Retorna a hora do sistema.                                                                               |
| [**RtlLocalTimeToSystemTime**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)               | Converte a hora local especificada em hora do sistema.                                                      |
| [**RtlTimeToSecondsSince1970**](/windows/desktop/api/Winternl/nf-winternl-rtltimetosecondssince1970)             | Converte a hora do sistema especificada para o número de segundos desde o primeiro segundo de 1º de janeiro de 1970. |
| [**SetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime)                                     | Define a data e a hora atuais do sistema.                                                                 |
| [**SetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment)                 | Habilita ou desabilita os ajustes de tempo periódicos no tempo do dia do sistema.                       |
| [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)                       | Converte uma hora do sistema em uma hora do arquivo.                                                                 |
| [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) | Converte uma hora UTC em uma hora local correspondente ao fuso horário especificado.                               |
| [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime) | Converte uma hora local em uma hora UTC.                                                                   |



 

As funções a seguir são usadas com a hora local.



| Função                                                                                           | Descrição                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-enumdynamictimezoneinformation)                           | Enumera as entradas de informações do horário de verão dinâmico armazenadas no registro.                                                             |
| [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime)                                         | Converte uma hora de arquivo UTC em uma hora de arquivo local.                                                                                                  |
| [**GetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation)                             | Recupera as configurações de fuso horário atual e horário de verão dinâmico.                                                                      |
| [**GetDynamicTimeZoneInformationEffectiveYears**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformationeffectiveyears) | Recupera um intervalo, expresso em anos, para o qual [**uma \_ \_ \_ informação de fuso horário dinâmico**](/windows/win32/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information) tem entradas válidas. |
| [**GetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime)                                                               | Recupera a data e a hora locais atuais.                                                                                                      |
| [**GetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)                                           | Recupera as configurações atuais de fuso horário.                                                                                                       |
| [**GetTimeZoneInformationForYear**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear)                             | Recupera as configurações de fuso horário para o ano e o fuso horário especificados.                                                                          |
| [**RtlLocalTimeToSystemTime**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)                                       | Converte a hora local especificada em hora do sistema.                                                                                               |
| [**SetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation)                             | Define o fuso horário atual e as configurações de horário de verão dinâmico.                                                                           |
| [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime)                                                               | Define a data e a hora locais atuais.                                                                                                           |
| [**SetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation)                                           | Define as configurações de fuso horário atuais.                                                                                                            |
| [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)                         | Converte uma hora UTC em uma hora local correspondente ao fuso horário especificado.                                                                        |
| [**SystemTimeToTzSpecificLocalTimeEx**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltimeex)                     | Converte uma hora UTC com configurações de horário de verão dinâmico para uma hora local correspondente no fuso horário especificado.                             |
| [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime)                         | Converte uma hora local em uma hora UTC.                                                                                                            |
| [**TzSpecificLocalTimeToSystemTimeEx**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtimeex)                     | Converte uma hora local com configurações de horário de verão dinâmico para a hora UTC.                                                                   |



 

As funções a seguir são usadas com a hora do arquivo.



| Função                                                   | Descrição                                                                                                     |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**CompareFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime)                 | Compara dois horários de arquivo.                                                                                        |
| [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) | Converte uma hora de arquivo UTC em uma hora de arquivo local.                                                                  |
| [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)       | Converte um arquivo de hora no formato de hora do sistema.                                                                     |
| [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime)                         | Recupera a data e a hora em que o arquivo ou diretório especificado foi criado, acessado e modificado pela última vez. |
| [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) | Recupera a data e a hora atuais do sistema no formato UTC.                                                       |
| [**LocalFileTimeToFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-localfiletimetofiletime) | Converte uma hora de arquivo local em uma hora de arquivo com base em UTC.                                                         |
| [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime)                         | Define a data e a hora em que o arquivo ou diretório especificado foi criado, acessado ou modificado pela última vez.       |
| [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)       | Converte uma hora do sistema em uma hora do arquivo.                                                                          |



 

As funções a seguir são usadas com a data e hora do MS-DOS.



| Função                                               | Descrição                                          |
|--------------------------------------------------------|------------------------------------------------------|
| [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) | Converte valores de data e hora do MS-DOS em uma hora do arquivo. |
| [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) | Converte uma hora de arquivo em valores de data e hora do MS-DOS. |



 

As funções a seguir são usadas com o tempo do Windows.



| Função                                 | Descrição                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) | Recupera informações de tempo do sistema.                                                                  |
| [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount)     | Recupera o número de milissegundos decorridos desde que o sistema foi iniciado, até 49,7 dias. |
| [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) | Recupera o número de milissegundos decorridos desde o início do sistema.                  |



 

As funções a seguir são usadas com contadores de desempenho de alta resolução.



| Função                                                              | Descrição                                                             |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)     | Recupera o valor atual do contador de desempenho de alta resolução. |
| [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) | Recupera a frequência do contador de desempenho de alta resolução.     |



 

As funções a seguir são usadas com o contador de desempenho auxiliar.



| Função                                                                                           | Descrição                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QueryAuxiliaryCounterFrequency**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryauxiliarycounterfrequency)                           | Consulta a frequência do contador auxiliar.                                                                                                                                                                      |
| [**ConvertAuxiliaryCounterToPerformanceCounter**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertauxiliarycountertoperformancecounter) | Converte o valor do contador auxiliar especificado para o valor do contador de desempenho correspondente; Opcionalmente, fornece o erro de conversão estimado em nanossegundos devido a latências e máximo possível descompasso. |
| [**ConvertPerformanceCounterToAuxiliaryCounter**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertperformancecountertoauxiliarycounter) | Converte o valor do contador de desempenho especificado para o valor do contador auxiliar correspondente; Opcionalmente, fornece o erro de conversão estimado em nanossegundos devido a latências e máximo possível descompasso. |



 

A função a seguir é usada com o tempo de interrupção.



| Função                                                                       | Descrição                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)                               | Obtém a contagem atual de tempo de interrupção.                                                                                                                                                                                                                |
| [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)                 | Obtém a contagem atual de tempo de interrupção, em uma forma mais precisa do que o [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) .                                                                                                                             |
| [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)               | Obtém a contagem atual de tempo de interrupção não polarizada. A contagem de tempo de interrupção não polarizada não inclui o tempo que o sistema gasta em suspensão ou hibernação.                                                                                                    |
| [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) | Obtém a contagem de tempo de interrupção não polarizada atual, em uma forma mais precisa do que o [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) . A contagem de tempo de interrupção não polarizada não inclui o tempo que o sistema gasta em suspensão ou hibernação. |



 

 

 
