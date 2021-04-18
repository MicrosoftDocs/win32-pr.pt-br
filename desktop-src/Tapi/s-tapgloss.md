---
description: Os termos a seguir são úteis para entender a tecnologia TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b4256a4a-c19e-4431-b62f-9e9fef4b5827
title: S (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f33f4d2c16110ad6c79a02401c6a63ad0fb8f4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810996"
---
# <a name="s-telephony-api"></a><span data-ttu-id="343c6-103">S (API de telefonia)</span><span class="sxs-lookup"><span data-stu-id="343c6-103">S (Telephony API)</span></span>

<span data-ttu-id="343c6-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [i](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) S [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="343c6-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) S [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="343c6-105"><span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**provedor de serviços**</span><span class="sxs-lookup"><span data-stu-id="343c6-105"><span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**service provider**</span></span>
</dt> <dd>

<span data-ttu-id="343c6-106">Uma biblioteca de vínculo dinâmico que dá suporte a comunicações por meio de uma rede telefônica por meio de um conjunto de funções de serviço exportadas.</span><span class="sxs-lookup"><span data-stu-id="343c6-106">A dynamic-link library that supports communications over a telephone network through a set of exported service functions.</span></span> <span data-ttu-id="343c6-107">O provedor de serviços responde às solicitações de telefonia, enviadas a ela pela biblioteca de vínculo dinâmico TAPI, realizando as tarefas de baixo nível necessárias para se comunicar pela rede telefônica.</span><span class="sxs-lookup"><span data-stu-id="343c6-107">The service provider responds to telephony requests, sent to it by the TAPI dynamic-link library, by carrying out the low-level tasks necessary to communicate over the telephone network.</span></span> <span data-ttu-id="343c6-108">Dessa forma, o provedor de serviços, em conjunto com a TAPI, protege os aplicativos dos detalhes dependentes do serviço e da tecnologia da comunicação de rede do telefone.</span><span class="sxs-lookup"><span data-stu-id="343c6-108">In this way, the service provider, in conjunction with TAPI, shields applications from the service- and technology-dependent details of the telephone network communication.</span></span>

</dd> <dt>

<span data-ttu-id="343c6-109"><span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**Subendereço**</span><span class="sxs-lookup"><span data-stu-id="343c6-109"><span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**subaddressing**</span></span>
</dt> <dd>

<span data-ttu-id="343c6-110">Um recurso fornecido em linhas ISDN que permite mais informações do que apenas um único número de telefone a ser usado durante a discagem.</span><span class="sxs-lookup"><span data-stu-id="343c6-110">A capability provided on ISDN lines that allows more information than just a single telephone number to be used when dialing.</span></span>

</dd> <dt>

<span data-ttu-id="343c6-111"><span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**Telefonia suplementar**</span><span class="sxs-lookup"><span data-stu-id="343c6-111"><span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**Supplementary Telephony**</span></span>
</dt> <dd>

<span data-ttu-id="343c6-112">Nível de serviço que fornece recursos de comutador avançados, como retenção, transferência e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="343c6-112">Level of service that provides advanced switch features such as hold, transfer, and so on.</span></span> <span data-ttu-id="343c6-113">Todos os serviços complementares são opcionais; ou seja, o provedor de serviços não precisa dar suporte a eles.</span><span class="sxs-lookup"><span data-stu-id="343c6-113">All supplementary services are optional; that is, the service provider is not required to support them.</span></span> <span data-ttu-id="343c6-114">Confira telefonia [*assistida*](a-tapgloss.md), telefonia [*básica*](b-tapgloss.md), [*telefonia estendida*](e-tapgloss.md#tapi2.extended_telephony_tapgloss).</span><span class="sxs-lookup"><span data-stu-id="343c6-114">See [*Assisted Telephony*](a-tapgloss.md), [*Basic Telephony*](b-tapgloss.md), [*Extended Telephony*](e-tapgloss.md#tapi2.extended_telephony_tapgloss).</span></span>

</dd> <dt>

<span data-ttu-id="343c6-115"><span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**56 comutados**</span><span class="sxs-lookup"><span data-stu-id="343c6-115"><span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**Switched 56**</span></span>
</dt> <dd>

<span data-ttu-id="343c6-116">Um serviço de dados alternado que permite ao usuário discar outra pessoa e transmitir em full duplex, digital síncrono 56 Kbps pelo preço de uma chamada telefônica.</span><span class="sxs-lookup"><span data-stu-id="343c6-116">A switched data service that lets the user dial someone else and transmit at full duplex, digital synchronous 56 Kbps for the price of a phone call.</span></span>

</dd> <dt>

<span data-ttu-id="343c6-117"><span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**replicação**</span><span class="sxs-lookup"><span data-stu-id="343c6-117"><span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**synchronous**</span></span>
</dt> <dd>

<span data-ttu-id="343c6-118">Método de transmissão de dados no qual há tempo constante entre bits, caracteres ou eventos sucessivos.</span><span class="sxs-lookup"><span data-stu-id="343c6-118">Data transmission method in which there is constant time between successive bits, characters, or events.</span></span> <span data-ttu-id="343c6-119">O tempo é obtido pelo compartilhamento de um único relógio.</span><span class="sxs-lookup"><span data-stu-id="343c6-119">The timing is achieved by the sharing of a single clock.</span></span> <span data-ttu-id="343c6-120">Cada extremidade da transmissão se sincroniza com o uso de relógios e informações enviadas junto com os dados transmitidos.</span><span class="sxs-lookup"><span data-stu-id="343c6-120">Each end of the transmission synchronizes itself with the use of clocks and information sent along with the transmitted data.</span></span> <span data-ttu-id="343c6-121">Os caracteres são espaçados por tempo, não por bits de início e de parada.</span><span class="sxs-lookup"><span data-stu-id="343c6-121">Characters are spaced by time, not by start and stop bits.</span></span> <span data-ttu-id="343c6-122">Consulte [*assíncrono*](a-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="343c6-122">See [*asynchronous*](a-tapgloss.md).</span></span>

</dd> </dl>

 

 



