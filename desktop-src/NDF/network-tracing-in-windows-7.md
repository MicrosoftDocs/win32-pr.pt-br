---
title: Rastreamento de rede no Windows 7
description: O Windows 7 expande o NDF (estrutura de diagnóstico de rede) para fornecer um método rápido para solucionar problemas de conectividade de rede, habilitando a coleta de todas as informações necessárias em uma única etapa e aproveitando o ETW (rastreamento de eventos para Windows) para registrar em log os pacotes de eventos de rede em um único arquivo.
ms.assetid: 7d331362-ff26-4ca0-aa45-07cc97304c7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e3abb4283262703123f8e7060a09af0b810477b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366682"
---
# <a name="network-tracing-in-windows-7"></a>Rastreamento de rede no Windows 7

À medida que a complexidade da pilha de rede aumenta, muitas vezes é difícil rastrear e diagnosticar rapidamente os problemas dentro da pilha. O Windows 7 expande o NDF (estrutura de diagnóstico de rede) para fornecer um método rápido para solucionar problemas de conectividade de rede, habilitando a coleta de todas as informações necessárias em uma única etapa e aproveitando o [ETW (rastreamento de eventos para Windows)](../etw/event-tracing-portal.md) para registrar eventos de rede & pacotes em um único arquivo.

Os eventos e os pacotes relacionados são agrupados para uma determinada atividade, como navegar por um site, entre os vários componentes na pilha de rede. A saída desse processo é um arquivo de log de rastreamento de eventos (ETL). Ao permitir que todos os eventos relacionados a uma atividade específica sejam exibidos ao mesmo tempo nesse arquivo, o tempo necessário para isolar e diagnosticar problemas de rede pode ser bastante reduzido.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|
| [Rastreamento de rede no Windows 7: arquitetura](network-tracing-in-windows-7-architecture.md)                                |
| [Ferramentas para solução de problemas usando o rastreamento de rede no Windows 7](tools-for-troubleshooting-network-tracing-in-windows-7.md) |
| [Rastreamento de rede no Windows 7: cenários](network-tracing-in-windows-7-scenarios.md)                                      |



 

 

 