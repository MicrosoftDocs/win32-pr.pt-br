---
description: A operação de suspensão permite que um único endereço manipule várias sessões de comunicação.
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Bloquear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df54b246c5bde5914a14b53dd56b71688d92a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827445"
---
# <a name="hold"></a><span data-ttu-id="40259-103">Bloquear</span><span class="sxs-lookup"><span data-stu-id="40259-103">Hold</span></span>

<span data-ttu-id="40259-104">A operação de suspensão permite que um único endereço manipule várias sessões de comunicação.</span><span class="sxs-lookup"><span data-stu-id="40259-104">The hold operation allows a single address to handle multiple communications sessions.</span></span> <span data-ttu-id="40259-105">Colocar uma sessão em um disco rígido libera a linha/endereço do usuário para fazer outras chamadas.</span><span class="sxs-lookup"><span data-stu-id="40259-105">Placing a session on a hard hold frees the user's line/address to make other calls.</span></span> <span data-ttu-id="40259-106">Uma chamada em retenção rígida normalmente não pode ser transferida ou incluída em uma chamada de conferência, mas uma chamada de consulta pode.</span><span class="sxs-lookup"><span data-stu-id="40259-106">A call on hard hold typically cannot be transferred or included in a conference call, but a consultation call can.</span></span> <span data-ttu-id="40259-107">As chamadas de consulta são iniciadas usando as operações de [conferência](conference-ovr.md) ou de [transferência](transfer-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="40259-107">Consultation calls are initiated using [conference](conference-ovr.md) or [transfer](transfer-ovr.md) operations.</span></span>

<span data-ttu-id="40259-108">Depois que uma chamada é colocada em espera com êxito, o estado de chamada normalmente faz a transição para o estado onHold.</span><span class="sxs-lookup"><span data-stu-id="40259-108">After a call has been successfully placed on hold, the call state typically transitions to the onhold state.</span></span> <span data-ttu-id="40259-109">Enquanto uma chamada está em espera, o aplicativo pode receber mensagens sobre alterações de estado da chamada mantida.</span><span class="sxs-lookup"><span data-stu-id="40259-109">While a call is on hold, the application can receive messages about state changes of the held call.</span></span> <span data-ttu-id="40259-110">Por exemplo, se a parte mantida for desligada, o estado da chamada poderá passar para desconectado.</span><span class="sxs-lookup"><span data-stu-id="40259-110">For example, if the held party hangs up, the call state can transition to disconnected.</span></span>

<span data-ttu-id="40259-111">Em uma situação de ponte, a operação de espera pode não fazer a chamada em espera.</span><span class="sxs-lookup"><span data-stu-id="40259-111">In a bridged situation, the hold operation may not actually place the call on hold.</span></span> <span data-ttu-id="40259-112">O status de outras estações na chamada pode controlar (por exemplo, tentar "manter" uma chamada quando não é possível participar de outras estações); em vez disso, a chamada pode simplesmente ser alterada para o estado inativo enquanto ela permanece conectada em outras estações.</span><span class="sxs-lookup"><span data-stu-id="40259-112">The status of other stations on the call can govern (for example, attempting to "hold" a call when other stations are participating is not possible); instead, the call can simply be changed to the inactive state while it remains connected at other stations.</span></span>

<span data-ttu-id="40259-113">Nem todos os provedores de serviço dão suporte ao uso desta operação.</span><span class="sxs-lookup"><span data-stu-id="40259-113">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="40259-114">**TAPI 2. x:** Consulte [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).</span><span class="sxs-lookup"><span data-stu-id="40259-114">**TAPI 2.x:** See [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).</span></span>

<span data-ttu-id="40259-115">**TAPI 3. x:** Consulte [**ITBasicCallControl:: Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).</span><span class="sxs-lookup"><span data-stu-id="40259-115">**TAPI 3.x:** See [**ITBasicCallControl::Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).</span></span>

 

 
