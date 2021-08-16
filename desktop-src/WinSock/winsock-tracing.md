---
description: Rastreamento winsock
ms.assetid: 0c430fc2-28e7-4537-a887-4c36d24fedee
title: Rastreamento winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb2d9593f4c2cea47e722075f1611151fb276cdf2646a2c9898a9c8d7d156098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321666"
---
# <a name="winsock-tracing"></a>Rastreamento winsock

## <a name="introduction"></a>Introdução

O rastreamento winsock é um recurso de solução de problemas que pode ser habilitado em binários de varejo para rastrear determinados Windows eventos de soquete com sobrecarga mínima. A meta de adicionar o rastreamento de varejo ao Windows Sockets é permitir melhores funcionalidades de diagnóstico para desenvolvedores e suporte a produtos. O rastreamento de eventos de rede Winsock dá suporte a operações de soquete de rastreamento para aplicativos IPv4 e IPv6. O rastreamento de alterações do catálogo Winsock dá suporte a alterações de rastreamento feitas no catálogo winsock por LSPs (provedores de serviços em camadas). O rastreamento winsock tem suporte no Windows Vista e posterior.

> [!Note]  
> Provedores de serviços em camadas foram preterido. Começando com Windows 8 e Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).

 

Quando ocorre um erro inesperado em um soquete, a principal dica para diagnosticar o problema é o código de erro retornado. Muitas vezes, o código de erro retornado não explica por que o erro ocorreu, especialmente quando o erro é iniciado pelo transporte de rede subjacente. O rastreamento winsock fornece um nível de rastreamento mais detalhado que pode registrar informações adicionais para capturar a corrupção de buffer e aplicativos mal escritos.

O rastreamento winsock usa o RASTREAMENTO de Windows (ETW), um recurso de rastreamento de alta velocidade de uso geral fornecido pelo sistema operacional. Usando um mecanismo de buffer e registro em log implementado no kernel, o ETW fornece um mecanismo de rastreamento para eventos gerados por aplicativos de modo de usuário e drivers de dispositivo no modo kernel. Além disso, o ETW oferece a capacidade de habilitar e desabilitar o registro em log dinamicamente, facilitando a execução de rastreamento detalhado em ambientes de produção sem a necessidade de reinicializações ou reinicializações do aplicativo. O mecanismo de registro em log usa buffers gravados em disco por um thread de autor assíncrono. Isso permite que aplicativos de servidor em grande escala gravem eventos com mínimo de confusão. O ETW foi introduzido pela primeira vez Windows 2000. O suporte para rastreamento winsock usando ETW foi adicionado Windows Vista e posterior. Para obter informações gerais sobre ETW, consulte [Melhorar a depuração e o ajuste de desempenho com ETW.](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)

O rastreamento winsock só pode ser habilitado no nível do sistema operacional para todos os processos e threads em execução em um computador. Atualmente, o rastreamento winsock não pode ser habilitado para apenas um único processo ou thread. Quando o rastreamento de eventos de rede Winsock está habilitado, todos os aplicativos de soquete (IPv4 e IPv6) em um computador são rastreados.

Os tópicos a seguir descrevem o rastreamento winsock com mais detalhes:

-   [Níveis de rastreamento winsock](winsock-tracing-levels.md)
-   [Controle do rastreamento winsock](control-of-winsock-tracing.md)
-   [Detalhes do rastreamento de eventos do Winsock Network](winsock-tracing-event-details.md)
-   [Detalhes de rastreamento de alterações do catálogo winsock](winsock-layered-service-provider-tracing-event-details.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Melhore o ajuste de depuração e desempenho com o ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Recursos de depuração e rastreamento](debug-and-trace-facilities-2.md)
</dt> </dl>

 

 
