---
description: O serviço de distribuição de mesmo nível da Microsoft dá suporte a funções para os cenários de função de consumidor e funções de Publicador.
ms.assetid: 3f5af891-4f5d-4523-8fe6-47fc6ff13b35
title: Funções da API de distribuição de pares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2532ad8bf5cbb14e18bd16a14bb1be2d79c1791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753946"
---
# <a name="peer-distribution-api-functions"></a>Funções da API de distribuição de pares

O serviço de distribuição de mesmo nível da Microsoft dá suporte a funções para os cenários de função de consumidor e funções de Publicador.

## <a name="the-following-functions-are-common-in-both-client-and-server-scenarios"></a>As funções a seguir são comuns nos cenários "cliente" e "servidor".



| Funções comuns                                                                                       | Descrição                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)                                                             | Cria uma nova instância de **\_ \_ identificador de instância PEERDIST** que deve ser passada para todas as outras APIs de distribuição de mesmo nível. |
| [**PeerDistShutdown**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistshutdown)                                                           | Libera recursos alocados pela chamada para [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup).                         |
| [**PeerDistGetStatus**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatus)                                                         | Retorna o status atual do serviço de distribuição de mesmo nível.                                                        |
| [**PeerDistGetStatusEx**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatusex)                                                     | Retorna o status atual e os recursos do serviço de distribuição de mesmo nível.                                   |
| [**PeerDistGetOverlappedResult**](/windows/desktop/api/peerdist/nf-peerdist-peerdistgetoverlappedresult)                                     | Recupera os resultados de operações assíncronas.                                                               |
| [**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)     | Solicita que o serviço de distribuição de mesmo nível notifique o chamador quando ocorrer uma alteração de status.                      |
| [**PeerDistRegisterForStatusChangeNotificationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotificationex) | Solicita que o serviço de distribuição de mesmo nível notifique o chamador quando ocorrer uma alteração de status.                      |
| [**PeerDistUnregisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistunregisterforstatuschangenotification) | Cancela o registro da notificação de alteração de status para a sessão associada ao identificador fornecido.                 |



 

## <a name="the-following-functions-are-only-supported-in-client-scenarios"></a>As funções a seguir têm suporte apenas em cenários "cliente".



| Funções de cliente                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)                               | Abre e retorna um **\_ \_ identificador de conteúdo PEERDIST** para fazer referência a esse conteúdo.                                                                                                                                                                                                                                                                     |
| [**PeerDistClientCloseContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientclosecontent)                             | Fecha o **\_ \_ identificador de conteúdo PEERDIST**.                                                                                                                                                                                                                                                                                                        |
| [**PeerDistClientGetInformationByHandle**](/windows/desktop/api/peerdist/nf-peerdist-peerdistclientgetinformationbyhandle)         | Recupera informações adicionais do serviço de distribuição de mesmo nível para um identificador de conteúdo específico.                                                                                                                                                                                                                                               |
| [**PeerDistClientAddContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientaddcontentinformation)           | Adiciona informações de conteúdo que, em seguida, são associadas com o **\_ \_ identificador de conteúdo PEERDIST**. Um **\_ \_ identificador de conteúdo PEERDIST** pode ser associado a qualquer informação de conteúdo.                                                                                                                                                                        |
| [**PeerDistClientCompleteContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcompletecontentinformation) | Indica o fim das informações de conteúdo.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientAddData**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientadddata)                                       | Usado para fornecer conteúdo ao cache local. Normalmente, isso é feito quando os dados não podem ser encontrados na rede local, conforme indicado quando o [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread) ou o [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread) é concluído com **\_ tempo limite de erro** ou **\_ \_ \_ dados ausentes no erro PEERDIST**. |
| [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread)                                   | Fornece acesso aleatório ao fluxo de conteúdo.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread)                                 | Fornece acesso sequencial ao fluxo de conteúdo.                                                                                                                                                                                                                                                                                                |
| [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)                             | Remove o conteúdo que foi adicionado anteriormente ao sistema de distribuição de pares local.                                                                                                                                                                                                                                                            |
| [**PeerDistClientCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcancelasyncoperation)             | Cancela a operação assíncrona associada a uma estrutura [sobreposta](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) e o identificador de conteúdo retornado por [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).                                                                                                                     |



 

## <a name="the-following-functions-are-only-supported-in-server-scenarios"></a>As funções a seguir têm suporte apenas em cenários de "servidor".



| Funções de servidor                                                                             | Descrição                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)                           | Cria o **\_ \_ identificador de fluxo PEERDIST** que pode ser usado com [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream) para criar informações de conteúdo para o fluxo de conteúdo. |
| [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream)                 | Adiciona dados ao fluxo referenciado pelo identificador de fluxo PeerDist.                                                                                                                                  |
| [**PeerDistServerPublishCompleteStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishcompletestream)           | Chamado para indicar que todos os dados foram adicionados ao fluxo.                                                                                                                                     |
| [**PeerDistServerCloseStreamHandle**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosestreamhandle)                   | Fecha o identificador de fluxo.                                                                                                                                                                          |
| [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish)                                   | Cancelar a publicação de conteúdo publicado anteriormente no serviço de distribuição de mesmo nível.                                                                                                                         |
| [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)         | Abre um **\_ \_ identificador CONTENTINFO PEERDIST** para conteúdo publicado.                                                                                                                                   |
| [**PeerDistServerOpenContentInformationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformationex)     | Abre um **\_ \_ identificador CONTENTINFO PEERDIST** para conteúdo publicado.                                                                                                                                   |
| [**PeerDistServerRetrieveContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverretrievecontentinformation) | Recupera as informações de conteúdo associadas ao conteúdo publicado.                                                                                                                               |
| [**PeerDistServerCloseContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosecontentinformation)       | **PEERDIST \_ CONTENTINFO o \_ identificador** aberto pelo [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation).                                                                  |
| [**PeerDistServerCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistservercancelasyncoperation)             | Cancela a operação assíncrona associada ao identificador de conteúdo e à estrutura [sobreposta](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .                                             |



 

 

 
