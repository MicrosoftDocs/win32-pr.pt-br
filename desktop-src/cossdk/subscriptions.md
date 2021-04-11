---
description: 'Os dados de assinatura residem no catálogo COM+ da assinatura. Uma assinatura pode ser criada usando a ferramenta administrativa serviços de componentes ou programaticamente usando a interface ICOMAdminCatalog:: InstallComponent.'
ms.assetid: 190e88f3-1d87-4c27-9451-0a633cbae829
title: Assinaturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9973eb76fc22354f1a2fc8e381c90cf5be1efee3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164015"
---
# <a name="subscriptions"></a>Assinaturas

Os dados de assinatura residem no catálogo COM+ da assinatura. Uma assinatura pode ser criada usando a ferramenta administrativa serviços de componentes ou programaticamente usando a interface [**ICOMAdminCatalog:: InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent) .

A coleção [**SubscriptionsForComponent**](subscriptionsforcomponent.md) é usada para adicionar, excluir ou alterar informações pertencentes a assinaturas. A coleção **SubscriptionsForComponent** é uma coleção filho de um componente. Para adicionar uma assinatura, obtenha a coleção **SubscriptionsForComponent** do componente e use o método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) para adicionar uma entrada à coleção. Para configurar as várias propriedades do objeto de assinatura, use a propriedade [**Value**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) . Para salvar as alterações, use [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) no objeto da coleção **SubscriptionsForComponent** .

Você também pode usar a ferramenta de administração de serviços de componentes para modificar algumas, mas não todas, as propriedades da assinatura. As assinaturas especificam as seguintes informações:

-   Identidade e local do assinante
-   Método de entrega
-   Métodos de evento a serem entregues
-   Objeto de classe de evento e a propriedade PublisherID de um componente de classe de evento do qual o assinante deseja receber eventos

As assinaturas existem independentemente dos objetos da classe de evento. Você pode desabilitar uma assinatura definindo a propriedade Enabled como false. Uma assinatura desabilitada não é chamada por eventos COM+.

Os três tipos de assinaturas são os seguintes:

<dl> <dt>

<span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>Persistente
</dt> <dd>

As assinaturas persistentes residem no catálogo COM+ e são independentes do tempo de vida do Assinante. As assinaturas persistentes sobrevivem a uma reinicialização do sistema. Geralmente, uma assinatura persistente é criada quando um aplicativo é instalado no computador de um assinante e removido quando o aplicativo é removido. Depois que uma assinatura persistente é criada, os eventos COM+ ativam o assinante sempre que um evento deve ser entregue a ele.

Quando um Publicador instancia e faz uma chamada em um objeto de [classe de evento](the-com--event-class-object.md) , o objeto procura todas as assinaturas persistentes no catálogo com+ e cria uma nova instância de cada objeto. O processo de criação pode ser direto ou por meio de um moniker para componentes em fila. Especifique o objeto de assinante pela propriedade [**SubscriberMoniker**](subscriptionsforcomponent.md) da assinatura. Os objetos de assinante criados por uma assinatura persistente são sempre liberados após cada chamada de evento.

</dd> <dt>

<span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>Transitório
</dt> <dd>

Para assinaturas transitórias, você pode usar a coleção [**TransientSubscriptions**](transientsubscriptions.md) , cujo objeto pai é o objeto de catálogo raiz. Assinaturas transitórias solicitam um evento para um objeto de Assinante específico que já existe. As assinaturas transitórias são armazenadas no catálogo COM+, mas a assinatura é excluída se o sistema de eventos ou o sistema operacional for interrompido. Ao contrário das assinaturas persistentes, as assinaturas transitórias são vinculadas a um objeto específico e são armazenadas apenas no sistema de eventos. Assinaturas transitórias podem ser mais eficientes do que assinaturas persistentes, mas você deve gerenciar seus ciclos de vida do objeto. Para obter informações sobre como registrar uma assinatura transitória, consulte [registrando uma assinatura transitória](registering-a-transient-subscription.md).

</dd> <dt>

<span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>Por usuário
</dt> <dd>

As assinaturas por usuário podem entregar eventos somente quando o assinante está conectado ao computador do sistema de eventos. Quando o assinante faz logon, o sistema de eventos habilita todas as assinaturas nas quais o sinalizador de *Peruser* está definido como **true** e *username* é definido como o nome do usuário que está conectado. Quando o assinante faz logoff, as assinaturas são desabilitadas.

As assinaturas por usuário entram em vigor somente quando o Publicador e o assinante estão no mesmo computador. O logon e o logoff são detectados somente no computador do Publicador — e não no computador no qual o objeto do assinante reside.

</dd> </dl>

O sistema de eventos usa meta-Events para notificar os assinantes interessados sempre que os objetos ou assinaturas da classe de evento forem criados, modificados ou removidos. Para receber meta-eventos do sistema de eventos, os aplicativos devem criar uma assinatura que resida no computador do sistema de eventos e que especifique a ID da interface de acionamento (IID \_ IEventObjectChange).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtrando eventos no COM+](filtering-events-in-com-.md)
</dt> <dt>

[Publicando e fornecendo eventos no COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[O objeto de classe de evento COM+](the-com--event-class-object.md)
</dt> <dt>

[Usando eventos COM+ com componentes em fila COM+](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



