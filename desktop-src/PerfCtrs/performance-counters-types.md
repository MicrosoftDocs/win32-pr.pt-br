---
description: A PDH define os seguintes tipos de dados.
ms.assetid: 8a2e8683-502a-4893-8b4f-5e2cf464a933
title: Tipos de dados de contadores de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38f9800288494eb82f675265b6e0b801c783668d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755064"
---
# <a name="performance-counters-data-types"></a>Tipos de dados de contadores de desempenho

## <a name="performance-data-helper-pdh-types"></a>Tipos de PDH (auxiliar de dados de desempenho)

Os consumidores que usam as funções [PDH (auxiliar de dados de desempenho)](using-the-pdh-functions-to-consume-counter-data.md) usam os seguintes tipos:

| Tipo de dados | Descrição
|-----------|------------
| **\_HQUERY PDH**   | Identificador para uma consulta. A função [**PdhOpenQuery**](/windows/win32/api/pdh/nf-pdh-pdhopenqueryw) retorna esse identificador. Feche o identificador usando [**PdhCloseQuery**](/windows/win32/api/pdh/nf-pdh-pdhclosequery).
| **\_HCOUNTER PDH** | Identificador para um contador. A função [**PdhAddCounter**](/windows/win32/api/pdh/nf-pdh-pdhaddcounterw) retorna esse identificador. Feche o identificador usando [**PdhRemoveCounter**](/windows/win32/api/pdh/nf-pdh-pdhremovecounter) ou fechando o identificador para a consulta que contém o contador. Não chame **PdhRemoveCounter** em um contador se a consulta correspondente já tiver sido fechada. A PDH mantém a ligação entre contadores e consultas e fechará automaticamente os identificadores de contador quando o identificador de consulta correspondente for fechado.
| **\_HLOG PDH**     | Identificador para um arquivo de log. As funções [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) e [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) retornam esse identificador. Feche o identificador usando [**PdhCloseLog**](/windows/win32/api/pdh/nf-pdh-pdhcloselog).
| **STATUS da PDH \_**   | Valor de status da PDH. Todas as funções de PDH retornam um valor do tipo **PDH \_ status**. Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro. Caso contrário, a função retorna um código de [erro do sistema](/windows/desktop/Debug/system-error-codes) ou um [código de erro PDH](pdh-error-codes.md).
