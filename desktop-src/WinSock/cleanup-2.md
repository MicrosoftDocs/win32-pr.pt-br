---
description: O \_32.dll Ws2 (e protocolos em camadas) chamará WSPCleanup uma vez para cada invocação de WSPStartup.
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: Limpeza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc294183f964d00ae9ebb1d74b90b346c2ce8fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813470"
---
# <a name="cleanup"></a>Limpeza

O \_32.dll Ws2 (e protocolos em camadas) chamará [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) uma vez para cada invocação de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Em cada invocação, **WSPCleanup** deve decrementar um contador de referência por processo e, quando o contador chega a zero, o provedor de serviços deve se preparar para ser descarregado da memória. A primeira ordem de negócios é concluir a transmissão de todos os dados não enviados em soquetes configurados para um fechamento normal. Depois disso, qualquer um e todos os recursos mantidos pelo provedor serão liberados. O provedor de serviços deve ser deixado em um estado em que possa ser reinicializado imediatamente por uma chamada para **WSPStartup**.

 

 
