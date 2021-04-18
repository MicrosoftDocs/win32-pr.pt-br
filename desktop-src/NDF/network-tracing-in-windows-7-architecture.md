---
title: Rastreamento de rede na arquitetura do Windows 7
description: A ilustração a seguir mostra a arquitetura básica de rastreamento de rede no Windows 7.
ms.assetid: b3023469-0f98-451c-b39f-c3eae771eacc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41221ebf434c05a8c9b7c8489e861128029b5320
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105759195"
---
# <a name="network-tracing-in-windows-7-architecture"></a>Rastreamento de rede no Windows 7: arquitetura

A ilustração a seguir mostra a arquitetura básica de rastreamento de rede no Windows 7.

![diagrama da arquitetura de rastreamento de rede](images/ut1.png)

O rastreamento de rede utiliza a estrutura ETW (rastreamento de eventos para Windows) disponível no Windows. Os componentes de rede (como Winsock, TCP/IP, NDIS, captura de pacotes e assim por diante) se registram como provedores de rastreamento ETW e emitem eventos relacionados à atividade de rede. Qualquer atividade gravável de significância pode ser um evento registrado no ETW. O rastreamento para esses componentes de rede e capturas de pacotes pode ser habilitado usando o contexto de **rastreamento netsh** que atua como um controlador ETW.

Os rastreamentos gerados são coletados em um arquivo de log de rastreamento de eventos (ETL). Esses arquivos ETL podem ser analisados usando várias ferramentas, como Monitor de Rede 3,2 e posterior, Visualizador de Eventos, **netsh trace Convert** ou Tracerpt.exe.

Cada evento ETW tem um cabeçalho comum em que o ETW armazena informações como as propriedades do evento, carimbos de data/hora e ID da atividade. (Para obter mais informações sobre IDs de atividade, consulte [escrevendo eventos relacionados em um cenário de ponta a ponta](../etw/writing-related-events-in-an-end-to-end-scenario.md)). A ID da atividade é usada para correlacionar eventos. No modo de usuário, as IDs de atividade são armazenadas em threads e todos os eventos registrados em um thread serão automaticamente marcados com a mesma ID de atividade. No modo kernel, a ID da atividade deve ser passada explicitamente quando um evento é registrado. Por padrão, os arquivos ETL são correlacionados para agrupar eventos em IDs de atividade específicas.

Para obter mais informações sobre eventos do Windows e ETW, consulte [eventos do Windows](../events/windows-events.md).

## <a name="etw-components-in-network-tracing"></a>Componentes do ETW no rastreamento de rede

O rastreamento de rede usa o ETW como seu mecanismo de rastreamento primário para fornecer informações sobre o que os subsistemas de rede estão fazendo. Há quatro componentes principais no ETW: sessões de rastreamento de eventos, provedores de eventos, controladores de eventos e consumidores de eventos.

O buffer e o log ocorrem em *sessões de rastreamento de eventos*, que aceitam eventos de provedores e criam arquivos de rastreamento.

Um *provedor de eventos* é uma entidade lógica que grava eventos em sessões de ETW. Um provedor de eventos pode ser um aplicativo de modo de usuário, um aplicativo gerenciado, um driver ou qualquer outra entidade de software. Os provedores de eventos se registram com o ETW e gravam eventos de vários pontos no código invocando a API de log do ETW. Devido à crescente Instrumentação de eventos em vários componentes do sistema operacional, mesmo um aplicativo ou cenário simples no Windows conterá vários componentes que são provedores de eventos.

Um *controlador de eventos* inicia e interrompe as sessões de rastreamento de eventos e habilita os provedores. Quando um provedor de eventos é habilitado dinamicamente pelo aplicativo do controlador de eventos, o provedor envia eventos para uma sessão de rastreamento de eventos específica designada pelo controlador de evento. Cada evento enviado pelo provedor de eventos para a sessão de rastreamento de eventos consiste em um cabeçalho fixo, que inclui metadados de eventos e quaisquer dados personalizados adicionais registrados pelo provedor.

Um *consumidor de eventos* é um aplicativo que lê arquivos de log ou que ouve uma sessão de rastreamento de eventos para eventos em tempo real e os processa. Um exemplo de um consumidor de evento é Monitor de Rede da Microsoft 3,2, que inclui a capacidade de ler e exibir arquivos de log produzidos pelo rastreamento de rede no Windows 7.

Os eventos são entregues aos consumidores de eventos em ordem cronológica e há vários aplicativos de consumidor de eventos que exibem os eventos em formatos específicos. Quando um evento é registrado em uma sessão, o ETW adiciona informações adicionais ao cabeçalho do evento, incluindo o carimbo de data/hora, o processo e a ID do thread, o número do processador e os dados de uso da CPU do thread de log. Esses dados são então passados para consumidores de eventos, juntamente com quaisquer dados personalizados incluídos pelo provedor.

Os provedores que usam as novas [APIs de log de eventos](/windows/win32/api/evntprov/nf-evntprov-eventwrite) devem fornecer um arquivo XML chamado manifesto de [evento](../wes/eventschema-schema.md). Esse arquivo fornece metadados para definir todos os dados personalizados e informações de layout para os eventos gravados pelo provedor. Em seguida, um aplicativo consumidor de uso geral usa APIs [TDH (Trace Data Helper)](/windows/win32/api/tdh/) para recuperar os metadados do evento, decodificar os eventos e exibi-los.

Com o rastreamento de rede no Windows 7, o lado do controlador de eventos/consumidor inclui suporte de rastreamento baseado em cenário de ponta a ponta integrado às experiências gerais de diagnóstico e suporte do Windows. Um cenário define uma coleção de provedores de eventos envolvidos no cenário. O lado do controlador de evento/consumidor define os cenários (contextos) em que o rastreamento pode ser usado, incluindo os provedores relevantes para determinados cenários em todos os componentes de rede. O lado do provedor de eventos inclui eventos de rastreamento de rede padronizados de diferentes componentes na pilha de rede, que podem ser correlacionados por meio de IDs de atividade de ETW. Os provedores usam um esquema de rede comum que padroniza o uso de conceitos de ETW, como palavras-chave, níveis, tarefas e OpCodes. O esquema também define eventos que são comuns para muitos componentes de rede, como eventos de erro, eventos de descarte de pacotes, eventos de esquema e eventos de transição de estado.

 

 