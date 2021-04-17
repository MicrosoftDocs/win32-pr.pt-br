---
description: O tempo de interrupção é a quantidade de tempo desde que o sistema foi iniciado pela última vez, em intervalos de 100 a nanossegundos.
ms.assetid: 56fe322e-53ea-4186-9b5e-352f69b09109
title: Tempo de interrupção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6018d97ab0eecd1182c02b734357ca13fbe12632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756126"
---
# <a name="interrupt-time"></a><span data-ttu-id="a366c-103">Tempo de interrupção</span><span class="sxs-lookup"><span data-stu-id="a366c-103">Interrupt Time</span></span>

<span data-ttu-id="a366c-104">O *tempo de interrupção* é a quantidade de tempo desde que o sistema foi iniciado pela última vez, em intervalos de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="a366c-104">*Interrupt time* is the amount of time since the system was last started, in 100-nanosecond intervals.</span></span> <span data-ttu-id="a366c-105">A contagem de tempo de interrupção começa em zero quando o sistema é iniciado e incrementado a cada interrupção de relógio pelo comprimento de um tique de relógio.</span><span class="sxs-lookup"><span data-stu-id="a366c-105">The interrupt-time count begins at zero when the system starts and is incremented at each clock interrupt by the length of a clock tick.</span></span> <span data-ttu-id="a366c-106">O comprimento exato de um tique de relógio depende do hardware subjacente e pode variar entre os sistemas.</span><span class="sxs-lookup"><span data-stu-id="a366c-106">The exact length of a clock tick depends on underlying hardware and can vary between systems.</span></span>

<span data-ttu-id="a366c-107">Ao contrário do [tempo do sistema](system-time.md), a contagem de tempo de interrupção não está sujeita a ajustes por usuários ou serviço de tempo do Windows, o que o torna uma opção melhor para medir durações curtas.</span><span class="sxs-lookup"><span data-stu-id="a366c-107">Unlike [system time](system-time.md), the interrupt-time count is not subject to adjustments by users or the Windows time service, making it a better choice for measuring short durations.</span></span> <span data-ttu-id="a366c-108">Os aplicativos que exigem maior precisão do que a contagem de tempo de interrupção devem usar um [temporizador de alta resolução](../winmsg/about-timers.md).</span><span class="sxs-lookup"><span data-stu-id="a366c-108">Applications that require greater precision than the interrupt-time count should use a [high-resolution timer](../winmsg/about-timers.md).</span></span> <span data-ttu-id="a366c-109">Use a função [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) para recuperar a frequência do temporizador de alta resolução e da função [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) para recuperar o valor do contador.</span><span class="sxs-lookup"><span data-stu-id="a366c-109">Use the [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) function to retrieve the frequency of the high-resolution timer and the [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) function to retrieve the counter's value.</span></span>

<span data-ttu-id="a366c-110">As funções [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) podem ser usadas para recuperar a contagem de tempo de interrupção.</span><span class="sxs-lookup"><span data-stu-id="a366c-110">The [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions can be used to retrieve the interrupt-time count.</span></span> <span data-ttu-id="a366c-111">Tempo de interrupção não polarizado significa que apenas a hora em que o sistema está no estado de trabalho é contado – portanto, a contagem de tempo de interrupção não é "polarizada" por tempo que o sistema gasta em suspensão ou hibernação.</span><span class="sxs-lookup"><span data-stu-id="a366c-111">Unbiased interrupt-time means that only time that the system is in the working state is counted—therefore, the interrupt-time count is not "biased" by time the system spends in sleep or hibernation.</span></span>

<span data-ttu-id="a366c-112">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP/2000:** A função [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) está disponível a partir do Windows 7 e do windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a366c-112">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:** The [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) function is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="a366c-113">A resolução do temporizador definida pelas funções [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) e [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) afeta a resolução das funções [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) e [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) .</span><span class="sxs-lookup"><span data-stu-id="a366c-113">The timer resolution set by the [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) functions affects the resolution of the [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) and [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) functions.</span></span> <span data-ttu-id="a366c-114">No entanto, o aumento da resolução do temporizador não é recomendado porque pode reduzir o desempenho geral do sistema e aumentar o consumo de energia, impedindo o processador de entrar nos Estados de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="a366c-114">However, increasing the timer resolution is not recommended because it can reduce overall system performance and increase power consumption by preventing the processor from entering power-saving states.</span></span> <span data-ttu-id="a366c-115">Em vez disso, os aplicativos devem usar um temporizador de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="a366c-115">Instead, applications should use a high-resolution timer.</span></span>

> [!Note]  
> <span data-ttu-id="a366c-116">As funções [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) produzem resultados diferentes nas compilações de depuração ("marcadas") do Windows, pois a contagem de tempo de interrupção e a contagem de tiques são avançadas por aproximadamente 49 dias.</span><span class="sxs-lookup"><span data-stu-id="a366c-116">The [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days.</span></span> <span data-ttu-id="a366c-117">Isso ajuda a identificar bugs que podem não ocorrer até que o sistema esteja em execução por um longo tempo.</span><span class="sxs-lookup"><span data-stu-id="a366c-117">This helps to identify bugs that might not occur until the system has been running for a long time.</span></span> <span data-ttu-id="a366c-118">A compilação verificada está disponível para assinantes do MSDN por meio do site do [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a366c-118">The checked build is available to MSDN subscribers through the [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) Web site.</span></span>

 

<span data-ttu-id="a366c-119">O exemplo a seguir mostra como recuperar a contagem de tempo de interrupção chamando as funções [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)e [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) .</span><span class="sxs-lookup"><span data-stu-id="a366c-119">The following example shows how to retrieve the interrupt-time count by calling the [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions.</span></span> <span data-ttu-id="a366c-120">Link para a biblioteca OneCore. lib quando você cria um aplicativo de console que chama essas funções.</span><span class="sxs-lookup"><span data-stu-id="a366c-120">Link to the OneCore.lib library when you build a console application that calls these functions.</span></span>


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



<span data-ttu-id="a366c-121">Para recuperar o tempo decorrido que conta para suspensão ou hibernação, use a função [**ObterContagemMarcaEscala**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) ou [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) ou use o contador de desempenho tempo de atividade do sistema.</span><span class="sxs-lookup"><span data-stu-id="a366c-121">To retrieve elapsed time that accounts for sleep or hibernation, use the [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) or [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) function, or use the System Up Time performance counter.</span></span> <span data-ttu-id="a366c-122">Esse contador de desempenho pode ser recuperado dos dados de desempenho na chave do registro **HKEY \_ performance \_ Data**.</span><span class="sxs-lookup"><span data-stu-id="a366c-122">This performance counter can be retrieved from the performance data in the registry key **HKEY\_PERFORMANCE\_DATA**.</span></span> <span data-ttu-id="a366c-123">O valor retornado é um valor de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="a366c-123">The value returned is an 8-byte value.</span></span> <span data-ttu-id="a366c-124">Para obter mais informações, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="a366c-124">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a366c-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a366c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a366c-126">**QueryInterruptTime**</span><span class="sxs-lookup"><span data-stu-id="a366c-126">**QueryInterruptTime**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[<span data-ttu-id="a366c-127">**QueryInterruptTimePrecise**</span><span class="sxs-lookup"><span data-stu-id="a366c-127">**QueryInterruptTimePrecise**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[<span data-ttu-id="a366c-128">**QueryUnbiasedInterruptTime**</span><span class="sxs-lookup"><span data-stu-id="a366c-128">**QueryUnbiasedInterruptTime**</span></span>](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[<span data-ttu-id="a366c-129">**QueryUnbiasedInterruptTimePrecise**</span><span class="sxs-lookup"><span data-stu-id="a366c-129">**QueryUnbiasedInterruptTimePrecise**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[<span data-ttu-id="a366c-130">**timeBeginPeriod**</span><span class="sxs-lookup"><span data-stu-id="a366c-130">**timeBeginPeriod**</span></span>](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[<span data-ttu-id="a366c-131">**timeEndPeriod**</span><span class="sxs-lookup"><span data-stu-id="a366c-131">**timeEndPeriod**</span></span>](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 
