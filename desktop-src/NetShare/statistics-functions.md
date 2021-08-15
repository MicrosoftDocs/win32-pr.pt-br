---
description: o sistema operacional Windows acumula um conjunto de estatísticas operacionais para estações de trabalho e servidores a partir do momento em que o serviço de estação de trabalho ou servidor é iniciado.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Funções de estatísticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2261f0c4f8f8249b401e658759827d6471d3ac47b6eb10df769ad5f37d8ce7af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063586"
---
# <a name="statistics-functions"></a>Funções de estatísticas

o sistema operacional Windows acumula um conjunto de estatísticas operacionais para estações de trabalho e servidores a partir do momento em que o serviço de estação de trabalho ou servidor é iniciado. Para recuperar essas estatísticas, você pode chamar a função de estatísticas de gerenciamento de rede a seguir.



| Função                                     | Descrição                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [**NetStatisticsGet**](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | Recupera estatísticas operacionais para um serviço; dá suporte aos serviços de estação de trabalho e servidor. |



 

A função **NetStatisticsGet** retorna uma estrutura [**stat da estação de \_ trabalho \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) quando as estatísticas da estação de trabalho são solicitadas; a função retorna uma estrutura [**stat \_ Server \_ 0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) quando as estatísticas do servidor são solicitadas.

 

 



