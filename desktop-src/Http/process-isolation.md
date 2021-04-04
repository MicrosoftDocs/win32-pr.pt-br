---
title: Isolamento do processo
description: A API do servidor HTTP versão 2,0 fornece a capacidade de criar um serviço mais seguro e confiável isolando os processos de trabalho que estão atendendo às solicitações na fila de solicitações.
ms.assetid: 893741b7-025c-4642-aff4-a5d69244763f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efcfccc78bbef435aa0c74e918003383135bc4ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "103837552"
---
# <a name="process-isolation"></a>Isolamento do processo

A API do servidor HTTP versão 2,0 fornece a capacidade de criar um serviço mais seguro e confiável isolando os processos de trabalho que estão atendendo às solicitações na fila de solicitações. A fila de solicitações é criada e administrada por um processo de controlador ou criador que controla estritamente o acesso a ela. O processo do controlador inicia um ou mais processos de trabalho separados que executam e/s na fila de solicitações. O processo do controlador é executado com privilégio administrativo e configura a fila de solicitações, enquanto o trabalho de menor privilégio processa o acesso e as solicitações de serviço da fila de solicitações. Essa arquitetura dá suporte à política de aplicativos executados sob "privilégios mínimos" e reduz a possibilidade de vulnerabilidades de segurança introduzidas por código de terceiros que podem estar em execução em processos de trabalho.

O acesso à fila de solicitações é concedido quando o processo do controlador cria a fila de solicitações com um nome e uma ACL (lista de controle de acesso). Os aplicativos Web incluídos na ACL podem abrir uma fila de solicitações existente por nome. O processo criador também pode ser um processo de trabalho na fila de solicitações. Para obter mais informações, consulte o tópico [fila de solicitações nomeadas](named-request-queue.md) . O diagrama a seguir mostra a arquitetura de um aplicativo HTTP típico em execução com o modelo de processo de trabalho:

![Diagrama que mostra a arquitetura de um aplicativo H T P usando o modelo de processo de trabalho.](images/processisolation.png)

Os processos de trabalho individuais dentro do aplicativo são isolados de outros processos de trabalho, e a integridade de cada um dos processos de trabalho pode ser monitorada pelo processo do controlador. O processo do controlador é isolado dos processos de trabalho. Os componentes da arquitetura HTTP são descritos abaixo:

-   Processo do criador ou do controlador: o processo do controlador pode ser executado com ou sem privilégios administrativos para monitorar a integridade e configurar o serviço. O processo do controlador normalmente cria uma única sessão de servidor para o serviço e define os grupos de URLs na sessão do servidor. O grupo de URLs ao qual uma URL específica está associada determina quais serviços de fila de solicitação o namespace denotado pela URL específica. O processo do controlador também cria a fila de solicitações e inicia os processos de trabalho que podem acessar a fila de solicitações.
-   Processo de trabalho: os processos de trabalho, iniciados pelo processo do controlador, executam e/s na fila de solicitações associada às URLs que eles acessam. O aplicativo Web recebe acesso à fila de solicitações pelo processo do controlador na ACL quando a fila de solicitações é criada. A menos que o aplicativo Web também seja o processo criador, ele não gerencia o serviço nem configura a fila de solicitações. O processo do controlador comunica o nome da fila de solicitações ao processo de trabalho e o processo de trabalho abre a fila de solicitações por nome. Os processos de trabalho podem carregar aplicativos Web de terceiros sem introduzir vulnerabilidades de segurança em outras partes do aplicativo.
-   Fila de solicitações: a fila de solicitações é criada e configurada pelo processo do controlador. O controlador especifica os processos que têm permissão de acesso à fila de solicitações na ACL quando a fila de solicitações é criada.
-   Sessão de servidor: o processo do controlador normalmente cria e configura uma sessão de servidor único para o aplicativo. A sessão de servidor mantém as propriedades de configuração para todo o aplicativo. Os grupos de URLs são criados na sessão do servidor pelo processo do controlador.
-   Grupo de URLs: o processo do controlador cria os grupos de URLs na sessão do servidor e configura o grupo de URLs independentemente da sessão do servidor. As URLs são adicionadas ao grupo pelo processo do controlador. As solicitações são roteadas para a fila de solicitações à qual o grupo de URLs está associado.

 

 




