---
description: As funções relacionadas ao tempo retornam o tempo em um dos vários formatos. Você pode usar as funções de tempo para converter entre alguns formatos de tempo para facilitar a comparação e a exibição. A tabela a seguir resume os formatos de hora.
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: Sobre o tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a95571637bb480920f82e90011a72f6eba9e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011138"
---
# <a name="about-time"></a><span data-ttu-id="8b565-105">Sobre o tempo</span><span class="sxs-lookup"><span data-stu-id="8b565-105">About Time</span></span>

<span data-ttu-id="8b565-106">As funções relacionadas ao tempo retornam o tempo em um dos vários formatos.</span><span class="sxs-lookup"><span data-stu-id="8b565-106">Time-related functions return time in one of several formats.</span></span> <span data-ttu-id="8b565-107">Você pode usar as funções de tempo para converter entre alguns formatos de tempo para facilitar a comparação e a exibição.</span><span class="sxs-lookup"><span data-stu-id="8b565-107">You can use the time functions to convert between some time formats for ease of comparison and display.</span></span> <span data-ttu-id="8b565-108">A tabela a seguir resume os formatos de hora.</span><span class="sxs-lookup"><span data-stu-id="8b565-108">The following table summarizes the time formats.</span></span>



| <span data-ttu-id="8b565-109">Formatar</span><span class="sxs-lookup"><span data-stu-id="8b565-109">Format</span></span>          | <span data-ttu-id="8b565-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8b565-110">Type</span></span>                                                                     | <span data-ttu-id="8b565-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b565-111">Description</span></span>                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b565-112">Sistema</span><span class="sxs-lookup"><span data-stu-id="8b565-112">System</span></span>          | [<span data-ttu-id="8b565-113">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="8b565-113">**SYSTEMTIME**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | <span data-ttu-id="8b565-114">Ano, mês, dia, hora, segundo e milissegundos, obtidos do relógio de hardware interno.</span><span class="sxs-lookup"><span data-stu-id="8b565-114">Year, month, day, hour, second, and millisecond, taken from the internal hardware clock.</span></span>                                            |
| <span data-ttu-id="8b565-115">Local</span><span class="sxs-lookup"><span data-stu-id="8b565-115">Local</span></span>           | <span data-ttu-id="8b565-116">[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) ou [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)</span><span class="sxs-lookup"><span data-stu-id="8b565-116">[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) or [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)</span></span> | <span data-ttu-id="8b565-117">Hora do sistema ou horário do arquivo convertido no fuso horário local do sistema.</span><span class="sxs-lookup"><span data-stu-id="8b565-117">A system time or file time converted to the system's local time zone.</span></span>                                                               |
| <span data-ttu-id="8b565-118">Arquivo</span><span class="sxs-lookup"><span data-stu-id="8b565-118">File</span></span>            | [<span data-ttu-id="8b565-119">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="8b565-119">**FILETIME**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | <span data-ttu-id="8b565-120">O número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="8b565-120">The number of 100-nanosecond intervals since January 1, 1601.</span></span>                                                                       |
| <span data-ttu-id="8b565-121">MS-DOS</span><span class="sxs-lookup"><span data-stu-id="8b565-121">MS-DOS</span></span>          | <span data-ttu-id="8b565-122">**WORD**</span><span class="sxs-lookup"><span data-stu-id="8b565-122">**WORD**</span></span>                                                                 | <span data-ttu-id="8b565-123">Uma palavra compactada para a data, outra para a hora.</span><span class="sxs-lookup"><span data-stu-id="8b565-123">A packed word for the date, another for the time.</span></span>                                                                                   |
| <span data-ttu-id="8b565-124">Windows</span><span class="sxs-lookup"><span data-stu-id="8b565-124">Windows</span></span>         | <span data-ttu-id="8b565-125">**DWORD** ou **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="8b565-125">**DWORD** or **ULONGLONG**</span></span>                                               | <span data-ttu-id="8b565-126">O número de milissegundos desde que o sistema foi iniciado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="8b565-126">The number of milliseconds since the system was last started.</span></span> <span data-ttu-id="8b565-127">Quando recuperada como um valor DWORD, o tempo do Windows é ciclos a cada 49,7 dias.</span><span class="sxs-lookup"><span data-stu-id="8b565-127">When retrieved as a DWORD value, Windows time cycles every 49.7 days.</span></span> |
| <span data-ttu-id="8b565-128">Contagem de interrupção</span><span class="sxs-lookup"><span data-stu-id="8b565-128">Interrupt Count</span></span> | <span data-ttu-id="8b565-129">**ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="8b565-129">**ULONGLONG**</span></span>                                                            | <span data-ttu-id="8b565-130">O número de intervalos de 100 a nanossegundos desde que o sistema foi iniciado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="8b565-130">The number of 100-nanosecond intervals since the system was last started.</span></span>                                                           |



 

<span data-ttu-id="8b565-131">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="8b565-131">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="8b565-132">Hora do sistema</span><span class="sxs-lookup"><span data-stu-id="8b565-132">System Time</span></span>](system-time.md)
-   [<span data-ttu-id="8b565-133">Hora local</span><span class="sxs-lookup"><span data-stu-id="8b565-133">Local Time</span></span>](local-time.md)
-   [<span data-ttu-id="8b565-134">Horas de arquivo</span><span class="sxs-lookup"><span data-stu-id="8b565-134">File Times</span></span>](file-times.md)
-   [<span data-ttu-id="8b565-135">Data e hora do MS-DOS</span><span class="sxs-lookup"><span data-stu-id="8b565-135">MS-DOS Date and Time</span></span>](ms-dos-date-and-time.md)
-   [<span data-ttu-id="8b565-136">Tempo do Windows</span><span class="sxs-lookup"><span data-stu-id="8b565-136">Windows Time</span></span>](windows-time.md)
-   [<span data-ttu-id="8b565-137">Tempo de interrupção</span><span class="sxs-lookup"><span data-stu-id="8b565-137">Interrupt Time</span></span>](interrupt-time.md)

 

 
