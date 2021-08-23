---
description: Monitore as notificações de eventos do sistema de programas executados em computadores móveis para determinar a largura de banda e a latência da conexão de rede. Escrever aplicativos otimizados para computação móvel e LANs de alta latência.
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: Serviço de Notificação de Eventos do Sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e76ee51ea0e7a341f0205528e9083cb1f6c0420f941025ec71c32c9154850b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003924"
---
# <a name="system-event-notification-service"></a>Serviço de Notificação de Eventos do Sistema

## <a name="purpose"></a>Finalidade

Aplicativos projetados para uso por usuários móveis exigem um conjunto exclusivo de funções de conectividade e notificações. No passado, esses aplicativos individuais eram necessários para implementar esses recursos internamente. O SENS (Serviço de Notificação de Eventos do Sistema) agora fornece esses recursos no sistema operacional, criando uma interface de notificação e conectividade uniforme para aplicativos. O uso de desenvolvedores SENS pode determinar informações de largura de banda e latência de conexão de dentro de seu aplicativo e otimizar a operação do aplicativo com base nessas condições.

## <a name="where-applicable"></a>Quando aplicável

As funções de conectividade e as notificações do SENS são úteis para aplicativos escritos para computadores móveis ou computadores conectados a redes de área local de alta latência.

## <a name="developer-audience"></a>Público de desenvolvedores

Este documento destina-se a desenvolvedores de software que desenvolvem aplicativos para redes locais de alta latência e computação móvel. Este documento fornece uma referência completa de todas as partes do Serviço de Notificação de Eventos do Sistema, incluindo o objeto SENS e métodos de suporte.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Requer o Microsoft Windows XP ou posterior. Para obter informações sobre quais sistemas operacionais são necessários para usar uma interface ou função específica, consulte a seção Requisitos da documentação.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                              | Descrição                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Visão geral](about-system-event-notification-service.md)<br/> | Informações gerais sobre o Serviço de Notificação de Eventos do Sistema.<br/>               |
| [Referência](sens-reference.md)<br/>                         | Documentação de interfaces e métodos do Serviço de Notificação de Eventos do Sistema.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IEventSubscription**](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 
