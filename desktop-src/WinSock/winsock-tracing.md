---
description: Rastreamento de Winsock
ms.assetid: 0c430fc2-28e7-4537-a887-4c36d24fedee
title: Rastreamento de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803be6220d4d2d440811033786b0f043fab0ff9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814546"
---
# <a name="winsock-tracing"></a>Rastreamento de Winsock

## <a name="introduction"></a>Introdução

O rastreamento do Winsock é um recurso de solução de problemas que pode ser habilitado em binários de varejo para rastrear certos eventos de soquete do Windows com sobrecarga mínima. O objetivo de adicionar o rastreamento de varejo ao Windows Sockets é permitir melhores recursos de diagnóstico para desenvolvedores e suporte a produtos. O rastreamento de eventos de rede do Winsock dá suporte a operações de soquete de rastreamento para aplicativos IPv4 e IPv6. O rastreamento de alterações do catálogo Winsock dá suporte a alterações de rastreamento feitas no catálogo Winsock por provedores de serviço em camadas (LSPs). O rastreamento do Winsock tem suporte no Windows Vista e posterior.

> [!Note]  
> Os provedores de serviço em camadas são preteridos. A partir do Windows 8 e do Windows Server 2012, use a [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).

 

Quando ocorre um erro inesperado em um soquete, a dica principal para diagnosticar o problema é o código de erro retornado. Com muita frequência, o código de erro retornado não explica por que o erro ocorreu, especialmente quando o erro é iniciado pelo transporte de rede subjacente. O rastreamento do Winsock fornece um nível de rastreamento mais detalhado que pode registrar em log informações adicionais para detectar corrupção do buffer e aplicativos mal escritos.

O rastreamento do Winsock usa o ETW (rastreamento de eventos para Windows), um recurso de rastreamento de uso geral de alta velocidade fornecido pelo sistema operacional. Usando um mecanismo de registro em buffer e de log implementado no kernel, o ETW fornece um mecanismo de rastreamento para eventos gerados por aplicativos de modo de usuário e drivers de dispositivo em modo kernel. Além disso, o ETW oferece a capacidade de habilitar e desabilitar o registro em log dinamicamente, facilitando a execução de rastreamento detalhado em ambientes de produção sem a necessidade de reinicializações ou reinicializações do aplicativo. O mecanismo de registro em log usa buffers gravados no disco por um thread de gravador assíncrono. Isso permite que aplicativos de servidor de grande escala gravem eventos com distúrbios mínimo. O ETW foi introduzido pela primeira vez no Windows 2000. O suporte ao rastreamento do Winsock usando o ETW foi adicionado ao Windows Vista e posterior. Para obter informações gerais sobre o ETW, consulte [melhorar a depuração e ajuste de desempenho com o ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

O rastreamento do Winsock só pode ser habilitado no nível do sistema operacional para todos os processos e threads em execução em um computador. Atualmente, o rastreamento de Winsock não pode ser habilitado apenas para um único processo ou thread. Quando o rastreamento de eventos de rede do Winsock está habilitado, todos os aplicativos de soquete (IPv4 e IPv6) em um computador são rastreados.

Os tópicos a seguir descrevem o rastreamento do Winsock mais detalhadamente:

-   [Níveis de rastreamento do Winsock](winsock-tracing-levels.md)
-   [Controle do rastreamento do Winsock](control-of-winsock-tracing.md)
-   [Detalhes de rastreamento de eventos de rede do Winsock](winsock-tracing-event-details.md)
-   [Detalhes de rastreamento de alteração do catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Melhore o ajuste de depuração e desempenho com o ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Recursos de depuração e rastreamento](debug-and-trace-facilities-2.md)
</dt> </dl>

 

 
