---
description: Detalhes de eventos de rastreamento do Winsock.
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Eventos de rastreamento de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b2f36991a187d32359694956efcc7b7e3243ac17efd769db454848b5f87e5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821980"
---
# <a name="winsock-tracing-events"></a>Eventos de rastreamento de Winsock

Esta seção descreve informações detalhadas sobre os detalhes específicos de eventos de rastreamento do Winsock.

o rastreamento do Winsock é um recurso de solução de problemas que pode ser habilitado em binários de varejo para rastrear certos Windows eventos de soquete com sobrecarga mínima. Esse recurso permite melhores recursos de diagnóstico para desenvolvedores e suporte a produtos. O rastreamento de eventos de rede do Winsock dá suporte a operações de soquete de rastreamento para aplicativos IPv4 e IPv6. O rastreamento de alterações do catálogo Winsock dá suporte a alterações de rastreamento feitas no catálogo Winsock por provedores de serviço em camadas (LSPs).

> [!Note]  
> Os provedores de serviço em camadas são preteridos. começando com Windows 8 e Windows Server 2012, use [Windows plataforma de filtragem](../fwp/windows-filtering-platform-start-page.md).

 

o rastreamento do Winsock usa o ETW (rastreamento de eventos para Windows), um recurso de rastreamento de uso geral de alta velocidade fornecido pelo sistema operacional. O ETW fornece um mecanismo de rastreamento para eventos gerados por aplicativos de modo de usuário e drivers de dispositivo em modo kernel. O ETW pode habilitar e desabilitar o registro em log dinamicamente, facilitando a execução de rastreamento detalhado em ambientes de produção sem a necessidade de reinicializações ou reinicializações do aplicativo. o suporte ao rastreamento do Winsock usando o ETW foi adicionado no Windows Vista e posterior. Para obter informações gerais sobre o ETW, consulte [melhorar a depuração e ajuste de desempenho com o ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

A lista a seguir fornece informações detalhadas para cada evento de rastreamento do Winsock. Para obter informações adicionais sobre qualquer evento, clique no nome do evento.



| Nome do evento                                                            | Descrição                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_criar evento de AFD \_**](afd-event-create.md)                        | Evento de rastreamento de rede Winsock para uma operação de criação de soquete.                            |
| [**\_fechamento do evento de AFD \_**](afd-event-close.md)                          | Evento de rastreamento de rede Winsock para operação de fechamento de soquete.                                 |
| [**Instalação do WINSOCK \_ ws2help \_ LSP \_**](winsock-ws2help-lsp-install.md) | Evento de alteração de catálogo Winsock para uma operação de instalação do LSP (provedor de serviço em camadas). |
| [**\_Remoção de \_ LSP \_ ws2help do Winsock**](winsock-ws2help-lsp-remove.md)   | Evento de alteração de catálogo Winsock para uma operação de remoção de LSP (provedor de serviço em camadas).      |
| [**\_ \_ Desabilitação de LSP ws2help do Winsock \_**](winsock-ws2help-lsp-disable.md) | Evento de alteração de catálogo Winsock para uma operação de desabilitação de LSP (provedor de serviço em camadas).      |
| [**Redefinição de \_ LSP ws2help Winsock \_ \_**](winsock-ws2help-lsp-reset.md)     | Evento de alteração de catálogo Winsock para uma operação de redefinição de catálogo Winsock.                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Melhore o ajuste de depuração e desempenho com o ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Rastreamento de Winsock](winsock-tracing.md)
</dt> <dt>

[Níveis de rastreamento do Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Controle do rastreamento do Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Detalhes de rastreamento de eventos de rede do Winsock](winsock-tracing-event-details.md)
</dt> <dt>

[Detalhes de rastreamento de alteração do catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
