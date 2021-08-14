---
title: Comportamento do pool do sistema
description: Discussão sobre as ações tomadas pelo pool do sistema quando os avisos de evento são enviados e quando nenhuma operação biométrica está pendente.
ms.assetid: cc1f8ffa-ce69-48ff-8509-81d85807d12a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923cfff4b36bd14d100ce1f73db455be5261d75dc2c5be1eddc8f9d6af87fce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911589"
---
# <a name="system-pool-behavior"></a>Comportamento do pool do sistema

A discussão a seguir destaca as ações realizadas pelo pool do sistema quando os avisos de evento são enviados e quando nenhuma operação biométrica está pendente.

## <a name="event-dispatching"></a>Expedição de eventos

Quando uma unidade biométrica gera um aviso de evento, o pool do sistema usa um filtro em cascata para expedir o aviso e atribuir a ele um dos seguintes níveis de prioridade:

-   A alta prioridade é atribuída a solicitações explícitas de correspondência e registro geradas pelos clientes.
-   A prioridade média é atribuída a eventos de correspondência ou registro inesperados ou não afirmados.
-   A baixa prioridade é atribuída a eventos de navegação.

Os eventos de captura são entregues na seguinte sequência:

-   Se a janela de foco atual estiver aguardando uma operação de correspondência ou registro, o exemplo será processado e enviado ao cliente que possui a janela de foco atual.
-   Se o evento de captura não for confirmado pela janela de foco atual e um manipulador de eventos não confirmado tiver sido registrado com o serviço biométrico Windows, o evento de captura será enviado para esse manipulador.
-   Se o evento permanecer nãoclamado, ele será descartado.

Se o evento for um evento de navegação e um manipulador de eventos de navegação tiver sido registrado com o serviço biométrico Windows, o evento de captura será enviado para esse manipulador. Se não houver nenhum manipulador de eventos, o evento será descartado.

## <a name="idle-mode"></a>Modo ocioso

Quando não há clientes aguardando a conclusão de solicitações explícitas de correspondência ou registro, o pool de sistema determina se deve gerar automaticamente solicitações de captura repetidas e enviar o aviso de evento resultante para o manipulador de eventos nãocladido ou aguardar eventos de navegação e enviá-los para o manipulador de eventos de navegação.

Se um manipulador de eventos não confirmado tiver sido registrado com o serviço biométrico Windows, o pool de sistema executará as seguintes ações:

-   O modo de navegação para o sensor está desabilitado.
-   Operações não afirmadas são enviadas para o manipulador de eventos, independentemente do foco da janela.
-   Se não houver solicitações pendentes para uma operação biométrica, uma captura automática será executada.

Se um manipulador de navegação tiver sido registrado com o serviço biométrico Windows, o pool de sistema faz o seguinte:

-   As unidades biométricas no pool do sistema serão colocadas em um estado de navegação se nenhuma operação biométrica estiver pendente.
-   Os eventos de navegação serão desabilitados se uma notificação de evento de registro ou de corresponder for enviada por um cliente.
-   Se um manipulador de eventos não confirmado tiver sido registrado, os eventos de navegação serão desabilitados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pool de Sensor Privado](private-sensor-pool.md)
</dt> <dt>

[Sensor Pools](sensor-pools.md)
</dt> <dt>

[Pool de Sensor do Sistema](system-sensor-pool.md)
</dt> </dl>

 

 




