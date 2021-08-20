---
description: As funções a seguir são usadas com a hora do sistema.
ms.assetid: 3733f611-c6a1-4d48-b21e-ada3490c5de1
title: Funções de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d537224ceaf072fd5e11f0fdd839215c7317a5378de90e1be56def3f90490105
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117958039"
---
# <a name="time-functions"></a>Funções de tempo

As funções a seguir são usadas com a hora do sistema.



| Função                                                                   | Descrição                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**Getsystemtime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime)                                     | Recupera a data e hora atuais do sistema no formato UTC.                                              |
| [**GetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment)                 | Determina se o sistema está aplicando ajustes periódicos de tempo ao relógio de hora do dia.          |
| [**Gettimeformat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata)                                    | Formatar uma hora do sistema como uma cadeia de caracteres de tempo para uma localidade especificada.                                         |
| [**NtQuerySystemTime**](/windows/desktop/api/Winternl/nf-winternl-ntquerysystemtime)                             | Retorna a hora do sistema.                                                                               |
| [**RtlLocalTimeToSystemTime**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)               | Converte a hora local especificada em hora do sistema.                                                      |
| [**RtlTimeToSecondsSince1970**](/windows/desktop/api/Winternl/nf-winternl-rtltimetosecondssince1970)             | Converte a hora do sistema especificada para o número de segundos desde o primeiro segundo de 1º de janeiro de 1970. |
| [**SetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime)                                     | Define a data e a hora atuais do sistema.                                                                 |
| [**SetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment)                 | Habilita ou desabilita ajustes periódicos de tempo para o relógio de hora do sistema.                       |
| [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)                       | Converte uma hora do sistema em uma hora do arquivo.                                                                 |
| [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) | Converte uma hora UTC em uma hora local correspondente de um fuso horário especificado.                               |
| [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime) | Converte uma hora local em uma hora UTC.                                                                   |



 

As funções a seguir são usadas com a hora local.



| Função                                                                                           | Descrição                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-enumdynamictimezoneinformation)                           | Enumera entradas de informações de horário de verão dinâmico armazenadas no Registro.                                                             |
| [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime)                                         | Converte uma hora do arquivo UTC em uma hora de arquivo local.                                                                                                  |
| [**GetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation)                             | Recupera o fuso horário atual e as configurações dinâmicas de horário de verão.                                                                      |
| [**GetDynamicTimeZoneInformationEffectiveYears**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformationeffectiveyears) | Recupera um intervalo, expresso em anos, para o qual uma [**INFORMAÇÃO DE FUSO HORÁRIO \_ \_ \_ DINÂMICO**](/windows/win32/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information) tem entradas válidas. |
| [**GetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime)                                                               | Recupera a data e hora locais atuais.                                                                                                      |
| [**Gettimezoneinformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)                                           | Recupera as configurações de fuso horário atuais.                                                                                                       |
| [**GetTimeZoneInformationForYear**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear)                             | Recupera as configurações de fuso horário para o ano e o fuso horário especificados.                                                                          |
| [**RtlLocalTimeToSystemTime**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)                                       | Converte a hora local especificada em hora do sistema.                                                                                               |
| [**SetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation)                             | Define o fuso horário atual e as configurações dinâmicas de horário de verão.                                                                           |
| [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime)                                                               | Define a data e a hora locais atuais.                                                                                                           |
| [**SetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation)                                           | Define as configurações de fuso horário atuais.                                                                                                            |
| [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)                         | Converte uma hora UTC em uma hora local correspondente de um fuso horário especificado.                                                                        |
| [**SystemTimeToTzSpecificLocalTimeEx**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltimeex)                     | Converte uma hora UTC com configurações dinâmicas de horário de verão em um fuso horário local correspondente.                             |
| [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime)                         | Converte uma hora local em uma hora UTC.                                                                                                            |
| [**TzSpecificLocalTimeToSystemTimeEx**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtimeex)                     | Converte uma hora local com configurações dinâmicas de horário de verão em horário UTC.                                                                   |



 

As funções a seguir são usadas com o tempo do arquivo.



| Função                                                   | Descrição                                                                                                     |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**CompareFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime)                 | Compara duas vezes de arquivo.                                                                                        |
| [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) | Converte uma hora do arquivo UTC em uma hora de arquivo local.                                                                  |
| [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)       | Converte uma hora do arquivo no formato de hora do sistema.                                                                     |
| [**Getfiletime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime)                         | Recupera a data e a hora em que o arquivo ou diretório especificado foi criado, acessado pela última vez e modificado pela última vez. |
| [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) | Recupera a data e hora atuais do sistema no formato UTC.                                                       |
| [**LocalFileTimeToFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-localfiletimetofiletime) | Converte uma hora do arquivo local em um tempo de arquivo com base em UTC.                                                         |
| [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime)                         | Define a data e a hora em que o arquivo ou diretório especificado foi criado, acessado pela última vez ou modificado pela última vez.       |
| [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)       | Converte uma hora do sistema em uma hora do arquivo.                                                                          |



 

As funções a seguir são usadas com data e hora do MS-DOS.



| Função                                               | Descrição                                          |
|--------------------------------------------------------|------------------------------------------------------|
| [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) | Converte valores de data e hora do MS-DOS em uma hora do arquivo. |
| [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) | Converte uma hora do arquivo em valores de data e hora do MS-DOS. |



 

As funções a seguir são usadas com Windows tempo.



| Função                                 | Descrição                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) | Recupera informações de tempo do sistema.                                                                  |
| [**Obtercontagemmarcaescala**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount)     | Recupera o número de milissegundos decorridos desde que o sistema foi iniciado, até 49,7 dias. |
| [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) | Recupera o número de milissegundos decorridos desde que o sistema foi iniciado.                  |



 

As funções a seguir são usadas com contadores de desempenho de alta resolução.



| Função                                                              | Descrição                                                             |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**Queryperformancecounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)     | Recupera o valor atual do contador de desempenho de alta resolução. |
| [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) | Recupera a frequência do contador de desempenho de alta resolução.     |



 

As funções a seguir são usadas com o contador de desempenho auxiliar.



| Função                                                                                           | Descrição                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QueryIliaryCounterFrequency**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryauxiliarycounterfrequency)                           | Consulta a frequência do contador auxiliar.                                                                                                                                                                      |
| [**ConvertIliaryCounterToPerformanceCounter**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertauxiliarycountertoperformancecounter) | Converte o valor do contador auxiliar especificado no valor do contador de desempenho correspondente; opcionalmente, fornece o erro de conversão estimado em nanossegundos devido a latências e ao desnência máximo possível. |
| [**ConvertPerformanceCounterToIliaryCounter**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertperformancecountertoauxiliarycounter) | Converte o valor do contador de desempenho especificado no valor do contador auxiliar correspondente; opcionalmente, fornece o erro de conversão estimado em nanossegundos devido a latências e ao desnência máximo possível. |



 

A função a seguir é usada com o tempo de interrupção.



| Função                                                                       | Descrição                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)                               | Obtém a contagem atual de tempo de interrupção.                                                                                                                                                                                                                |
| [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)                 | Obtém a contagem atual de tempo de interrupção, em uma forma mais precisa do [**que QueryInterruptTime.**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)                                                                                                                             |
| [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)               | Obtém a contagem atual de tempo de interrupção sem imparcialidade. A contagem de tempo de interrupção sem imparcialidade não inclui o tempo gasto pelo sistema em sleep ou hibernação.                                                                                                    |
| [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) | Obtém a contagem atual de tempo de interrupção sem imparcialidade, em uma forma mais precisa do [**que QueryUnbiasedInterruptTime.**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) A contagem de tempo de interrupção sem imparcialidade não inclui o tempo gasto pelo sistema em sleep ou hibernação. |



 

 

 
