---
title: Comportamento do pool do sistema
description: Discussão sobre as ações executadas pelo pool do sistema quando avisos de evento são enviados e quando nenhuma operação biométrica está pendente.
ms.assetid: cc1f8ffa-ce69-48ff-8509-81d85807d12a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a82d957b2b1b4968835eec1482662e30765e4a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364057"
---
# <a name="system-pool-behavior"></a>Comportamento do pool do sistema

A discussão a seguir realça as ações executadas pelo pool do sistema quando avisos de evento são enviados e quando nenhuma operação biométrica está pendente.

## <a name="event-dispatching"></a>Expedição de eventos

Quando uma unidade biométrica gera um aviso de evento, o pool de sistema usa um filtro em cascata para enviar o aviso e atribuir a ele um dos seguintes níveis de prioridade:

-   A prioridade alta é atribuída à correspondência explícita e às solicitações de registro geradas pelos clientes.
-   A prioridade média é atribuída a eventos de registro ou de correspondência inesperados ou não reivindicados.
-   Baixa prioridade é atribuída a eventos de navegação.

Os eventos de captura são entregues na seguinte sequência:

-   Se a janela de foco atual estiver aguardando uma operação de registro ou correspondência, o exemplo será processado e enviado ao cliente que possui a janela de foco atual.
-   Se o evento de captura não for reivindicado pela janela de foco atual e um manipulador de eventos não reivindicado tiver sido registrado com o serviço biométrico do Windows, o evento de captura será enviado para esse manipulador.
-   Se o evento permanecer não reivindicado, ele será Descartado.

Se o evento for um evento de navegação e um manipulador de eventos de navegação tiver sido registrado com o serviço biométrico do Windows, o evento de captura será enviado para esse manipulador. Se não houver nenhum manipulador de eventos, o evento será Descartado.

## <a name="idle-mode"></a>Modo ocioso

Quando não há clientes aguardando que as solicitações de registro ou correspondência explícita sejam concluídas, o pool do sistema determina se as solicitações de captura repetidas devem ser geradas automaticamente e o aviso de evento resultante será enviado ao manipulador de eventos não reivindicado ou se os eventos de navegação serão enviados para o manipulador de eventos de navegação.

Se um manipulador de eventos não reivindicado tiver sido registrado com o serviço biométrico do Windows, o pool do sistema executará as seguintes ações:

-   O modo de navegação do sensor está desabilitado.
-   As operações não solicitadas são enviadas para o manipulador de eventos, independentemente do foco da janela.
-   Se não houver nenhuma solicitação pendente para uma operação biométrica, uma captura automática será executada.

Se um manipulador de navegação tiver sido registrado com o serviço biométrico do Windows, o pool do sistema fará o seguinte:

-   As unidades biométricas no pool do sistema serão colocadas em um estado de navegação se nenhuma operação biométrica estiver pendente.
-   Os eventos de navegação serão desabilitados se um aviso de evento de correspondência ou de registro for enviado por um cliente.
-   Se um manipulador de eventos não reivindicado tiver sido registrado, os eventos de navegação serão desabilitados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pool de sensores privado](private-sensor-pool.md)
</dt> <dt>

[Pools de sensores](sensor-pools.md)
</dt> <dt>

[Pool do sensor do sistema](system-sensor-pool.md)
</dt> </dl>

 

 




