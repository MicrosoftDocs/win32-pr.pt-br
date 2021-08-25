---
description: O PDH define os seguintes tipos de dados.
ms.assetid: 8a2e8683-502a-4893-8b4f-5e2cf464a933
title: Tipos de dados de contadores de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23208978cfc3c0a67c7547598f26e506a5571a54d0d5ddfc93b7ecff38f9c559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674736"
---
# <a name="performance-counters-data-types"></a>Tipos de dados de contadores de desempenho

## <a name="performance-data-helper-pdh-types"></a>Tipos de PDH (Auxiliar de Dados de Desempenho)

Os consumidores que usam [as funções de PDH (Auxiliar](using-the-pdh-functions-to-consume-counter-data.md) de Dados de Desempenho) usam os seguintes tipos:

| Tipo de dados | Descrição
|-----------|------------
| **PDH \_ HQUERY**   | Lidar com uma consulta. A [**função PdhOpenQuery**](/windows/win32/api/pdh/nf-pdh-pdhopenqueryw) retorna esse handle. Feche o alçamento usando [**PdhCloseQuery.**](/windows/win32/api/pdh/nf-pdh-pdhclosequery)
| **PDH \_ HCOUNTER** | Lidar com um contador. A [**função PdhAddCounter**](/windows/win32/api/pdh/nf-pdh-pdhaddcounterw) retorna esse handle. Feche o handle usando [**PdhRemoveCounter**](/windows/win32/api/pdh/nf-pdh-pdhremovecounter) ou fechando o handle para a consulta que contém o contador. Não chame **PdhRemoveCounter em** um contador se a consulta correspondente já tiver sido fechada. O PDH mantém a vinculação entre contadores e consultas e fechará automaticamente os alças do contador quando o alça de consulta correspondente for fechado.
| **PDH \_ HLOG**     | Manipular para um arquivo de log. As [**funções PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) e [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) retornam esse handle. Feche o alçamento usando [**PdhCloseLog.**](/windows/win32/api/pdh/nf-pdh-pdhcloselog)
| **STATUS \_ DO PDH**   | Valor de status pdh. Todas as funções PDH retornam um valor do tipo **PDH \_ STATUS**. Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS. Caso contrário, a função retornará [um código de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de erro [PDH](pdh-error-codes.md).
