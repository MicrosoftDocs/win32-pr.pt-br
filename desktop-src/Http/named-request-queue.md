---
title: Fila de solicitações nomeadas
description: Fila de solicitações nomeadas
ms.assetid: d0686a9b-fc3d-4b69-b083-d04b35ce5b50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4aca045f84fe9f9e4b57365ba8831456f2dc1ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292711"
---
# <a name="named-request-queue"></a>Fila de solicitações nomeadas

A API do servidor HTTP versão 2,0 chamada solicitação de fila de solicitações permite que vários aplicativos, operando sob processos e contas de usuário separados, acessem a fila de solicitações. A fila de solicitações é aberta por nome e protegida usando ACLs (listas de controle de acesso) para garantir que os aplicativos não possam acessar os dados de outros. Um único processo cria a fila de solicitações e concede permissão a outros processos para usar a fila de solicitações. Assim, outros processos no computador acessam a fila de solicitações com o privilégio mínimo necessário para solicitações de serviço. Possíveis danos ao serviço HTTP, devido a vulnerabilidades no código de terceiros, são minimizados quando os aplicativos estão sendo executados sob privilégios mínimos.

A fila de solicitações nomeada é criada com a função [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) . Quando a fila de solicitações é criada, o aplicativo especifica a ACL no parâmetro *pSecurityAttribute* . A ACL, que só pode ser definida quando a fila de solicitações é criada, permite que os processos de trabalho Abram a fila de solicitações, recebam solicitações e enviem respostas. Por padrão, os processos não têm permissão para abrir uma fila de solicitações, a menos que tenham recebido permissão na ACL. Os aplicativos não exigem privilégios administrativos para criar a fila de solicitações.

A fila de solicitações deve ser criada com um nome especificado no parâmetro *pname* de [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) para que outros processos Abram a fila de solicitações. Se *pname* for **NULL**, uma fila de solicitação sem nome será criada e nenhum outro processo poderá abri-la.

## <a name="creator-and-controller-processes"></a>Processos do criador e do controlador

Quando a fila de solicitações é criada, o aplicativo pode abri-lo como um processo de controlador ou um processo de criador. Os processos de controlador e criador atuam como administradores para a fila de solicitações, mas o controlador não executa operações de e/s nele. O aplicativo indica que se trata de um processo de controlador quando a fila de solicitações é criada especificando o **controlador de \_ sinalizador de fila de solicitação de criação \_ \_ \_ \_ de http** no parâmetro *flags* de [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue). Se o sinalizador do **controlador do sinalizador de \_ fila de \_ solicitação \_ \_ \_ http Create** não estiver definido, o aplicativo será um processo criador.

A lista a seguir contém tarefas executadas pelo processo do controlador e o processo Criador:

-   Crie a fila de solicitações e especifique o nome.
-   Configure a fila de solicitações usando a função [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) .
-   Consulte os parâmetros de configuração da fila de solicitação usando a função [**HttpQueryRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) .
-   Crie grupos de URLs e associe-os a uma fila de solicitações.
-   Defina a ACL especificando os processos de trabalho que têm permissão para receber e/s na fila de solicitações.
-   Chame [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) para atrasar a instanciação dos processos de trabalho até que a primeira solicitação chegue à fila de solicitações.

Além dessas tarefas, o processo criador também pode executar operações de e/s na fila de solicitações.

## <a name="worker-processes"></a>Processos de Trabalho

Um processo de trabalho pode abrir uma fila de solicitações existente somente se tiver recebido acesso a ela na ACL. Os processos de trabalho operando sob privilégios mínimos podem abrir uma fila de solicitação e executar e/s nela. Os aplicativos abrem uma fila de solicitações existente chamando [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) com o **sinalizador de fila de solicitação HTTP \_ Create \_ \_ \_ \_ aberto \_ existente** no parâmetro *flags* e o nome da fila de solicitações no parâmetro *pname* .

O processo de trabalho executa as seguintes funções:

-   Receber solicitações e enviar respostas na fila de solicitações.
-   Abra uma fila de solicitações existente por nome. O identificador para a fila de solicitações retornado ao processo de trabalho não pode ser usado para configurar a fila de solicitações.
-   Consulte os parâmetros de configuração da fila de solicitações.

O diagrama a seguir mostra o modelo de processo de trabalho para filas de solicitações. A fila de solicitações pode ter vários processos de trabalho que processam e/s e um processo de criador que configura a fila de solicitações.

![modelo de processo de trabalho para filas de solicitações](images/namedrequestqueue.png)

 

 




