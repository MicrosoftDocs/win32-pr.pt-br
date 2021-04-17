---
description: Os termos a seguir são úteis para entender a tecnologia TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 23331332-38bc-41b9-84c4-281722ddf563
title: C (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c6fade540235ef6c68b42a0aba364038d674e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780611"
---
# <a name="c-telephony-api"></a><span data-ttu-id="c68b8-103">C (API de telefonia)</span><span class="sxs-lookup"><span data-stu-id="c68b8-103">C (Telephony API)</span></span>

<span data-ttu-id="c68b8-104">[A](a-tapgloss.md) [B](b-tapgloss.md) C [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [i](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="c68b8-104">[A](a-tapgloss.md) [B](b-tapgloss.md) C [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="c68b8-105"><span id="tapi2.call_classification_tapgloss"></span><span id="TAPI2.CALL_CLASSIFICATION_TAPGLOSS"></span>**classificação de chamada**</span><span class="sxs-lookup"><span data-stu-id="c68b8-105"><span id="tapi2.call_classification_tapgloss"></span><span id="TAPI2.CALL_CLASSIFICATION_TAPGLOSS"></span>**call classification**</span></span>
</dt> <dd>

<span data-ttu-id="c68b8-106">Processo TAPI que relata alterações no tipo de fluxo de mídia (voz, fax, modem de dados e assim por diante) para aplicativos participantes.</span><span class="sxs-lookup"><span data-stu-id="c68b8-106">TAPI process that reports changes in the type of media stream (voice, fax, data modem, and so on) to participating applications.</span></span>

</dd> <dt>

<span data-ttu-id="c68b8-107"><span id="tapi2.call_progress_monitoring_tapgloss"></span><span id="TAPI2.CALL_PROGRESS_MONITORING_TAPGLOSS"></span>**monitoramento do andamento da chamada**</span><span class="sxs-lookup"><span data-stu-id="c68b8-107"><span id="tapi2.call_progress_monitoring_tapgloss"></span><span id="TAPI2.CALL_PROGRESS_MONITORING_TAPGLOSS"></span>**call progress monitoring**</span></span>
</dt> <dd>

<span data-ttu-id="c68b8-108">O processo de escuta de tons audíveis, como um tom de discagem, tons de informações especiais, sinais ocupados e tons de toque para determinar o estado de uma chamada (seu progresso pela rede).</span><span class="sxs-lookup"><span data-stu-id="c68b8-108">The process of listening for audible tones such as a dial tone, special information tones, busy signals, and ringback tones to determine the state of a call (its progress through the network).</span></span>

</dd> <dt>

<span data-ttu-id="c68b8-109"><span id="tapi2.call_redirection_tapgloss"></span><span id="TAPI2.CALL_REDIRECTION_TAPGLOSS"></span>**redirecionamento de chamada**</span><span class="sxs-lookup"><span data-stu-id="c68b8-109"><span id="tapi2.call_redirection_tapgloss"></span><span id="TAPI2.CALL_REDIRECTION_TAPGLOSS"></span>**call redirection**</span></span>
</dt> <dd>

<span data-ttu-id="c68b8-110">Uma função que permite a um aplicativo desviar uma chamada de oferta para outro endereço sem primeiro responder à chamada.</span><span class="sxs-lookup"><span data-stu-id="c68b8-110">A function that allows an application to deflect an offering call to another address without first answering the call.</span></span> <span data-ttu-id="c68b8-111">O redirecionamento de chamada é diferente do encaminhamento de chamadas, pois o encaminhamento de chamadas é executado pelo switch sem o envolvimento do aplicativo; o redirecionamento pode ser feito em uma base chamada por chamada pelo aplicativo, por exemplo, orientado pelas informações de ID do chamador.</span><span class="sxs-lookup"><span data-stu-id="c68b8-111">Call redirection differs from call forwarding in that call forwarding is performed by the switch without the involvement of the application; redirection can be done on a call-by-call basis by the application, for example, driven by caller ID information.</span></span> <span data-ttu-id="c68b8-112">Ele difere da transferência de chamada no que a transferência de uma chamada exige que a chamada seja respondida primeiro.</span><span class="sxs-lookup"><span data-stu-id="c68b8-112">It differs from call transfer in that transferring a call requires that the call first be answered.</span></span> <span data-ttu-id="c68b8-113">Consulte *Call-ID*, *Caller-ID*, [*ID de redirecionamento*](r-tapgloss.md), [*ID de redirecionamento*](r-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="c68b8-113">See *called-ID*, *caller-ID*, [*redirecting ID*](r-tapgloss.md), [*redirection ID*](r-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="c68b8-114"><span id="tapi2.called_id_tapgloss"></span><span id="TAPI2.CALLED_ID_TAPGLOSS"></span>**ID de chamada**</span><span class="sxs-lookup"><span data-stu-id="c68b8-114"><span id="tapi2.called_id_tapgloss"></span><span id="TAPI2.CALLED_ID_TAPGLOSS"></span>**called-ID**</span></span>
</dt> <dd>

<span data-ttu-id="c68b8-115">Identifica o endereço de destino original de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="c68b8-115">Identifies the original destination address of a call.</span></span> <span data-ttu-id="c68b8-116">Consulte *redirecionamento de chamada*.</span><span class="sxs-lookup"><span data-stu-id="c68b8-116">See *call redirection*.</span></span>

</dd> <dt>

<span data-ttu-id="c68b8-117"><span id="tapi2.caller_id_tapgloss"></span><span id="TAPI2.CALLER_ID_TAPGLOSS"></span>**ID do chamador**</span><span class="sxs-lookup"><span data-stu-id="c68b8-117"><span id="tapi2.caller_id_tapgloss"></span><span id="TAPI2.CALLER_ID_TAPGLOSS"></span>**caller-ID**</span></span>
</dt> <dd>

<span data-ttu-id="c68b8-118">Identifica o endereço de origem de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="c68b8-118">Identifies the originating address of a call.</span></span> <span data-ttu-id="c68b8-119">Consulte *redirecionamento de chamada*.</span><span class="sxs-lookup"><span data-stu-id="c68b8-119">See *call redirection*.</span></span>

</dd> <dt>

<span data-ttu-id="c68b8-120"><span id="tapi2.central_office_tapgloss"></span><span id="TAPI2.CENTRAL_OFFICE_TAPGLOSS"></span>**escritório central**</span><span class="sxs-lookup"><span data-stu-id="c68b8-120"><span id="tapi2.central_office_tapgloss"></span><span id="TAPI2.CENTRAL_OFFICE_TAPGLOSS"></span>**central office**</span></span>
</dt> <dd>

<span data-ttu-id="c68b8-121">A instalação local da empresa telefônica que fornece serviço de telefone em uma área específica.</span><span class="sxs-lookup"><span data-stu-id="c68b8-121">Telephone company's local facility that provides telephone service in a specific area.</span></span> <span data-ttu-id="c68b8-122">Normalmente, as linhas dos assinantes são unidas a alternar equipamentos que conectam outros assinantes entre si, localmente e por longa distância.</span><span class="sxs-lookup"><span data-stu-id="c68b8-122">Typically, subscribers' lines are joined to switching equipment that connects other subscribers to each other, locally and over long distance.</span></span> <span data-ttu-id="c68b8-123">Também chamado de *co*.</span><span class="sxs-lookup"><span data-stu-id="c68b8-123">Also called *CO*.</span></span>

</dd> <dt>

<span data-ttu-id="c68b8-124"><span id="tapi2.centrex_tapgloss"></span><span id="TAPI2.CENTREX_TAPGLOSS"></span>**Centrex**</span><span class="sxs-lookup"><span data-stu-id="c68b8-124"><span id="tapi2.centrex_tapgloss"></span><span id="TAPI2.CENTREX_TAPGLOSS"></span>**Centrex**</span></span>
</dt> <dd>

<span data-ttu-id="c68b8-125">Um serviço de telefone comercial oferecido por uma empresa telefônica local de um escritório central local.</span><span class="sxs-lookup"><span data-stu-id="c68b8-125">A business telephone service offered by a local telephone company from a local, central office.</span></span>

</dd> <dt>

<span data-ttu-id="c68b8-126"><span id="tapi2.computer_centric_connection_tapgloss"></span><span id="TAPI2.COMPUTER_CENTRIC_CONNECTION_TAPGLOSS"></span>**conexão centrada em computador**</span><span class="sxs-lookup"><span data-stu-id="c68b8-126"><span id="tapi2.computer_centric_connection_tapgloss"></span><span id="TAPI2.COMPUTER_CENTRIC_CONNECTION_TAPGLOSS"></span>**computer-centric connection**</span></span>
</dt> <dd>

<span data-ttu-id="c68b8-127">Uma conexão que usa uma placa de suplemento do computador ou uma caixa externa que está conectada à rede de telefone e ao conjunto de telefone.</span><span class="sxs-lookup"><span data-stu-id="c68b8-127">A connection that uses a computer add-in card or external box that is connected to both the telephone network and the phone set.</span></span> <span data-ttu-id="c68b8-128">Compare [*a conexão centrada em telefone*](p-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="c68b8-128">Compare [*phone-centric connection*](p-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="c68b8-129"><span id="tapi2.connected_id_tapgloss"></span><span id="TAPI2.CONNECTED_ID_TAPGLOSS"></span>**ID conectada**</span><span class="sxs-lookup"><span data-stu-id="c68b8-129"><span id="tapi2.connected_id_tapgloss"></span><span id="TAPI2.CONNECTED_ID_TAPGLOSS"></span>**connected-ID**</span></span>
</dt> <dd>

<span data-ttu-id="c68b8-130">Identificador para a parte à qual a chamada foi realmente conectada.</span><span class="sxs-lookup"><span data-stu-id="c68b8-130">Identifier for the party to which the call was actually connected.</span></span> <span data-ttu-id="c68b8-131">Isso pode ser diferente da parte chamada se a chamada tiver sido divertida.</span><span class="sxs-lookup"><span data-stu-id="c68b8-131">This may be different from the called party if the call was diverted.</span></span>

</dd> </dl>

 

 



