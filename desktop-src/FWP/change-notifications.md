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
# <a name="change-notifications"></a><span data-ttu-id="bcd80-103">Notificações de alteração</span><span class="sxs-lookup"><span data-stu-id="bcd80-103">Change Notifications</span></span>

<span data-ttu-id="bcd80-104">As notificações de alteração do aplicativo de filtragem de base (BFE) seguem o padrão de publicação/assinatura: para receber uma das notificações de alteração publicadas, um aplicativo precisa se inscrever nele.</span><span class="sxs-lookup"><span data-stu-id="bcd80-104">The Base Filtering Engine (BFE) change notifications follow the publish/subscribe pattern: in order to receive one of the published change notifications, an application has to subscribe to it.</span></span>

<span data-ttu-id="bcd80-105">As notificações de alteração BFE publicadas são adicionar e remover para [**textos explicativos**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**filtros**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**provedores**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**contextos de provedor**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)e [**subcamadas.**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)</span><span class="sxs-lookup"><span data-stu-id="bcd80-105">The published BFE change notifications are Add and Remove for [**callouts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**filters**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**providers**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**provider contexts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0), and [**sub-layers**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).</span></span>

<span data-ttu-id="bcd80-106">Para assinar uma das notificações acima, um aplicativo chama a função de gerenciamento [**Fwpm \* SubscribeChanges0**](fwp-mgmt-functions.md) correspondente (por exemplo, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)).</span><span class="sxs-lookup"><span data-stu-id="bcd80-106">To subscribe to one of the above notifications, an application calls the corresponding [**Fwpm\*SubscribeChanges0**](fwp-mgmt-functions.md) management function (for example, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)).</span></span> <span data-ttu-id="bcd80-107">A função de retorno de chamada passada como um argumento para **Fwpm \* SubscribeChanges0** é invocada por BFE quando a alteração na qual ele se inscreveu ocorre.</span><span class="sxs-lookup"><span data-stu-id="bcd80-107">The callback function passed as an argument to **Fwpm\*SubscribeChanges0** is invoked by BFE when the change to which it subscribed occurs.</span></span>

<span data-ttu-id="bcd80-108">Para cancelar a assinatura de uma das notificações acima, um aplicativo chama a função de gerenciamento **Fwpm \* UnsubscribeChanges0** correspondente (por exemplo, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).</span><span class="sxs-lookup"><span data-stu-id="bcd80-108">To unsubscribe to one of the above notifications, an application calls the corresponding **Fwpm\*UnsubscribeChanges0** management function (for example, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).</span></span>

<span data-ttu-id="bcd80-109">Para ver as assinaturas atuais de uma das notificações acima, um aplicativo chama a função de gerenciamento [**Fwpm \* SubscriptionsGet0**](fwp-mgmt-functions.md) correspondente (por exemplo, [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).</span><span class="sxs-lookup"><span data-stu-id="bcd80-109">To see the current subscriptions for one of the above notifications, an application calls the corresponding [**Fwpm\*SubscriptionsGet0**](fwp-mgmt-functions.md) management function (for example [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).</span></span>

<span data-ttu-id="bcd80-110">As notificações de alteração oferecidas pelo BFE são:</span><span class="sxs-lookup"><span data-stu-id="bcd80-110">The change notifications offered by the BFE are:</span></span>

-   <span data-ttu-id="bcd80-111">Assíncrono — a chamada de função que disparou uma notificação pode retornar antes que a notificação seja expedida para todos os assinantes.</span><span class="sxs-lookup"><span data-stu-id="bcd80-111">Asynchronous — The function call that triggered a notification may return before the notification has been dispatched to all subscribers.</span></span>
-   <span data-ttu-id="bcd80-112">Não confiável – nenhuma garantia é feita informando que as notificações serão entregues com êxito.</span><span class="sxs-lookup"><span data-stu-id="bcd80-112">Unreliable — No guarantee is made that notifications will be successfully delivered.</span></span>

<span data-ttu-id="bcd80-113">Os assinantes não recebem notificações para alterações feitas com o identificador de sessão que eles usaram para assinar.</span><span class="sxs-lookup"><span data-stu-id="bcd80-113">Subscribers do not receive notifications for changes made with the session handle they used to subscribe.</span></span> <span data-ttu-id="bcd80-114">Geralmente, os assinantes precisam ser informados apenas sobre as alterações feitas por outros; Eles já sabem quais alterações foram feitas por conta própria.</span><span class="sxs-lookup"><span data-stu-id="bcd80-114">Generally, subscribers only need to be informed of the changes made by others; they already know which changes were made by themselves.</span></span>

 

 




