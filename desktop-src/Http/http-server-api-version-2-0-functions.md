---
title: Funções da API do servidor HTTP versão 2,0
description: A API do servidor HTTP versão 2,0 fornece as funções a seguir.
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- Funções da API do servidor HTTP versão 2,0
- Funções HTTP, API do servidor HTTP versão 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b832a3f8fb1a97c48c49809d3e2f1975965becdc4c7bbf3942601d577d4702d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981356"
---
# <a name="http-server-api-version-20-functions"></a>Funções da API do servidor HTTP versão 2,0

A API do servidor HTTP versão 2,0 fornece as funções a seguir.

| Função | Descrição |
|-|-|
| [**HttpDelegateRequestEx**](/windows/win32/api/http/nf-http-httpdelegaterequestex) | Delega uma solicitação da fila de solicitação de origem para a fila de solicitação de destino. |
| [**HttpFindUrlGroupId**](/windows/win32/api/http/nf-http-httpfindurlgroupid) | Recupera uma ID de grupo de URL para uma URL e uma fila de solicitação. |
| [**HttpIsFeatureSupported**](/windows/win32/api/http/nf-http-httpisfeaturesupported) | Verifica se há suporte para um recurso específico. |

## <a name="server-session"></a>Sessão de servidor

| Função | Descrição |
|-|-|
| [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession) | |
| [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) | |
| [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) | |
| [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) | |

## <a name="url-groups"></a>Grupos de URLs

| Função | Descrição |
|-|-|
| [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) | |
| [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) | |
| [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) | |
| [**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) | |
| [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) | |
| [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) | |

## <a name="request-queue"></a>Fila de solicitação

| Função | Descrição |
|-|-|
| [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue) | |
| [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) | |
| [**HttpQueryRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) | |
| [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) | |
| [**HttpShutdownRequestQueue**](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue) | |
| [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) | |

## <a name="related-topics"></a>Tópicos relacionados

[Estruturas da API do servidor HTTP versão 2,0](http-server-api-version-2-0-structures.md)
