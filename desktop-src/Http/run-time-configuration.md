---
title: Configuração de Run-Time
description: A API HTTP permite que os aplicativos executem a configuração dinâmica em tempo de execução.
ms.assetid: 5118b48b-b44c-4cf5-9754-ce23c5a0b87e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b240438ada7fce186f334df3175b8ecc5b557626c5f1f085cdf82965fb32365
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393748"
---
# <a name="run-time-configuration"></a>Configuração de Run-Time

A API HTTP permite que os aplicativos executem a configuração dinâmica em tempo de execução. A configuração de tempo de execução não é persistente, requer apenas privilégios de nível baixo e afeta somente o aplicativo. A configuração de tempo de execução pode incluir qualquer uma das seguintes atividades:

-   Inicializar o serviço HTTP e criar uma sessão de servidor. Um aplicativo Inicializa o serviço HTTP chamando a função [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) . O servidor deve ser inicializado antes que qualquer outra função de servidor possa ser chamada. Em seguida, o aplicativo cria uma sessão de servidor chamando a função [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) . A sessão de servidor é um contêiner para propriedades que se aplicam a todos os grupos de URLs que pertencem a essa sessão de servidor. Normalmente, cada allication tem apenas uma sessão de servidor. Para obter informações sobre como definir propriedades de sessão de servidor e sobre seu escopo, consulte [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).
-   Registrando para URLs. Depois que a sessão do servidor é criada, um aplicativo pode se registrar para URLs criando um ou mais grupos de URLs. Um grupo de URLs é um grupo de URLs para os quais as mesmas propriedades serão aplicadas. Um aplicativo cria um grupo de URLs chamando a função [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) e, em seguida, adiciona as URLs desejadas chamando a função [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) . Depois que um aplicativo for registrado para URLs criando um grupo de URLs e tiver associado o grupo de URLs a uma fila de solicitações (consulte [criando e ligando a uma fila de solicitações](creating-and-binding-to-a-request-queue.md)), todas as solicitações provenientes dessas URLs serão roteadas para a fila de solicitações associada a esse aplicativo. Para obter mais informações sobre as propriedades do grupo de URLs de configurações, consulte [ **HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
-   Habilitando recursos definindo as propriedades do servidor HTTP, como [autenticação](authentication-in-http-version-2-0.md), [registro em log](server-side-logging-in-http-version-2-0.md), configurações de QoS, tempos limite, estado habilitado e informações de associação. Para obter informações sobre como definir propriedades, consulte [**\_ \_ Propriedade do servidor http**](/windows/desktop/api/Http/ne-http-http_server_property).

 

 




