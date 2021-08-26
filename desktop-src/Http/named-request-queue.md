---
title: Fila de Solicitação Nomeada
description: Fila de Solicitação Nomeada
ms.assetid: d0686a9b-fc3d-4b69-b083-d04b35ce5b50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2174044f23f30470f3285e3c8fcf9bd2dbd474b10c306df7f2fbb215b992eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078336"
---
# <a name="named-request-queue"></a>Fila de Solicitação Nomeada

O recurso de fila de solicitação nomeada da API do Servidor HTTP versão 2.0 permite que vários aplicativos, operando em processos separados e contas de usuário, acessem a fila de solicitações. A fila de solicitações é aberta por nome e protegida usando ACLs (Listas de Controle de Acesso) para garantir que os aplicativos não sejam capazes de acessar os dados uns dos outros. Um único processo cria a fila de solicitações e concede permissão a outros processos para usar a fila de solicitação. Portanto, outros processos no computador acessam a fila de solicitações com o privilégio mínimo necessário para as solicitações de serviço. Possíveis danos ao serviço HTTP, devido a vulnerabilidades no código de terceiros, são minimizados quando os aplicativos estão em execução com privilégios mínimos.

A fila de solicitação nomeada é criada com a [**função HttpCreateRequestQueue.**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) Quando a fila de solicitação é criada, o aplicativo especifica a ACL no *parâmetro pSecurityAttribute.* A ACL, que só pode ser definida quando a fila de solicitação é criada, permite que os processos de trabalho abram a fila de solicitações, recebam solicitações e enviem respostas. Por padrão, os processos não têm permissão para abrir uma fila de solicitações, a menos que tenham sido concedidas permissões na ACL. Os aplicativos não exigem privilégios administrativos para criar a fila de solicitações.

A fila de solicitação deve ser criada com um nome especificado no parâmetro *pName* de [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) para outros processos abrirem a fila de solicitação. Se *pName* for **NULL,** uma fila de solicitações sem nome será criada e nenhum outro processo poderá abri-la.

## <a name="creator-and-controller-processes"></a>Processos de criador e controlador

Quando a fila de solicitação é criada, o aplicativo pode abri-la como um processo de controlador ou um processo de criador. Os processos do controlador e do criador atuam como administradores para a fila de solicitações, mas o controlador não executa operações de E/S nele. O aplicativo indica que é um processo de controlador quando a fila de solicitação é criada especificando **HTTP CREATE REQUEST QUEUE FLAG \_ \_ \_ \_ \_ CONTROLLER** no parâmetro *Flags* de [**HttpCreateRequestQueue.**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) Se o sinalizador CONTROLADOR DE SINALIZADOR **\_ DE FILA DE \_ \_ \_ SOLICITAÇÃO \_ HTTP CREATE** não estiver definido, o aplicativo será um processo de criador.

A lista a seguir contém tarefas executadas pelo processo do controlador e pelo processo do criador:

-   Crie a fila de solicitações e especifique o nome.
-   Configure a fila de solicitações usando [**a função HttpSetRequestQueueProperty.**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty)
-   Consulte os parâmetros de configuração da fila de solicitação usando a [**função HttpQueryRequestQueueProperty.**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty)
-   Crie Grupos de URL e associe-os a uma fila de solicitações.
-   Definir a ACL especificando os processos de trabalho que têm permissão para receber E/S na fila de solicitação.
-   Chame [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) para atrasar a instalização de processos de trabalho até que a primeira solicitação chegue na fila de solicitação.

Além dessas tarefas, o processo do criador também pode executar operações de E/S na fila de solicitações.

## <a name="worker-processes"></a>Processos de Trabalho

Um processo de trabalho poderá abrir uma fila de solicitações existente somente se tiver sido concedido acesso a ela na ACL. Processos de trabalho que operam com privilégios mínimos podem abrir uma fila de solicitações e executar E/S nele. Os aplicativos abrem uma fila de solicitação existente chamando [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) com o SINALIZADOR DE FILA DE SOLICITAÇÃO HTTP CREATE OPEN **\_ \_ \_ \_ \_ \_ EXISTING** no parâmetro *Flags* e o nome da fila de solicitação no parâmetro *pName.*

O processo de trabalho executa as seguintes funções:

-   Receba solicitações e envie respostas na fila de solicitações.
-   Abra uma fila de solicitações existente por nome. O handle para a fila de solicitação retornada ao processo de trabalho não pode ser usado para configurar a fila de solicitação.
-   Consulte os parâmetros de configuração da fila de solicitação.

O diagrama a seguir mostra o modelo de processo de trabalho para filas de solicitação. A fila de solicitação pode ter vários processos de trabalho que processam E/S e um processo de criador que configura a fila de solicitações.

![modelo de processo de trabalho para filas de solicitação](images/namedrequestqueue.png)

 

 




