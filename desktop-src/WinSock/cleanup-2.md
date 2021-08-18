---
description: O Ws232.dll (e protocolos em camadas) chamará WSPCleanup uma vez para cada \_ invocação de WSPStartup.
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: Limpeza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aefac8f58b7d6eed0380b7aa0e7759ff07e5af2a2762cde7d8e9bab445ca1fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741425"
---
# <a name="cleanup"></a>Limpeza

O Ws232.dll (e protocolos em camadas) chamará \_ [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) uma vez para cada invocação de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Em cada invocação, **WSPCleanup** deve decrementar um contador de referência por processo e, quando o contador atinge zero, o provedor de serviços deve se preparar para ser descarregado da memória. A primeira ordem dos negócios é concluir a transmissão de dados nãoents em soquetes configurados para um fechamento normalmente. Depois disso, todos os recursos mantidos pelo provedor devem ser liberados. O provedor de serviços deve ser deixado em um estado em que possa ser reinicializado imediatamente por uma chamada para **WSPStartup**.

 

 
