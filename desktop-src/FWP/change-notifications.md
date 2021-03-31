---
title: Notificações de alteração
description: As notificações de alteração do mecanismo de filtragem base (BFE) seguem o padrão de publicação/assinatura.
ms.assetid: 443f1767-5694-4584-ba0f-229275900774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7a3a2069525cc44823ed975fade3b5f100efd8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103917011"
---
# <a name="change-notifications"></a>Notificações de alteração

As notificações de alteração do aplicativo de filtragem de base (BFE) seguem o padrão de publicação/assinatura: para receber uma das notificações de alteração publicadas, um aplicativo precisa se inscrever nele.

As notificações de alteração BFE publicadas são adicionar e remover para [**textos explicativos**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**filtros**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**provedores**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**contextos de provedor**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)e [**subcamadas.**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)

Para assinar uma das notificações acima, um aplicativo chama a função de gerenciamento [**Fwpm \* SubscribeChanges0**](fwp-mgmt-functions.md) correspondente (por exemplo, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)). A função de retorno de chamada passada como um argumento para **Fwpm \* SubscribeChanges0** é invocada por BFE quando a alteração na qual ele se inscreveu ocorre.

Para cancelar a assinatura de uma das notificações acima, um aplicativo chama a função de gerenciamento **Fwpm \* UnsubscribeChanges0** correspondente (por exemplo, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).

Para ver as assinaturas atuais de uma das notificações acima, um aplicativo chama a função de gerenciamento [**Fwpm \* SubscriptionsGet0**](fwp-mgmt-functions.md) correspondente (por exemplo, [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).

As notificações de alteração oferecidas pelo BFE são:

-   Assíncrono — a chamada de função que disparou uma notificação pode retornar antes que a notificação seja expedida para todos os assinantes.
-   Não confiável – nenhuma garantia é feita informando que as notificações serão entregues com êxito.

Os assinantes não recebem notificações para alterações feitas com o identificador de sessão que eles usaram para assinar. Geralmente, os assinantes precisam ser informados apenas sobre as alterações feitas por outros; Eles já sabem quais alterações foram feitas por conta própria.

 

 




