---
description: A operação de retirada permite que um aplicativo responda a uma sessão que está alertando em outro endereço. O aplicativo identifica o destino da retirada e retorna um identificador de sessão para a chamada retirada.
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: Separação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e033689ffccf6ba01ad06eb071514c1c37aaca03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662767"
---
# <a name="pickup"></a><span data-ttu-id="cd7b5-104">Separação</span><span class="sxs-lookup"><span data-stu-id="cd7b5-104">Pickup</span></span>

<span data-ttu-id="cd7b5-105">A operação de retirada permite que um aplicativo responda a uma sessão que está alertando em outro endereço.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-105">The pickup operation allows an application to answer a session that is alerting at another address.</span></span> <span data-ttu-id="cd7b5-106">O aplicativo identifica o destino da retirada e retorna um identificador de sessão para a chamada retirada.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-106">The application identifies the target of the pickup and is returned a session identifier for the picked-up call.</span></span>

<span data-ttu-id="cd7b5-107">Há várias maneiras de identificar o destino da solicitação de retirada.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-107">There are several ways to identify the target of the pickup request.</span></span> <span data-ttu-id="cd7b5-108">Primeiro, o aplicativo pode especificar o endereço da parte de alerta.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-108">First, the application may specify the address of the alerting party.</span></span> <span data-ttu-id="cd7b5-109">Em segundo lugar, se nenhum endereço for especificado e a opção permitir, o aplicativo poderá pegar qualquer sessão de alerta em seu grupo de retirada.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-109">Second, if no address is specified and the switch allows it, the application can pick up any alerting session in its pickup group.</span></span> <span data-ttu-id="cd7b5-110">Em terceiro lugar, algumas opções permitem a retirada de um alerta de sessão em um grupo de retirada diferente se o identificador de grupo for especificado.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-110">Third, some switches allow pickup of a session alerting in a different pickup group if the group identifier is specified.</span></span>

<span data-ttu-id="cd7b5-111">Alguns sistemas telefônicos importantes dão suporte a uma *transferência por meio* do recurso de bloqueio em aparências de chamada exclusivas em ponte.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-111">Some key telephone systems support a *transfer through hold* capability on bridged-exclusive call appearances.</span></span> <span data-ttu-id="cd7b5-112">Nesse esquema, um telefone específico possui uma chamada exclusivamente quando a chamada está ativa, mas quando a chamada está em espera, qualquer telefone que tenha uma aparência da linha pode pegar a chamada.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-112">In this scheme, a particular phone owns a call exclusively when the call is active, but when the call is on hold, any phone that has an appearance of the line can pick up the call.</span></span>

<span data-ttu-id="cd7b5-113">**TAPI 2. x:** Um aplicativo pode usar uma operação de retirada com um endereço de destino **nulo** para essa finalidade, semelhante a como a função é usada para pegar uma chamada em espera de chamada em uma linha analógica.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-113">**TAPI 2.x:** An application can use a pickup operation with a **NULL** target address for this purpose, similar to how the function is used to pick up a call waiting call on an analog line.</span></span> <span data-ttu-id="cd7b5-114">LINEADDRFEATURE \_ PICKUPHELD indica a existência do recurso.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-114">LINEADDRFEATURE\_PICKUPHELD indicates the existence of the capability.</span></span>

<span data-ttu-id="cd7b5-115">Se LINEADDRCAPFLAGS \_ PICKUPCALLWAIT for **true**, uma sessão poderá ser selecionada para a qual o usuário tenha forma audível detectado o sinal de espera de chamada, mas para o qual o provedor de serviços não consegue realizar a detecção.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-115">If LINEADDRCAPFLAGS\_PICKUPCALLWAIT is **TRUE**, a session can be picked up for which the user has audibly detected the call-waiting signal but for which the service provider is unable to perform the detection.</span></span> <span data-ttu-id="cd7b5-116">Isso dá ao usuário um mecanismo para "responder" uma chamada em espera mesmo que o provedor de serviços não consiga detectar o sinal de espera de chamada.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-116">This gives the user a mechanism to "answer" a waiting call even though the service provider was unable to detect the call-waiting signal.</span></span> <span data-ttu-id="cd7b5-117">O endereço de destino e a ID do grupo devem ser **nulos** para pegar uma chamada de chamada em espera.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-117">Both the destination address and the group ID must be **NULL** to pick up a call-waiting call.</span></span>

<span data-ttu-id="cd7b5-118">Quando uma sessão tiver sido removida com êxito, o aplicativo receberá uma notificação de alteração de estado com o [motivo](reason-ovr.md) definido como LINECALLREASON \_ pickup.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-118">When a session has been picked up successfully, the application receives a state change notification with the [reason](reason-ovr.md) set to LINECALLREASON\_PICKUP.</span></span>

<span data-ttu-id="cd7b5-119">Nem todos os provedores de serviço dão suporte ao uso desta operação.</span><span class="sxs-lookup"><span data-stu-id="cd7b5-119">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="cd7b5-120">**TAPI 2. x:** Consulte [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).</span><span class="sxs-lookup"><span data-stu-id="cd7b5-120">**TAPI 2.x:** See [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).</span></span>

<span data-ttu-id="cd7b5-121">**TAPI 3. x:** Consulte [**ITBasicCallControl::P ickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).</span><span class="sxs-lookup"><span data-stu-id="cd7b5-121">**TAPI 3.x:** See [**ITBasicCallControl::Pickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).</span></span>

 

 
