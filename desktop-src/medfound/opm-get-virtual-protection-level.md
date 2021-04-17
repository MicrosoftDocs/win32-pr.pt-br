---
description: Retorna o nível de proteção virtual para um mecanismo de proteção especificado.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7ac36abd0a043a74a18401205bbb5e661ac17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813334"
---
# <a name="opm_get_virtual_protection_level"></a><span data-ttu-id="d1e4f-103">OPM \_ obter \_ \_ nível de proteção virtual \_</span><span class="sxs-lookup"><span data-stu-id="d1e4f-103">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="d1e4f-104">Retorna o nível de proteção virtual para um mecanismo de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="d1e4f-104">Returns the virtual protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="d1e4f-105">O nível de proteção *virtual* é o nível solicitado pelo aplicativo durante a sessão do Gerenciador de proteção de saída (OPM) atual.</span><span class="sxs-lookup"><span data-stu-id="d1e4f-105">The *virtual* protection level is the level requested by the application during the current Output Protection Manager (OPM) session.</span></span> <span data-ttu-id="d1e4f-106">O driver pode aplicar um nível mais alto, devido a eventos fora dessa sessão OPM.</span><span class="sxs-lookup"><span data-stu-id="d1e4f-106">The driver might apply a higher level, due to events outside of this OPM session.</span></span> <span data-ttu-id="d1e4f-107">Para localizar o nível de proteção real que está em vigor, envie a consulta de [**\_ \_ \_ \_ nível de proteção OPM**](opm-get-actual-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e4f-107">To find the actual protection level that is in effect, send the [**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**](opm-get-actual-protection-level.md) query.</span></span>



| <span data-ttu-id="d1e4f-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1e4f-108">Requirement</span></span> | <span data-ttu-id="d1e4f-109">Valor</span><span class="sxs-lookup"><span data-stu-id="d1e4f-109">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e4f-110">GUID de solicitação</span><span class="sxs-lookup"><span data-stu-id="d1e4f-110">Request GUID</span></span> | <span data-ttu-id="d1e4f-111">OPM \_ obter \_ \_ nível de proteção virtual \_</span><span class="sxs-lookup"><span data-stu-id="d1e4f-111">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>                                                                                                                                          |
| <span data-ttu-id="d1e4f-112">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="d1e4f-112">Input data</span></span>   | <span data-ttu-id="d1e4f-113">O mecanismo de proteção a ser consultado, especificado como um inteiro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d1e4f-113">The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="d1e4f-114">O valor é interpretado como um membro dos [**sinalizadores de tipo de proteção OPM**](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d1e4f-114">The value is interpreted as a member of the [**OPM Protection Type Flags**](opm-protection-type-flags.md).</span></span> |
| <span data-ttu-id="d1e4f-115">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="d1e4f-115">Return data</span></span>  | <span data-ttu-id="d1e4f-116">Uma estrutura de [**\_ \_ informações de OPM padrão**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="d1e4f-116">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span>                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="d1e4f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1e4f-117">Remarks</span></span>

<span data-ttu-id="d1e4f-118">O nível de proteção é retornado no membro **ulInformation** da estrutura [**de \_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="d1e4f-118">The protection level is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="d1e4f-119">O significado desse valor depende do mecanismo de proteção que é consultado.</span><span class="sxs-lookup"><span data-stu-id="d1e4f-119">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="d1e4f-120">Para cada mecanismo de proteção, o valor de **ulInformation** é um sinalizador de uma enumeração diferente, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1e4f-120">For each protection mechanism, the value of **ulInformation** is a flag from a different enumeration, as shown in the following table.</span></span>



| <span data-ttu-id="d1e4f-121">Mecanismo de proteção</span><span class="sxs-lookup"><span data-stu-id="d1e4f-121">Protection mechanism</span></span> | <span data-ttu-id="d1e4f-122">Enumeração</span><span class="sxs-lookup"><span data-stu-id="d1e4f-122">Enumeration</span></span>                                                       |
|----------------------|-------------------------------------------------------------------|
| <span data-ttu-id="d1e4f-123">ACP</span><span class="sxs-lookup"><span data-stu-id="d1e4f-123">ACP</span></span>                  | [<span data-ttu-id="d1e4f-124">**nível de proteção do OPM \_ ACP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d1e4f-124">**OPM\_ACP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| <span data-ttu-id="d1e4f-125">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="d1e4f-125">CGMS-A</span></span>               | [<span data-ttu-id="d1e4f-126">**CGMS-um sinalizador de proteção**</span><span class="sxs-lookup"><span data-stu-id="d1e4f-126">**CGMS-A Protection Flags**</span></span>](cgms-a-protection-flags.md)        |
| <span data-ttu-id="d1e4f-127">DPCP</span><span class="sxs-lookup"><span data-stu-id="d1e4f-127">DPCP</span></span>                 | [<span data-ttu-id="d1e4f-128">**\_nível de \_ proteção OPM DPCP \_**</span><span class="sxs-lookup"><span data-stu-id="d1e4f-128">**OPM\_DPCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| <span data-ttu-id="d1e4f-129">HDCP</span><span class="sxs-lookup"><span data-stu-id="d1e4f-129">HDCP</span></span>                 | [<span data-ttu-id="d1e4f-130">**\_nível de \_ proteção de HDCP de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="d1e4f-130">**OPM\_HDCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

<span data-ttu-id="d1e4f-131">Essa consulta é equivalente à consulta DXVA \_ COPPQueryLocalProtectionLevel usada no protocolo de proteção de saída certificado (Copp).</span><span class="sxs-lookup"><span data-stu-id="d1e4f-131">This query is equivalent to the DXVA\_COPPQueryLocalProtectionLevel query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1e4f-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1e4f-132">Requirements</span></span>



| <span data-ttu-id="d1e4f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1e4f-133">Requirement</span></span> | <span data-ttu-id="d1e4f-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d1e4f-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e4f-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1e4f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d1e4f-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1e4f-136">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d1e4f-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1e4f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d1e4f-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d1e4f-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d1e4f-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1e4f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1e4f-140"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1e4f-140"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1e4f-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1e4f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e4f-142">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="d1e4f-142">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="d1e4f-143">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="d1e4f-143">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="d1e4f-144">Solicitações de status OPM</span><span class="sxs-lookup"><span data-stu-id="d1e4f-144">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




