---
description: O tempo de interrupção é a quantidade de tempo desde que o sistema foi iniciado pela última vez, em intervalos de 100 a nanossegundos.
ms.assetid: 56fe322e-53ea-4186-9b5e-352f69b09109
title: Tempo de interrupção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0da8fa92fc51cdceef6f0052dda7a2cd27d7b21b24d11bd8ec7b1ea4aff18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885506"
---
# <a name="interrupt-time"></a>Tempo de interrupção

O *tempo de interrupção* é a quantidade de tempo desde que o sistema foi iniciado pela última vez, em intervalos de 100 a nanossegundos. A contagem de tempo de interrupção começa em zero quando o sistema é iniciado e incrementado a cada interrupção de relógio pelo comprimento de um tique de relógio. O comprimento exato de um tique de relógio depende do hardware subjacente e pode variar entre os sistemas.

ao contrário do [tempo do sistema](system-time.md), a contagem de tempo de interrupção não está sujeita a ajustes por usuários ou ao serviço de tempo de Windows, o que o torna uma opção melhor para medir durações curtas. Os aplicativos que exigem maior precisão do que a contagem de tempo de interrupção devem usar um [temporizador de alta resolução](../winmsg/about-timers.md). Use a função [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) para recuperar a frequência do temporizador de alta resolução e da função [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) para recuperar o valor do contador.

As funções [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) podem ser usadas para recuperar a contagem de tempo de interrupção. Tempo de interrupção não polarizado significa que apenas a hora em que o sistema está no estado de trabalho é contado – portanto, a contagem de tempo de interrupção não é "polarizada" por tempo que o sistema gasta em suspensão ou hibernação.

**Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP/2000:** a função [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) está disponível a partir do Windows 7 e do Windows Server 2008 R2.

A resolução do temporizador definida pelas funções [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) e [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) afeta a resolução das funções [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) e [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) . No entanto, o aumento da resolução do temporizador não é recomendado porque pode reduzir o desempenho geral do sistema e aumentar o consumo de energia, impedindo o processador de entrar nos Estados de economia de energia. Em vez disso, os aplicativos devem usar um temporizador de alta resolução.

> [!Note]  
> as funções [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) produzem resultados diferentes em compilações ("marcadas") de Windows, porque a contagem de tempo de interrupção e a contagem de tiques são avançadas por aproximadamente 49 dias. Isso ajuda a identificar bugs que podem não ocorrer até que o sistema esteja em execução por um longo tempo. A compilação verificada está disponível para assinantes do MSDN por meio do site do [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) .

 

O exemplo a seguir mostra como recuperar a contagem de tempo de interrupção chamando as funções [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) . Link para a biblioteca OneCore. lib quando você cria um aplicativo de console que chama essas funções.


```C++
#include "stdafx.h"
#include <windows.h>
#include <realtimeapiset.h>

void InterruptTimeTest()
{
    ULONGLONG InterruptTime;
    ULONGLONG PreciseInterruptTime;
    ULONGLONG UnbiasedInterruptTime;
    ULONGLONG PreciseUnbiasedInterruptTime;

        // The interrupt time that QueryInterruptTime reports is based on the 
        // latest tick of the system clock timer. The system clock timer is 
        // the hardware timer that periodically generates interrupts for the 
        // system clock. The uniform period between system clock timer 
        // interrupts is referred to as a system clock tick, and is typically 
        // in the range of 0.5 milliseconds to 15.625 milliseconds, depending 
        // on the hardware platform. The interrupt time value retrieved by 
        // QueryInterruptTime is accurate within a system clock tick.

    QueryInterruptTime(&InterruptTime);
    printf("Interrupt time: %.7f seconds\n", 
            (double)InterruptTime/(double)10000000);

        // Precise interrupt time is more precise than the interrupt time that
        // QueryInterruptTime reports because the functions that report  
        // precise interrupt time read the timer hardware directly.

    QueryInterruptTimePrecise(&PreciseInterruptTime);
    printf("Precise interrupt time: %.7f seconds\n", 
            (double)PreciseInterruptTime/(double)10000000);

        // Unbiased interrupt time means that only time that the system is in 
        // the working state is counted. Therefore, the interrupt-time count 
        // is not biased by time the system spends in sleep or hibernation.

    QueryUnbiasedInterruptTime(&UnbiasedInterruptTime);
    printf("Unbiased interrupt time: %.7f seconds\n", 
            (double)UnbiasedInterruptTime/(double)10000000);

        // QueryUnbiasedInterruptTimePrecise gets an interrupt-time count
        // that is both unbiased and precise, as defined in the comments
        // included earlier in this example.

    QueryUnbiasedInterruptTimePrecise(&PreciseUnbiasedInterruptTime);
    printf("Precise unbiased interrupt time: %.7f seconds\n", 
            (double)PreciseUnbiasedInterruptTime/(double)10000000);

}

int main(void)
{
    void InterruptTimeTime();

    InterruptTimeTest();
    return(0);
}
```



Para recuperar o tempo decorrido que conta para suspensão ou hibernação, use a função [**ObterContagemMarcaEscala**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) ou [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) ou use o contador de desempenho tempo de atividade do sistema. Esse contador de desempenho pode ser recuperado dos dados de desempenho na chave do registro **HKEY \_ performance \_ Data**. O valor retornado é um valor de 8 bytes. Para obter mais informações, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 
