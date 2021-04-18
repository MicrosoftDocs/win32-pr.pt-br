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
# <a name="setting-a-time-range-for-a-query"></a>Definindo um intervalo de tempo para uma consulta

Se a fonte de dados for um arquivo de log, você poderá especificar um intervalo de tempo para a consulta. A consulta recupera dados do contador do arquivo de log que foi coletado durante o intervalo de tempo especificado. Para definir o intervalo de tempo, chame a função [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) . O **PdhSetQueryTimeRange** não é usado para consultar dados de desempenho de fontes de dados em tempo real.

Para criar um valor de tempo, use as etapas a seguir.

1.  Aloque uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) e inicialize os campos com o valor de hora desejado.
2.  Chame [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) para converter o valor de tempo da estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) em um tempo de estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .
3.  Converta a estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) como uma variável LONGLONG, tendo em mente as convenções de preenchimento de membro da estrutura da sua plataforma e do compilador.
4.  Copie o valor LONGLONG para o campo apropriado na estrutura [**de \_ \_ informações de tempo da PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) .

Para recuperar o intervalo de tempo de todos os dados de desempenho contidos em um arquivo de log, chame a função [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) .

 

 
