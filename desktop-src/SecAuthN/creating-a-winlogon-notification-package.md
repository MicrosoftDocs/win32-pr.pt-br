---
description: Um pacote de notificação do Winlogon é uma DLL que exporta funções que manipulam eventos do Winlogon. Por exemplo, quando um usuário faz logon no sistema, o Winlogon chama a função de manipulador de eventos de logon de cada pacote de notificação para fornecer informações sobre o evento.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Criando um pacote de notificação do Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0127674967ee3155d42e143a1b142d8c83137c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751616"
---
# <a name="creating-a-winlogon-notification-package"></a><span data-ttu-id="38793-104">Criando um pacote de notificação do Winlogon</span><span class="sxs-lookup"><span data-stu-id="38793-104">Creating a Winlogon Notification Package</span></span>

<span data-ttu-id="38793-105">Um pacote de notificação do [*Winlogon*](/windows/desktop/SecGloss/w-gly) é uma DLL que exporta funções que manipulam eventos do Winlogon.</span><span class="sxs-lookup"><span data-stu-id="38793-105">A [*Winlogon*](/windows/desktop/SecGloss/w-gly) notification package is a DLL that exports functions that handle Winlogon events.</span></span> <span data-ttu-id="38793-106">Por exemplo, quando um usuário faz logon no sistema, o Winlogon chama a função de manipulador de eventos de logon de cada pacote de notificação para fornecer informações sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="38793-106">For example, when a user logs onto the system, Winlogon calls each notification package's logon event handler function to provide information about the event.</span></span>

<span data-ttu-id="38793-107">Os nomes das funções de manipulador de eventos implementadas em um pacote de notificação são deixados para o desenvolvedor; O Winlogon verifica o registro para obter os nomes das funções do manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="38793-107">The names of the event handler functions implemented in a notification package are left up to the developer; Winlogon checks the registry to obtain the names of the event handler functions.</span></span> <span data-ttu-id="38793-108">Por exemplo, um pacote de notificação pode implementar a função de manipulador de eventos de logon como sendo que `WLEventLogon` outro pode usar `HandleLogonEvent` .</span><span class="sxs-lookup"><span data-stu-id="38793-108">For example, one notification package might implement the logon event handler function as `WLEventLogon` whereas another might use `HandleLogonEvent`.</span></span>

<span data-ttu-id="38793-109">Você não precisa implementar e registrar manipuladores de eventos para cada evento Winlogon, somente para eventos que são úteis para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="38793-109">You do not have to implement and register event handlers for every Winlogon event, only for events that are useful to your application.</span></span> <span data-ttu-id="38793-110">Cada função de manipulador de eventos deve usar o protótipo de função descrito no [protótipo de função do manipulador de eventos](event-handler-function-prototype.md).</span><span class="sxs-lookup"><span data-stu-id="38793-110">Each event handler function must use the function prototype described in [Event Handler Function Prototype](event-handler-function-prototype.md).</span></span> <span data-ttu-id="38793-111">Este protótipo tem um único parâmetro: uma estrutura de [**\_ \_ informações de notificação do WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) que contém detalhes sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="38793-111">This prototype has a single parameter: a [**WLX\_NOTIFICATION\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) structure that contains details about the event.</span></span>

<span data-ttu-id="38793-112">O Winlogon ignora a saída das funções do manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="38793-112">Winlogon ignores the output of event handler functions.</span></span> <span data-ttu-id="38793-113">Se a manipulação de um evento exigir interação com o Winlogon, use as [funções de suporte do Winlogon](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="38793-113">If handling an event requires interacting with Winlogon, use the [Winlogon Support Functions](authentication-functions.md).</span></span>

<span data-ttu-id="38793-114">Para usar o pacote de notificação do Winlogon, a DLL deve ser copiada para a pasta% SystemRoot% \\ System32 e uma atualização do registro deve ser feita para o pacote de notificação.</span><span class="sxs-lookup"><span data-stu-id="38793-114">To use your Winlogon notification package, the DLL must be copied to the %SystemRoot%\\system32 folder, and a registry update must be made for the notification package.</span></span> <span data-ttu-id="38793-115">Para obter informações sobre a atualização do registro, consulte [registrando um pacote de notificação do Winlogon](registering-a-winlogon-notification-package.md).</span><span class="sxs-lookup"><span data-stu-id="38793-115">For information about the registry update, see [Registering a Winlogon Notification Package](registering-a-winlogon-notification-package.md).</span></span>

 

 
