---
description: O encaminhamento é a deflexão de uma sessão de entrada para um endereço de destino diferente.
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: Encaminhar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4154e2bb6f8c688feffe2e33d3c5988b0b7da27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827139"
---
# <a name="forward"></a><span data-ttu-id="de431-103">Encaminhar</span><span class="sxs-lookup"><span data-stu-id="de431-103">Forward</span></span>

<span data-ttu-id="de431-104">O encaminhamento é a deflexão de uma sessão de entrada para um endereço de destino diferente.</span><span class="sxs-lookup"><span data-stu-id="de431-104">Forwarding is the deflection of an incoming session to a different destination address.</span></span> <span data-ttu-id="de431-105">A TAPI permite que um aplicativo especifique uma lista de condições de encaminhamento para um endereço.</span><span class="sxs-lookup"><span data-stu-id="de431-105">TAPI allows an application to specify a list of forwarding conditions for an address.</span></span> <span data-ttu-id="de431-106">As condições de encaminhamento podem ser tão refinadas como um destino e [**modo de encaminhamento**](./lineforwardmode--constants.md) diferentes para cada endereço de chamador.</span><span class="sxs-lookup"><span data-stu-id="de431-106">Forwarding conditions can be as finely grained as a different destination and [**forwarding mode**](./lineforwardmode--constants.md) for each caller address.</span></span>

<span data-ttu-id="de431-107">A operação de encaminhamento também pode ser usada para implementar um recurso do-não-perturbe seletivo, encaminhando alguns chamadores para o correio de voz e permitindo que outros tentem a conclusão.</span><span class="sxs-lookup"><span data-stu-id="de431-107">The forwarding operation can also be used to implement a selective do-not-disturb feature, by forwarding some callers to voice mail and allowing others to attempt completion.</span></span>

<span data-ttu-id="de431-108">A operação de encaminhamento também pode cancelar qualquer encaminhamento atualmente em vigor.</span><span class="sxs-lookup"><span data-stu-id="de431-108">The forwarding operation can also cancel any forwarding currently in effect.</span></span>

<span data-ttu-id="de431-109">Alguns provedores de serviços exigem que um aplicativo crie uma chamada de consulta antes de uma operação de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="de431-109">Some service providers require that an application create a consultation call prior to a forwarding operation.</span></span> <span data-ttu-id="de431-110">Em seguida, a operação de encaminhamento passa um ponteiro para a chamada de consulta.</span><span class="sxs-lookup"><span data-stu-id="de431-110">The forwarding operation is then passed a pointer to the consultation call.</span></span>

<span data-ttu-id="de431-111">Nem todos os provedores de serviço dão suporte ao uso desta operação.</span><span class="sxs-lookup"><span data-stu-id="de431-111">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="de431-112">**TAPI 2. x:** Para definir [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) para obter [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), altere a mensagem de notificação [**\_ addressstate de linha**](./line-addressstate.md) com o LINEADDRESSSTATE \_ forward.</span><span class="sxs-lookup"><span data-stu-id="de431-112">**TAPI 2.x:** To set [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) to get [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), change the [**LINE\_ADDRESSSTATE**](./line-addressstate.md) notification message with LINEADDRESSSTATE\_FORWARD.</span></span>

<span data-ttu-id="de431-113">**TAPI 3. x:** Consulte [**ITAddress:: encaminhar**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress:: get \_ CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), notificação de alteração: [**ITADDRESSEVENT:: get \_ evento**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) com AE \_ forward.</span><span class="sxs-lookup"><span data-stu-id="de431-113">**TAPI 3.x:** See [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress::get\_CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), change notification: [**ITAddressEvent::get\_Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE\_FORWARD.</span></span>

> [!Note]  
> <span data-ttu-id="de431-114">Pode ser impossível que um provedor de serviços saiba sempre que o encaminhamento está em vigor para um endereço.</span><span class="sxs-lookup"><span data-stu-id="de431-114">It may be impossible for a service provider to know at all times what forwarding is in effect for an address.</span></span> <span data-ttu-id="de431-115">O encaminhamento pode ser cancelado ou alterado de maneiras que não resultam em notificação para o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="de431-115">Forwarding can be canceled or changed in ways that do not result in notification to the service provider.</span></span>

 

 

 
