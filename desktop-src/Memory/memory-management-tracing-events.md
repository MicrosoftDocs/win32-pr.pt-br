---
description: 'Saiba mais sobre: eventos de rastreamento de gerenciamento de memória'
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: Eventos de rastreamento de gerenciamento de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ca05260b6c29ecae765c047691b81a26116fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766886"
---
# <a name="memory-management-tracing-events"></a>Eventos de rastreamento de gerenciamento de memória

Esta seção descreve informações detalhadas sobre detalhes específicos do evento de rastreamento de gerenciamento de memória.

O rastreamento de gerenciamento de memória é um recurso de solução de problemas que pode ser habilitado em binários de varejo para rastrear determinados eventos de gerenciamento de memória com sobrecarga mínima. Esse recurso permite melhores recursos de diagnóstico para desenvolvedores e suporte a produtos. O rastreamento de eventos de gerenciamento de memória dá suporte à alocação de heap de rastreamento, realocação e operações gratuitas.

O rastreamento de eventos de gerenciamento de memória usa o ETW (rastreamento de eventos para Windows), um recurso de rastreamento de alta velocidade e uso geral fornecido pelo sistema operacional. O ETW fornece um mecanismo de rastreamento para eventos gerados por aplicativos de modo de usuário e drivers de dispositivo em modo kernel. O ETW pode habilitar e desabilitar o registro em log dinamicamente, facilitando a execução de rastreamento detalhado em ambientes de produção sem a necessidade de reinicializações ou reinicializações do aplicativo. O rastreamento de eventos de gerenciamento de memória usando o ETW tem suporte no Windows 7, Windows Server 2008 R2 e posterior. Para obter informações gerais sobre o ETW, consulte [melhorar a depuração e ajuste de desempenho com o ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

A lista a seguir fornece informações detalhadas para cada evento de rastreamento de gerenciamento de memória. Para obter informações adicionais sobre qualquer evento, clique no nome do evento.



| Nome do evento                                                  | Descrição                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [**\_alocação de \_ evento de heap do ETW \_**](etw-heap-event-alloc.md)     | Evento de rastreamento de gerenciamento de memória para uma operação de alocação de heap.    |
| [**evento de heap de ETW \_ \_ \_ gratuito**](etw-heap-event-free.md)       | Evento de rastreamento de gerenciamento de memória para uma operação de heap livre.          |
| [**realocação de evento de \_ heap ETW \_ \_**](etw-heap-event-realloc.md) | Evento de rastreamento de gerenciamento de memória para uma operação de realocação de heap. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Melhore o ajuste de depuração e desempenho com o ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
