---
description: Os dados de assinatura residem no catálogo COM+ da assinatura. Uma assinatura pode ser criada usando a ferramenta administrativa serviços de componentes ou programaticamente usando a interface ICOMAdminCatalog::InstallComponent.
ms.assetid: 190e88f3-1d87-4c27-9451-0a633cbae829
title: Assinaturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48810ae90f3507ea7afb661b106c4d05f8cc5b9a4f1b09aafdfb26d9fdb03a75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546168"
---
# <a name="subscriptions"></a>Assinaturas

Os dados de assinatura residem no catálogo COM+ da assinatura. Uma assinatura pode ser criada usando a ferramenta administrativa serviços de componentes ou programaticamente usando a interface [**ICOMAdminCatalog::InstallComponent.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)

A [**coleção SubscriptionsForComponent**](subscriptionsforcomponent.md) é usada para adicionar, excluir ou alterar informações referentes às assinaturas. A **coleção SubscriptionsForComponent** é uma coleção filho de um componente. Para adicionar uma assinatura, obter a coleção **SubscriptionsForComponent** do componente e usar o método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) para adicionar uma entrada à coleção. Para configurar as várias propriedades do objeto de assinatura, use a [**propriedade**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) Value. Para salvar as alterações, use [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) no objeto de coleção **SubscriptionsForComponent.**

Você também pode usar a ferramenta de administração dos Serviços de Componentes para modificar algumas das propriedades da assinatura, mas não todas. As assinaturas especificam as seguintes informações:

-   Identidade e local do assinante
-   Método de entrega
-   Métodos de evento a entregar
-   Objeto de classe de evento e propriedade PublisherID de um componente de classe de evento do qual o assinante deseja receber eventos

As assinaturas existem independentemente dos objetos de classe de evento. Você pode desabilitar uma assinatura definindo a propriedade Habilitado como False. Uma assinatura desabilitada não é chamada por Eventos COM+.

Os três tipos de assinaturas são os seguinte:

<dl> <dt>

<span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>Persistente
</dt> <dd>

As assinaturas persistentes residem no catálogo COM+ e são independentes do tempo de vida do assinante. As assinaturas persistentes sobrevivem a uma reinicialização do sistema. Em geral, uma assinatura persistente é criada quando um aplicativo é instalado no computador de um assinante e removido quando o aplicativo é removido. Depois que uma assinatura persistente é criada, eventos COM+ ativam o assinante sempre que um evento deve ser entregue a ele.

Quando um publicador instancia e [](the-com--event-class-object.md) faz uma chamada em um objeto de classe de evento, o objeto procura todas as assinaturas persistentes no catálogo COM+ e cria uma nova instância de cada objeto. O processo de criação pode ser direto ou por meio de um moniker para componentes na fila. Especifique o objeto de assinante [**pela propriedade SubscriberMoniker**](subscriptionsforcomponent.md) da assinatura. Os objetos de assinante criados por uma assinatura persistente sempre são liberados após cada chamada de evento.

</dd> <dt>

<span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>Transitório
</dt> <dd>

Para assinaturas transitórias, você pode usar a coleção [**TransientSubscriptions,**](transientsubscriptions.md) cujo objeto pai é o objeto de catálogo raiz. As assinaturas transitórias solicitam um evento para um objeto de assinante específico que já existe. As assinaturas transitórias são armazenadas no catálogo COM+, mas a assinatura será excluída se o sistema operacional ou o sistema operacional de eventos for interrompido. Ao contrário das assinaturas persistentes, as assinaturas transitórias são vinculadas a um objeto específico e são armazenadas somente no sistema de eventos. Assinaturas transitórias podem ser mais eficientes do que assinaturas persistentes, mas você deve gerenciar seus ciclos de vida do objeto. Para obter informações sobre como registrar uma assinatura transitória, consulte [Registrando uma assinatura transitória.](registering-a-transient-subscription.md)

</dd> <dt>

<span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>Por usuário
</dt> <dd>

As assinaturas por usuário podem entregar eventos somente quando o assinante estiver conectado ao computador do sistema de eventos. Quando o assinante faz logor, o sistema de eventos habilita todas as assinaturas nas quais o sinalizador *PerUser* está definido como **TRUE** e *UserName* é definido como o nome do usuário que está conectado. Quando o assinante faz o login, as assinaturas são desabilitadas.

As assinaturas por usuário só são efetivadas quando o publicador e o assinante estão no mesmo computador. O logon e o logoff são detectados somente no computador do editor, não no computador no qual o objeto do assinante reside.

</dd> </dl>

O sistema de eventos usa metadados para notificar os assinantes interessados sempre que objetos de classe de evento ou assinaturas são criados, modificados ou removidos. Para receber metadados do sistema de eventos, os aplicativos devem criar uma assinatura que reside no computador do sistema de eventos e que especifique a ID da interface de acionamento \_ (IID IEventObjectChange).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtrando eventos em COM+](filtering-events-in-com-.md)
</dt> <dt>

[Publicando e entregando eventos em COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[O objeto da classe de evento COM+](the-com--event-class-object.md)
</dt> <dt>

[Usando eventos COM+ com componentes em fila COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



