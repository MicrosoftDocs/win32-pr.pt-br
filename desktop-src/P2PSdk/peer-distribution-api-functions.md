---
description: O serviço distribuição de pares da Microsoft dá suporte a funções para cenários de função de consumidor e de função de editor.
ms.assetid: 3f5af891-4f5d-4523-8fe6-47fc6ff13b35
title: Funções da API de Distribuição de Pares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a594313300c6bf39a2ea4f08efba89d1ed757ba4b8a50eda074466b94433e1e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612317"
---
# <a name="peer-distribution-api-functions"></a>Funções da API de Distribuição de Pares

O serviço distribuição de pares da Microsoft dá suporte a funções para cenários de função de consumidor e de função de editor.

## <a name="the-following-functions-are-common-in-both-client-and-server-scenarios"></a>As funções a seguir são comuns em cenários de "cliente" e "servidor".



| Funções comuns                                                                                       | Descrição                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)                                                             | Cria uma nova **instância DO PEERDIST \_ INSTANCE \_ HANDLE** que deve ser passada para todas as outras APIs de Distribuição Par. |
| [**PeerDistShutdown**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistshutdown)                                                           | Libera os recursos alocados pela chamada para [**PeerDistStartup.**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)                         |
| [**PeerDistGetStatus**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatus)                                                         | Retorna o status atual do serviço distribuição de pares.                                                        |
| [**PeerDistGetStatusEx**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistgetstatusex)                                                     | Retorna o status atual e as funcionalidades do serviço distribuição de pares.                                   |
| [**PeerDistGetOverlappedResult**](/windows/desktop/api/peerdist/nf-peerdist-peerdistgetoverlappedresult)                                     | Recupera os resultados de operações assíncronas.                                                               |
| [**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)     | Solicita que o serviço distribuição de pares notifique o chamador quando ocorrer uma alteração de status.                      |
| [**PeerDistRegisterForStatusChangeNotificationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotificationex) | Solicita que o serviço distribuição de pares notifique o chamador quando ocorrer uma alteração de status.                      |
| [**PeerDistUnregisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistunregisterforstatuschangenotification) | Desregula o registro da notificação de alteração de status para a sessão associada ao handle fornecido.                 |



 

## <a name="the-following-functions-are-only-supported-in-client-scenarios"></a>As funções a seguir só têm suporte em cenários de "cliente".



| Funções de cliente                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)                               | Abre e retorna um **PEERDIST \_ CONTENT \_ HANDLE** para fazer referência a esse conteúdo.                                                                                                                                                                                                                                                                     |
| [**PeerDistClientCloseContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientclosecontent)                             | Fecha o **PEERDIST \_ CONTENT \_ HANDLE**.                                                                                                                                                                                                                                                                                                        |
| [**PeerDistClientGetInformationByHandle**](/windows/desktop/api/peerdist/nf-peerdist-peerdistclientgetinformationbyhandle)         | Recupera informações adicionais do serviço distribuição de pares para um manipular conteúdo específico.                                                                                                                                                                                                                                               |
| [**PeerDistClientAddContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientaddcontentinformation)           | Adiciona informações de conteúdo associadas ao **PEERDIST \_ CONTENT \_ HANDLE.** Um **PEERDIST \_ CONTENT \_ HANDLE** pode ser associado a qualquer informação de conteúdo.                                                                                                                                                                        |
| [**PeerDistClientCompleteContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcompletecontentinformation) | Indica o final das informações de conteúdo.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientAddData**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientadddata)                                       | Usado para fornecer conteúdo ao cache local. Normalmente, isso é feito quando os dados não podem ser encontrados na rede local, conforme indicado quando [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread) ou [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread) são concluídos com **ERROR \_ TIMEOUT** ou **PEERDIST \_ ERROR MISSING \_ \_ DATA**.. |
| [**PeerDistClientBlockRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientblockread)                                   | Fornece acesso aleatório ao fluxo de conteúdo.                                                                                                                                                                                                                                                                                                    |
| [**PeerDistClientStreamRead**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientstreamread)                                 | Fornece acesso sequencial ao fluxo de conteúdo.                                                                                                                                                                                                                                                                                                |
| [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)                             | Remove o conteúdo que foi adicionado anteriormente ao sistema de Distribuição de Pares local.                                                                                                                                                                                                                                                            |
| [**PeerDistClientCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientcancelasyncoperation)             | Cancela a operação assíncrona associada a uma estrutura [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) e ao handle de conteúdo retornado por [**PeerDistClientOpenContent.**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)                                                                                                                     |



 

## <a name="the-following-functions-are-only-supported-in-server-scenarios"></a>As funções a seguir só têm suporte em cenários de "servidor".



| Funções de servidor                                                                             | Descrição                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)                           | Cria o **PEERDIST \_ STREAM \_ HANDLE** que pode ser usado com [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream) para criar informações de conteúdo para o fluxo de conteúdo. |
| [**PeerDistServerPublishAddToStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishaddtostream)                 | Adiciona dados ao fluxo referenciado pelo alça de fluxo PeerDist.                                                                                                                                  |
| [**PeerDistServerPublishCompleteStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishcompletestream)           | Chamado para indicar que todos os dados foram adicionados ao fluxo.                                                                                                                                     |
| [**PeerDistServerCloseStreamHandle**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosestreamhandle)                   | Fecha o alça de fluxo.                                                                                                                                                                          |
| [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish)                                   | Não publica o conteúdo publicado anteriormente no serviço distribuição de pares.                                                                                                                         |
| [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)         | Abre um **PEERDIST \_ CONTENTINFO \_ HANDLE** para conteúdo publicado.                                                                                                                                   |
| [**PeerDistServerOpenContentInformationEx**](/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformationex)     | Abre um **PEERDIST \_ CONTENTINFO \_ HANDLE** para conteúdo publicado.                                                                                                                                   |
| [**PeerDistServerRetrieveContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverretrievecontentinformation) | Recupera as informações de conteúdo associadas ao conteúdo publicado.                                                                                                                               |
| [**PeerDistServerCloseContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverclosecontentinformation)       | **PEERDIST \_ CONTENTINFO \_ HANDLE** aberto [**por PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation).                                                                  |
| [**PeerDistServerCancelAsyncOperation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistservercancelasyncoperation)             | Cancela a operação assíncrona associada ao identificador de conteúdo e à [estrutura OVERLAPPED.](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)                                             |



 

 

 
