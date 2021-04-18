---
description: As \_ constantes de sinalizador de bit LINECALLPARTYID descrevem a natureza das informações disponíveis sobre as partes envolvidas em uma chamada.
ms.assetid: e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db
title: Constantes de LINECALLPARTYID_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5dd8cca75fe6e91b97fac63dca6c0fdda554394
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813056"
---
# <a name="linecallpartyid_-constants"></a><span data-ttu-id="ce331-103">\_Constantes LINECALLPARTYID</span><span class="sxs-lookup"><span data-stu-id="ce331-103">LINECALLPARTYID\_ Constants</span></span>

<span data-ttu-id="ce331-104">As constantes de sinalizador de bit **LINECALLPARTYID \_** descrevem a natureza das informações disponíveis sobre as partes envolvidas em uma chamada.</span><span class="sxs-lookup"><span data-stu-id="ce331-104">The **LINECALLPARTYID\_** bit-flag constants describe the nature of the information available about the parties involved in a call.</span></span>

<dl> <dt>

<span data-ttu-id="ce331-105"><span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**\_endereço LINECALLPARTYID**</span><span class="sxs-lookup"><span data-stu-id="ce331-105"><span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**LINECALLPARTYID\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ce331-106">As informações de identificador de terceiros consistem no endereço da parte em formato de endereço canônico ou formato de endereço de discagem.</span><span class="sxs-lookup"><span data-stu-id="ce331-106">Party identifier information consists of the party's address in either canonical address format or dialable address format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce331-107"><span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="ce331-107"><span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ce331-108">As informações de identificador de terceiros não estão disponíveis porque foram bloqueadas pela parte remota.</span><span class="sxs-lookup"><span data-stu-id="ce331-108">Party identifier information is not available because it has been blocked by the remote party.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce331-109"><span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**nome do LINECALLPARTYID \_**</span><span class="sxs-lookup"><span data-stu-id="ce331-109"><span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**LINECALLPARTYID\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ce331-110">As informações de identificador de terceiros consistem no nome da parte (como, por exemplo, de um diretório mantido dentro do comutador).</span><span class="sxs-lookup"><span data-stu-id="ce331-110">Party identifier information consists of the party's name (as, for example, from a directory kept inside the switch).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce331-111"><span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID \_ OUTOFAREA**</span><span class="sxs-lookup"><span data-stu-id="ce331-111"><span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID\_OUTOFAREA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ce331-112">As informações de ID do chamador para a chamada não estão disponíveis porque não são propagadas por meio da rede.</span><span class="sxs-lookup"><span data-stu-id="ce331-112">Caller ID information for the call is not available because it is not propagated all the way by the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce331-113"><span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID \_ parcial**</span><span class="sxs-lookup"><span data-stu-id="ce331-113"><span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ce331-114">As informações de identificador de terceiros são válidas, mas são limitadas apenas a informações parciais.</span><span class="sxs-lookup"><span data-stu-id="ce331-114">Party identifier information is valid but it is limited to partial information only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce331-115"><span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID não \_ disp.**</span><span class="sxs-lookup"><span data-stu-id="ce331-115"><span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ce331-116">As informações do identificador da parte não estão disponíveis e não serão disponibilizadas mais tarde.</span><span class="sxs-lookup"><span data-stu-id="ce331-116">Party identifier information is not available and will not become available later.</span></span> <span data-ttu-id="ce331-117">As informações podem estar indisponíveis por motivos não especificados.</span><span class="sxs-lookup"><span data-stu-id="ce331-117">Information may be unavailable for unspecified reasons.</span></span> <span data-ttu-id="ce331-118">Por exemplo, as informações não foram entregues pela rede, elas foram ignoradas pelo provedor de serviços e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="ce331-118">For example, the information was not delivered by the network, it was ignored by the service provider, and so forth.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce331-119"><span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="ce331-119"><span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ce331-120">As informações de identificador de terceiros atualmente são desconhecidas, mas podem se tornar conhecidas mais tarde.</span><span class="sxs-lookup"><span data-stu-id="ce331-120">Party identifier information is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce331-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce331-121">Remarks</span></span>

<span data-ttu-id="ce331-122">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="ce331-122">No extensibility.</span></span> <span data-ttu-id="ce331-123">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="ce331-123">All 32 bits are reserved.</span></span>

<span data-ttu-id="ce331-124">Para cada uma das partes possíveis envolvidas em uma chamada, as **constantes \_ LINECALLPARTYID** descrevem como as informações do identificador da parte são formatadas.</span><span class="sxs-lookup"><span data-stu-id="ce331-124">For each of the possible parties involved in a call, the **LINECALLPARTYID\_** constants describe how the party identifier information is formatted.</span></span> <span data-ttu-id="ce331-125">Essas informações são fornecidas na estrutura de dados [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="ce331-125">This information is supplied in the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce331-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce331-126">Requirements</span></span>



| <span data-ttu-id="ce331-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce331-127">Requirement</span></span> | <span data-ttu-id="ce331-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ce331-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ce331-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="ce331-129">TAPI version</span></span><br/> | <span data-ttu-id="ce331-130">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ce331-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ce331-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce331-131">Header</span></span><br/>       | <dl> <span data-ttu-id="ce331-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce331-132"><dt>Tapi.h</dt></span></span> </dl> |



 

 




