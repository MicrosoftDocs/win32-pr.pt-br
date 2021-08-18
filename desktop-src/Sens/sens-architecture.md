---
description: O Serviço de Notificação de Eventos do Sistema funciona com o Sistema de Eventos COM+.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: Arquitetura DO SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586ad8ae9c5ec50f4f36c07ed592599cf5e09775bd7f450844c83cc42a4c580f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890405"
---
# <a name="sens-architecture"></a>Arquitetura DO SENS

O Serviço de Notificação de Eventos do Sistema funciona com o Sistema de Eventos COM+. O SENS é um editor de eventos para as classes de eventos que monitora: eventos de rede, logon e energia/bateria. O aplicativo que recebe uma notificação é chamado de assinante de evento.

Quando um aplicativo assina receber notificações, ele também pode especificar filtros associados aos eventos inscritos. Eventos SENS e COM+ usam os filtros para determinar ainda mais quando o aplicativo deve ser notificado.

As notificações são assíncronas, portanto, o aplicativo que recebe a notificação não precisa estar ativo quando a notificação é enviada. Quando um aplicativo assina receber notificações, ele pode especificar se ele deve ser ativado quando o evento ocorrer ou ser notificado posteriormente quando estiver ativo.

A assinatura pode ser transitória e válida somente até que o aplicativo pare de ser executado ou possa ser persistente e válido até que o aplicativo seja removido do sistema.

Um armazenamento de dados de Eventos COM+ contém informações sobre o SENS (Editor de Eventos), assinantes de eventos e filtros. O SENS também predefine uma interface de saída para cada classe de evento em uma biblioteca de tipos.



| Classe de eventos    | GUID                          | Interface    |
|----------------|-------------------------------|--------------|
| Eventos de rede | SENSGUID \_ EVENTCLASS \_ NETWORK | ISensNetwork |
| Eventos de logon   | LOGON DE EVENTCLASS SENSGUID \_ \_   | ISensLogon   |
| Eventos de energia   | SENSGUID \_ EVENTCLASS \_ ONNOW   | ISensOnNow   |



 

Para receber notificações para qualquer um desses eventos, seu aplicativo deve fazer duas coisas:

-   Assine os eventos SENS que lhe interessam. Para assinar um evento, use as interfaces **IEventSubscription** e **IEventSystem** em Eventos COM+. Você precisa fornecer um identificador para as classes de evento e o identificador do editor SENS, SENSGUID \_ PUBLISHER. As assinaturas estão em um nível por evento, portanto, o aplicativo de assinatura também deve especificar quais eventos dentro da classe são de interesse. Cada evento corresponde a um método na interface correspondente à sua classe de evento.
-   Crie um objeto de sink com uma implementação para cada interface que você manipular. Consulte [**ISensNetwork,**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)e [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) para obter mais informações sobre essas interfaces e os eventos com suporte em cada uma delas.

Quando um dos eventos monitorados ocorre, o SENS processa cada assinatura com quaisquer filtros associados e notifica os assinantes por meio do sistema de eventos COM+.

 

 



