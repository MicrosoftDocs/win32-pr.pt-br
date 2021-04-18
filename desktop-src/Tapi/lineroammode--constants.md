---
description: As \_ constantes de sinalizador de bit LINEROAMMODE descrevem o status de roaming de um dispositivo de linha.
ms.assetid: af0eb263-8deb-44ab-8acb-00e4ff7930ab
title: Constantes de LINEROAMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e40c40291567e7800b53070f882bf1e0bdac93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789452"
---
# <a name="lineroammode_-constants"></a><span data-ttu-id="90728-103">\_Constantes LINEROAMMODE</span><span class="sxs-lookup"><span data-stu-id="90728-103">LINEROAMMODE\_ Constants</span></span>

<span data-ttu-id="90728-104">As constantes de sinalizador de bit **LINEROAMMODE \_** descrevem o status de roaming de um dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="90728-104">The **LINEROAMMODE\_** bit-flag constants describe the roaming status of a line device.</span></span>

<dl> <dt>

<span data-ttu-id="90728-105"><span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**\_página inicial do LINEROAMMODE**</span><span class="sxs-lookup"><span data-stu-id="90728-105"><span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**LINEROAMMODE\_HOME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="90728-106">A linha está conectada ao nó da rede doméstica.</span><span class="sxs-lookup"><span data-stu-id="90728-106">The line is connected to the home network node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="90728-107"><span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**LINEROAMMODE \_ roama**</span><span class="sxs-lookup"><span data-stu-id="90728-107"><span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**LINEROAMMODE\_ROAMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="90728-108">A linha é conectada ao roam-uma transportadora e as chamadas são cobradas de acordo.</span><span class="sxs-lookup"><span data-stu-id="90728-108">The line is connected to the Roam-A carrier and calls are charged accordingly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="90728-109"><span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**LINEROAMMODE \_ ROAMB**</span><span class="sxs-lookup"><span data-stu-id="90728-109"><span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**LINEROAMMODE\_ROAMB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="90728-110">A linha é conectada à transportadora do roam-B e as chamadas são cobradas de acordo.</span><span class="sxs-lookup"><span data-stu-id="90728-110">The line is connected to the Roam-B carrier and calls are charged accordingly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="90728-111"><span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**LINEROAMMODE não \_ disp.**</span><span class="sxs-lookup"><span data-stu-id="90728-111"><span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**LINEROAMMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="90728-112">O modo de roaming não está disponível e não será conhecido.</span><span class="sxs-lookup"><span data-stu-id="90728-112">The roam mode is unavailable and will not be known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="90728-113"><span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**LINEROAMMODE \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="90728-113"><span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**LINEROAMMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="90728-114">O modo de roaming é desconhecido no momento, mas pode ser conhecido mais tarde.</span><span class="sxs-lookup"><span data-stu-id="90728-114">The roam mode is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90728-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="90728-115">Remarks</span></span>

<span data-ttu-id="90728-116">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="90728-116">No extensibility.</span></span> <span data-ttu-id="90728-117">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="90728-117">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="90728-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90728-118">Requirements</span></span>



| <span data-ttu-id="90728-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="90728-119">Requirement</span></span> | <span data-ttu-id="90728-120">Valor</span><span class="sxs-lookup"><span data-stu-id="90728-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="90728-121">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="90728-121">TAPI version</span></span><br/> | <span data-ttu-id="90728-122">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="90728-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="90728-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90728-123">Header</span></span><br/>       | <dl> <span data-ttu-id="90728-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="90728-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




