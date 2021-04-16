---
description: O serviço de notificação de eventos do sistema funciona com o sistema de eventos COM+.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: Arquitetura SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32976a716ab0ba5651ce6605fe524d639820696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753926"
---
# <a name="sens-architecture"></a>Arquitetura SENS

O serviço de notificação de eventos do sistema funciona com o sistema de eventos COM+. O SENS é um editor de eventos para as classes de eventos que ele monitora: eventos de rede, logon e energia/bateria. O aplicativo que recebe uma notificação é chamado de assinante de evento.

Quando um aplicativo assina o recebimento de notificações, ele também pode especificar filtros associados aos eventos assinados. Os eventos SENS e COM+ usam os filtros para determinar melhor quando o aplicativo deve ser notificado.

As notificações são assíncronas, portanto, o aplicativo que está recebendo a notificação não precisa estar ativo quando a notificação é enviada. Quando um aplicativo assina o recebimento de notificações, ele pode especificar se ele deve ser ativado quando o evento ocorrer ou notificado posteriormente quando estiver ativo.

A assinatura pode ser transitória e válida somente até que o aplicativo pare de ser executado, ou pode ser persistente e válido até que o aplicativo seja removido do sistema.

Um repositório de dados de eventos COM+ contém informações sobre o sensor de evento (SENS), os assinantes de eventos e os filtros. O SENS também predefine uma interface de saída para cada classe de evento em uma biblioteca de tipos.



| Classe de eventos    | GUID                          | Interface    |
|----------------|-------------------------------|--------------|
| Eventos de rede | \_rede SENSGUID EVENTCLASS \_ | ISensNetwork |
| Eventos de logon   | LOGON do SENSGUID \_ EVENTCLASS \_   | ISensLogon   |
| Eventos de energia   | SENSGUID \_ EVENTCLASS \_ ONNOW   | ISensOnNow   |



 

Para receber notificações para qualquer um desses eventos, seu aplicativo deve fazer duas coisas:

-   Assine os eventos SENS que lhe interessam. Para assinar um evento, use as interfaces **IEventSubscription** e **IEVENTSYSTEM** em eventos com+. Você precisa fornecer um identificador para as classes de evento e o identificador do editor do sensor, SENSGUID \_ Publisher. As assinaturas estão em um nível por evento, de modo que o aplicativo de assinatura também deve especificar quais eventos dentro da classe são interessantes. Cada evento corresponde a um método na interface correspondente à sua classe de evento.
-   Crie um objeto de coletor com uma implementação para cada interface que você manipular. Consulte [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)e [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) para obter mais informações sobre essas interfaces e os eventos com suporte em cada uma delas.

Quando um dos eventos monitorados ocorre, o SENS processa cada assinatura com qualquer filtro associado e notifica os assinantes por meio do sistema de eventos COM+.

 

 



