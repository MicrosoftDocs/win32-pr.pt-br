---
title: Desligamento e limpeza
description: Para que um aplicativo seja encerrado normalmente, ele deve executar as seguintes operações de limpeza.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf1c59534b73fee21489439c7818c286874185d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005623"
---
# <a name="shutdown-and-cleanup"></a>Desligamento e limpeza

Para que um aplicativo seja encerrado normalmente, ele deve executar as seguintes operações de limpeza:

-   Remova todas as URLs registradas do grupo de URLs chamando a função [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) para cancelar o registro de URLs registradas anteriormente na chamada para [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).
-   Feche o grupo de URLs chamando a função [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) . Todos os grupos de URLs criados em uma sessão de servidor devem ser fechados antes de fechar a sessão do servidor.
-   Feche a sessão de servidor chamando [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).
-   Feche o identificador para a fila de solicitações chamando [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).
-   Encerre os recursos criados pela API do servidor HTTP chamando a função [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) com as configurações de sinalizador correspondentes para cada chamada que o aplicativo fez originalmente para o [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize). Cada uma dessas chamadas encerra todos os recursos criados na chamada para [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).

 

 




