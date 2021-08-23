---
title: Desligamento e limpeza
description: Para que um aplicativo seja encerrado normalmente, ele deve executar as seguintes operações de limpeza.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a551ad57ddbf63c6ff598814794bc5837da646e98169d8250e543575abd013a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950686"
---
# <a name="shutdown-and-cleanup"></a>Desligamento e limpeza

Para que um aplicativo seja encerrado normalmente, ele deve executar as seguintes operações de limpeza:

-   Remova todas as URLs registradas do grupo de URL chamando a função [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) para desregister URLs registradas anteriormente na chamada para [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).
-   Feche o Grupo de URL chamando a [**função HttpCloseUrlGroup.**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) Todos os grupos de URL criados em uma sessão de servidor devem ser fechados antes de fechar a sessão do servidor.
-   Feche a sessão do servidor chamando [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).
-   Feche o alçamento para a fila de solicitações chamando [**HttpCloseRequestQueue.**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue)
-   Encente os recursos criados pela API do Servidor HTTP chamando a função [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) com as configurações de sinalizador correspondentes para cada chamada que o aplicativo originalmente fez para [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize). Cada uma dessas chamadas encerra todos os recursos criados na chamada para [**HttpInitialize.**](/windows/desktop/api/Http/nf-http-httpinitialize)

 

 




