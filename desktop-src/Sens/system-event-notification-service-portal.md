---
description: Monitore as notificações de eventos do sistema de programas executados em computadores móveis para determinar a largura de banda e a latência da conexão de rede. Crie aplicativos otimizados para computação móvel e LANs de alta latência.
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: Serviço de Notificação de Eventos do Sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3238441f82c26a33370c37fe09b3e4007639f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922428"
---
# <a name="system-event-notification-service"></a>Serviço de Notificação de Eventos do Sistema

## <a name="purpose"></a>Finalidade

Os aplicativos projetados para uso por usuários móveis exigem um conjunto exclusivo de funções e notificações de conectividade. No passado, esses aplicativos individuais eram necessários para implementar esses recursos internamente. O SENS (serviço de notificação de eventos do sistema) agora fornece esses recursos no sistema operacional, criando uma interface de notificação e conectividade uniforme para aplicativos. O uso de desenvolvedores de sensores pode determinar a largura de banda de conexão e informações de latência de dentro de seu aplicativo e otimizar a operação do aplicativo com base nessas condições.

## <a name="where-applicable"></a>Quando aplicável

As funções de conectividade e as notificações do SENS são úteis para aplicativos escritos para computadores móveis ou computadores conectados a redes locais de alta latência.

## <a name="developer-audience"></a>Público de desenvolvedores

Este documento destina-se a desenvolvedores de software que desenvolvem aplicativos para computação móvel e redes locais de alta latência. Este documento fornece uma referência completa de todas as partes do serviço de notificação de eventos do sistema, incluindo o objeto SENS e os métodos de suporte.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Requer o Microsoft Windows XP ou posterior. Para obter informações sobre quais sistemas operacionais são necessários para usar uma interface ou função específica, consulte a seção requisitos da documentação.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                              | Descrição                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Visão geral](about-system-event-notification-service.md)<br/> | Informações gerais sobre o serviço de notificação de eventos do sistema.<br/>               |
| [Referência](sens-reference.md)<br/>                         | Documentação de métodos e interfaces do serviço de notificação de eventos do sistema.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IEventSubscription**](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 
