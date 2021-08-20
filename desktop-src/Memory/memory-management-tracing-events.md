---
description: 'Saiba mais sobre: Eventos de rastreamento de gerenciamento de memória'
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: Eventos de rastreamento de gerenciamento de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb395082d46ddd668cbb91ee396f211a4055472f49682ab75efc90cedca7ad5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809003"
---
# <a name="memory-management-tracing-events"></a>Eventos de rastreamento de gerenciamento de memória

Esta seção descreve informações detalhadas sobre detalhes específicos do evento de rastreamento de gerenciamento de memória.

O rastreamento de gerenciamento de memória é um recurso de solução de problemas que pode ser habilitado em binários de varejo para rastrear determinados eventos de gerenciamento de memória com sobrecarga mínima. Esse recurso permite melhores funcionalidades de diagnóstico para desenvolvedores e suporte a produtos. O rastreamento de eventos de gerenciamento de memória dá suporte a alocação de heap de rastreamento, realocação e operações gratuitas.

O rastreamento de eventos de gerenciamento de memória usa o ETW (Rastreamento de Windows), um recurso de rastreamento de alta velocidade de uso geral fornecido pelo sistema operacional. O ETW fornece um mecanismo de rastreamento para eventos gerados por aplicativos de modo de usuário e drivers de dispositivo no modo kernel. O ETW pode habilitar e desabilitar o registro em log dinamicamente, facilitando a execução de rastreamento detalhado em ambientes de produção sem a necessidade de reinicializações ou reinicializações do aplicativo. O rastreamento de eventos de gerenciamento de memória usando ETW tem suporte no Windows 7 , Windows Server 2008 R2 e posterior. Para obter informações gerais sobre ETW, consulte [Melhorar a depuração e o ajuste de desempenho com ETW.](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)

A lista a seguir fornece informações detalhadas para cada evento de rastreamento de gerenciamento de memória. Para obter informações adicionais sobre qualquer evento, clique no nome do evento.



| Nome do evento                                                  | Descrição                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [**ETW \_ HEAP \_ EVENT \_ ALLOC**](etw-heap-event-alloc.md)     | Evento de rastreamento de gerenciamento de memória para uma operação de alocação de heap.    |
| [**EVENTO HEAP DE ETW \_ \_ \_ GRATUITO**](etw-heap-event-free.md)       | Evento de rastreamento de gerenciamento de memória para uma operação de heap livre.          |
| [**ETW \_ HEAP \_ EVENT \_ REALLOC**](etw-heap-event-realloc.md) | Evento de rastreamento de gerenciamento de memória para uma operação de reatribuição de heap. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Melhore o ajuste de depuração e desempenho com o ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
