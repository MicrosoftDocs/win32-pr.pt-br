---
description: Se a fonte de dados for um arquivo de log, você poderá especificar um intervalo de tempo para a consulta.
ms.assetid: 8d9c3e96-3645-4875-9b5f-a6c9ddf23ec3
title: Definindo um intervalo de tempo para uma consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55baf642a4a12a86476e2d6feada6b79f1fda72c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766838"
---
# <a name="setting-a-time-range-for-a-query"></a><span data-ttu-id="05a3d-103">Definindo um intervalo de tempo para uma consulta</span><span class="sxs-lookup"><span data-stu-id="05a3d-103">Setting a Time Range for a Query</span></span>

<span data-ttu-id="05a3d-104">Se a fonte de dados for um arquivo de log, você poderá especificar um intervalo de tempo para a consulta.</span><span class="sxs-lookup"><span data-stu-id="05a3d-104">If the data source is a log file, you can specify a time range for the query.</span></span> <span data-ttu-id="05a3d-105">A consulta recupera dados do contador do arquivo de log que foi coletado durante o intervalo de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="05a3d-105">The query retrieves counter data from the log file that was collected during the specified time range.</span></span> <span data-ttu-id="05a3d-106">Para definir o intervalo de tempo, chame a função [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) .</span><span class="sxs-lookup"><span data-stu-id="05a3d-106">To set the time range, call the [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) function.</span></span> <span data-ttu-id="05a3d-107">O **PdhSetQueryTimeRange** não é usado para consultar dados de desempenho de fontes de dados em tempo real.</span><span class="sxs-lookup"><span data-stu-id="05a3d-107">**PdhSetQueryTimeRange** is not used to query performance data from real time data sources.</span></span>

<span data-ttu-id="05a3d-108">Para criar um valor de tempo, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="05a3d-108">To create time value, use the following steps.</span></span>

1.  <span data-ttu-id="05a3d-109">Aloque uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) e inicialize os campos com o valor de hora desejado.</span><span class="sxs-lookup"><span data-stu-id="05a3d-109">Allocate a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure and initialize the fields with the desired time value.</span></span>
2.  <span data-ttu-id="05a3d-110">Chame [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) para converter o valor de tempo da estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) em um tempo de estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="05a3d-110">Call [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) to convert the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure time value to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure time.</span></span>
3.  <span data-ttu-id="05a3d-111">Converta a estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) como uma variável LONGLONG, tendo em mente as convenções de preenchimento de membro da estrutura da sua plataforma e do compilador.</span><span class="sxs-lookup"><span data-stu-id="05a3d-111">Cast the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure as a LONGLONG variable, keeping in mind the structure member padding conventions of your platform and compiler.</span></span>
4.  <span data-ttu-id="05a3d-112">Copie o valor LONGLONG para o campo apropriado na estrutura [**de \_ \_ informações de tempo da PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) .</span><span class="sxs-lookup"><span data-stu-id="05a3d-112">Copy the LONGLONG value to the appropriate field in the [**PDH\_TIME\_INFO**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) structure.</span></span>

<span data-ttu-id="05a3d-113">Para recuperar o intervalo de tempo de todos os dados de desempenho contidos em um arquivo de log, chame a função [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) .</span><span class="sxs-lookup"><span data-stu-id="05a3d-113">To retrieve the time range of all of the performance data contained in a log file, call the [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) function.</span></span>

 

 
