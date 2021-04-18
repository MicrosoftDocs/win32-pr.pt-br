---
description: O sistema operacional Windows acumula um conjunto de estatísticas operacionais para estações de trabalho e servidores a partir do momento em que o serviço de estação de trabalho ou servidor é iniciado.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Funções de estatísticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce62e12f3c4894ba86ff5e5aaaa38801d272195c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810293"
---
# <a name="statistics-functions"></a>Funções de estatísticas

O sistema operacional Windows acumula um conjunto de estatísticas operacionais para estações de trabalho e servidores a partir do momento em que o serviço de estação de trabalho ou servidor é iniciado. Para recuperar essas estatísticas, você pode chamar a função de estatísticas de gerenciamento de rede a seguir.



| Função                                     | Descrição                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [**NetStatisticsGet**](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | Recupera estatísticas operacionais para um serviço; dá suporte aos serviços de estação de trabalho e servidor. |



 

A função **NetStatisticsGet** retorna uma estrutura [**stat da estação de \_ trabalho \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) quando as estatísticas da estação de trabalho são solicitadas; a função retorna uma estrutura [**stat \_ Server \_ 0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) quando as estatísticas do servidor são solicitadas.

 

 



