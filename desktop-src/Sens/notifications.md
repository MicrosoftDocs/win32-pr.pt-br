---
description: O serviço de notificação de eventos do sistema permite que aplicativos com reconhecimento de mobilidade recebam notificações de eventos do sistema que o SENS monitora. Quando o evento solicitado ocorre, o SENS notifica o aplicativo.
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: Notificações (serviço de notificação de eventos do sistema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272f0ea60369015328e34d3a83231ab0b254253a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756373"
---
# <a name="notifications-system-event-notification-service"></a><span data-ttu-id="9259d-104">Notificações (serviço de notificação de eventos do sistema)</span><span class="sxs-lookup"><span data-stu-id="9259d-104">Notifications (System Event Notification Service)</span></span>

<span data-ttu-id="9259d-105">O serviço de notificação de eventos do sistema permite que aplicativos com reconhecimento de mobilidade recebam notificações de eventos do sistema que o SENS monitora.</span><span class="sxs-lookup"><span data-stu-id="9259d-105">The System Event Notification Service enables mobile-aware applications to receive notifications from system events that SENS monitors.</span></span> <span data-ttu-id="9259d-106">Quando o evento solicitado ocorre, o SENS notifica o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9259d-106">When the requested event occurs, SENS notifies the application.</span></span>

<span data-ttu-id="9259d-107">O SENS pode notificar aplicativos sobre três classes de eventos do sistema:</span><span class="sxs-lookup"><span data-stu-id="9259d-107">SENS can notify applications about three classes of system events:</span></span>

-   <span data-ttu-id="9259d-108">Eventos de rede TCP/IP, como o status de uma conexão de rede TCP/IP ou a qualidade da conexão.</span><span class="sxs-lookup"><span data-stu-id="9259d-108">TCP/IP network events, such as the status of a TCP/IP network connection or the quality of the connection.</span></span>
-   <span data-ttu-id="9259d-109">Eventos de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="9259d-109">User logon events.</span></span>
-   <span data-ttu-id="9259d-110">Eventos de energia de bateria e AC.</span><span class="sxs-lookup"><span data-stu-id="9259d-110">Battery and AC power events.</span></span>

<span data-ttu-id="9259d-111">Por exemplo, um aplicativo pode assinar qualquer um dos seguintes eventos do sistema:</span><span class="sxs-lookup"><span data-stu-id="9259d-111">For example, an application can subscribe to any of the following system events:</span></span>

-   <span data-ttu-id="9259d-112">Estabelecimento de conectividade de rede</span><span class="sxs-lookup"><span data-stu-id="9259d-112">Establishment of network connectivity</span></span>
-   <span data-ttu-id="9259d-113">Notificação quando um destino especificado pode ser alcançado dentro dos parâmetros de QOC (qualidade de conexão) especificados</span><span class="sxs-lookup"><span data-stu-id="9259d-113">Notification when a specified destination can be reached within specified Quality of Connection (QOC) parameters</span></span>
-   <span data-ttu-id="9259d-114">O computador mudou para a energia da bateria</span><span class="sxs-lookup"><span data-stu-id="9259d-114">The computer has switched to battery power</span></span>
-   <span data-ttu-id="9259d-115">A porcentagem de energia restante da bateria está dentro de um parâmetro especificado</span><span class="sxs-lookup"><span data-stu-id="9259d-115">The percentage of remaining battery power is within a specified parameter</span></span>
-   <span data-ttu-id="9259d-116">Ocorrem eventos agendados usando o Gerenciador de sincronização</span><span class="sxs-lookup"><span data-stu-id="9259d-116">Scheduled events using Synchronization Manager occur</span></span>

<span data-ttu-id="9259d-117">**Windows Server 2008 R2 e Windows 7:** O Assinante tem um máximo de 3 minutos para responder a uma notificação nas interfaces [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) e [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) .</span><span class="sxs-lookup"><span data-stu-id="9259d-117">**Windows Server 2008 R2 and Windows 7:** The subscriber has a maximum of 3 minutes to respond to a notification on the [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) and [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) interfaces.</span></span> <span data-ttu-id="9259d-118">Após 3 minutos, o SENS cancela a chamada para assinantes e desbloqueia o thread de notificação.</span><span class="sxs-lookup"><span data-stu-id="9259d-118">After 3 minutes, SENS cancels the call to subscribers and unblocks the notification thread.</span></span> <span data-ttu-id="9259d-119">Se uma operação demorada for necessária para responder à notificação, retorne de **ISensLogon** ou **ISensLogon2** o mais rápido possível e abra outro thread para processamento.</span><span class="sxs-lookup"><span data-stu-id="9259d-119">If a lengthy operation is required to respond to the notification, return from **ISensLogon** or **ISensLogon2** as quickly as possible and open another thread for processing.</span></span>

 

 



