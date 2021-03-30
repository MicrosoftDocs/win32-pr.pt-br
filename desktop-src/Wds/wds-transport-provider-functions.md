---
title: Funções do provedor de transporte do WDS
description: Os provedores de conteúdo definidos pelo usuário podem expor as seguintes funções de retorno de chamada para o servidor de multicast.
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e67747d8ef5738a4bf3bee8ff2ffb3b35cf43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637020"
---
# <a name="wds-transport-provider-functions"></a>Funções do provedor de transporte do WDS

Os provedores de conteúdo definidos pelo usuário podem expor as seguintes funções de retorno de chamada para o servidor de multicast.



| Função                                                                               | Descrição                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [*WdsTransportProviderCloseContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | Fecha um fluxo de conteúdo especificado por um identificador.                                                                          |
| [*WdsTransportProviderCloseInstance*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | Fecha uma instância de um provedor de conteúdo especificado por um identificador.                                                         |
| [*WdsTransportProviderCompareContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | Compara um nome de conteúdo e uma instância especificados para um fluxo de conteúdo aberto para determinar se eles são os mesmos.             |
| [*WdsTransportProviderCreateInstance*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | Abre uma nova instância de um provedor de conteúdo.                                                                             |
| [*WdsTransportProviderDumpState*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | Instrui o provedor de transporte a imprimir um resumo de seu estado e qualquer outra informação relevante para o log de rastreamento. |
| [*WdsTransportProviderGetContentMetadata*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | Recupera metadados para um fluxo de conteúdo aberto.                                                                          |
| [*WdsTransportProviderGetContentSize*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | Recupera o tamanho de um fluxo de conteúdo aberto.                                                                           |
| [*WdsTransportProviderInitialize*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | Inicializa um provedor de conteúdo.                                                                                         |
| [*WdsTransportProviderOpenContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | Abre uma nova exibição estática de um fluxo de conteúdo.                                                                            |
| [*WdsTransportProviderReadContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | Lê o conteúdo de um fluxo de conteúdo aberto.                                                                              |
| [*WdsTransportProviderRefreshSettings*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | Instrui o provedor de transporte a ler novamente as configurações relevantes.                                                       |
| [*WdsTransportProviderShutdown*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | Shutsdown o provedor de conteúdo.                                                                                         |
| [*WdsTransportProviderUserAccessCheck*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | Especifica o acesso a um fluxo de conteúdo com base no token de um usuário.                                                           |



 

 

 




