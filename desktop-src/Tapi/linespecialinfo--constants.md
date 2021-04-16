---
description: As \_ constantes de sinalizador de bit LINESPECIALINFO descrevem os sinais de informações especiais que a rede pode usar para relatar várias operações de observação de rede e relatórios.
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: Constantes de LINESPECIALINFO_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78154757515ebd5bfa36778795c26ef9fdc96db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757616"
---
# <a name="linespecialinfo_-constants"></a><span data-ttu-id="82ce3-103">\_Constantes LINESPECIALINFO</span><span class="sxs-lookup"><span data-stu-id="82ce3-103">LINESPECIALINFO\_ Constants</span></span>

<span data-ttu-id="82ce3-104">As constantes de sinalizador de bit **LINESPECIALINFO \_** descrevem os sinais de informações especiais que a rede pode usar para relatar várias operações de observação de rede e relatórios.</span><span class="sxs-lookup"><span data-stu-id="82ce3-104">The **LINESPECIALINFO\_** bit-flag constants describes special information signals that the network can use to report various reporting and network observation operations.</span></span> <span data-ttu-id="82ce3-105">Elas são sequências de tons codificadas especiais transmitidas no início dos comunicados gravados do comunicado de rede.</span><span class="sxs-lookup"><span data-stu-id="82ce3-105">They are special coded tone sequences transmitted at the beginning of network advisory recorded announcements.</span></span>

<dl> <dt>

<span data-ttu-id="82ce3-106"><span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO \_ CUSTIRREG**</span><span class="sxs-lookup"><span data-stu-id="82ce3-106"><span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO\_CUSTIRREG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="82ce3-107">Esse tom de informação especial precede um número vago, AIS, Centrex de alteração de número e estação de trabalho, código de acesso não discado ou discado com erro ou mensagem do operador de interceptação manual (categoria de irregularidade do cliente).</span><span class="sxs-lookup"><span data-stu-id="82ce3-107">This special information tone precedes a vacant number, AIS, Centrex number change and nonworking station, access code not dialed or dialed in error, or manual intercept operator message (customer irregularity category).</span></span> <span data-ttu-id="82ce3-108">LINESPECIALINFO \_ CUSTIRREG também é relatado quando as informações de cobrança são rejeitadas e quando o endereço discado é bloqueado no comutador.</span><span class="sxs-lookup"><span data-stu-id="82ce3-108">LINESPECIALINFO\_CUSTIRREG is also reported when billing information is rejected and when the dialed address is blocked at the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="82ce3-109"><span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO \_ NOcircuit**</span><span class="sxs-lookup"><span data-stu-id="82ce3-109"><span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO\_NOCIRCUIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="82ce3-110">Esse tom de informações especiais precede um circuito de não ou um comunicado de emergência (categoria de bloqueio de tronco).</span><span class="sxs-lookup"><span data-stu-id="82ce3-110">This special information tone precedes a no circuit or an emergency announcement (trunk blockage category).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="82ce3-111"><span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**\_REordenar LINESPECIALINFO**</span><span class="sxs-lookup"><span data-stu-id="82ce3-111"><span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**LINESPECIALINFO\_REORDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="82ce3-112">Esse tom de informação especial precede um anúncio de reordenação (categoria de irregularização de equipamentos).</span><span class="sxs-lookup"><span data-stu-id="82ce3-112">This special information tone precedes a reorder announcement (equipment irregularity category).</span></span> <span data-ttu-id="82ce3-113">\_A REordenação LINESPECIALINFO também é relatada quando o telefone é mantido offhook muito longo.</span><span class="sxs-lookup"><span data-stu-id="82ce3-113">LINESPECIALINFO\_REORDER is also reported when the telephone is kept offhook too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="82ce3-114"><span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO não \_ disp.**</span><span class="sxs-lookup"><span data-stu-id="82ce3-114"><span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="82ce3-115">As especificidades sobre o tom de informações especiais não estão disponíveis e não se tornarão conhecidas.</span><span class="sxs-lookup"><span data-stu-id="82ce3-115">Specifics about the special information tone are unavailable and will not become known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="82ce3-116"><span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="82ce3-116"><span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="82ce3-117">As especificidades sobre o tom de informações especiais são desconhecidas no momento, mas podem ser conhecidas mais tarde.</span><span class="sxs-lookup"><span data-stu-id="82ce3-117">Specifics about the special information tone are currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82ce3-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="82ce3-118">Remarks</span></span>

<span data-ttu-id="82ce3-119">Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82ce3-119">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="82ce3-120">Os 16 bits de ordem inferior são reservados.</span><span class="sxs-lookup"><span data-stu-id="82ce3-120">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="82ce3-121">Os tons de informação especiais são definidos para mensagens de consultoria e não são normalmente usados para cobrança ou finalidade de supervisão.</span><span class="sxs-lookup"><span data-stu-id="82ce3-121">Special information tones are defined for advisory messages and are not normally used for billing or supervisory purpose.</span></span>

## <a name="requirements"></a><span data-ttu-id="82ce3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82ce3-122">Requirements</span></span>



| <span data-ttu-id="82ce3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="82ce3-123">Requirement</span></span> | <span data-ttu-id="82ce3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="82ce3-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="82ce3-125">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="82ce3-125">TAPI version</span></span><br/> | <span data-ttu-id="82ce3-126">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="82ce3-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="82ce3-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82ce3-127">Header</span></span><br/>       | <dl> <span data-ttu-id="82ce3-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="82ce3-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




