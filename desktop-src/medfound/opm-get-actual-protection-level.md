---
description: Retorna o nível de proteção global para um mecanismo de proteção especificado.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 960d704fd44ca779f128795b26603698bb0ad622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010663"
---
# <a name="opm_get_actual_protection_level"></a><span data-ttu-id="38dc9-103">nível de proteção do OPM \_ obter \_ real \_ \_</span><span class="sxs-lookup"><span data-stu-id="38dc9-103">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="38dc9-104">Retorna o nível de proteção global para um mecanismo de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="38dc9-104">Returns the global protection level for a specified protection mechanism.</span></span>



| <span data-ttu-id="38dc9-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="38dc9-105">Requirement</span></span> | <span data-ttu-id="38dc9-106">Valor</span><span class="sxs-lookup"><span data-stu-id="38dc9-106">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38dc9-107">GUID de solicitação</span><span class="sxs-lookup"><span data-stu-id="38dc9-107">Request GUID</span></span> | <span data-ttu-id="38dc9-108">nível de proteção do OPM \_ obter \_ real \_ \_</span><span class="sxs-lookup"><span data-stu-id="38dc9-108">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>                                                                                                                                       |
| <span data-ttu-id="38dc9-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="38dc9-109">Input data</span></span>   | <span data-ttu-id="38dc9-110">O mecanismo de proteção a ser consultado, especificado como um inteiro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="38dc9-110">The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="38dc9-111">O valor é interpretado como um membro dos [sinalizadores de tipo de proteção OPM](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="38dc9-111">The value is interpreted as a member of the [OPM Protection Type Flags](opm-protection-type-flags.md).</span></span> |
| <span data-ttu-id="38dc9-112">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="38dc9-112">Return data</span></span>  | <span data-ttu-id="38dc9-113">Uma estrutura de [**\_ \_ informações de OPM padrão**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="38dc9-113">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="38dc9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="38dc9-114">Remarks</span></span>

<span data-ttu-id="38dc9-115">O nível de proteção global é o nível de proteção que está sendo aplicado no conector, independentemente de como o driver de gráficos foi instruído a aplicar a proteção.</span><span class="sxs-lookup"><span data-stu-id="38dc9-115">The global protection level is the protection level that is currently being applied on the connector, regardless of how the graphics driver was instructed to apply the protection.</span></span> <span data-ttu-id="38dc9-116">Por exemplo, um aplicativo pode definir o nível de proteção de ACP chamando a função **ChangeDisplaySettingsEx** .</span><span class="sxs-lookup"><span data-stu-id="38dc9-116">For example, an application can set the ACP protection level by calling the **ChangeDisplaySettingsEx** function.</span></span> <span data-ttu-id="38dc9-117">Nesse caso, o nível de proteção global refletiria essa configuração, embora ela não tenha sido solicitada por meio do Gerenciador de proteção de saída (OPM).</span><span class="sxs-lookup"><span data-stu-id="38dc9-117">In that case, the global protection level would reflect this setting, even though it was not requested through Output Protection Manager (OPM).</span></span>

<span data-ttu-id="38dc9-118">O nível de proteção é retornado no membro **ulInformation** da estrutura [**de \_ \_ informações padrão OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="38dc9-118">The protection level is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="38dc9-119">O significado desse valor depende do mecanismo de proteção que é consultado.</span><span class="sxs-lookup"><span data-stu-id="38dc9-119">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="38dc9-120">Para cada mecanismo de proteção, o valor de **ulInformation** é um sinalizador de uma enumeração diferente, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="38dc9-120">For each protection mechanism, the value of **ulInformation** is a flag from a different enumeration, as shown in the following table.</span></span>



| <span data-ttu-id="38dc9-121">Mecanismo de proteção</span><span class="sxs-lookup"><span data-stu-id="38dc9-121">Protection mechanism</span></span> | <span data-ttu-id="38dc9-122">Enumeração</span><span class="sxs-lookup"><span data-stu-id="38dc9-122">Enumeration</span></span>                                                       |
|----------------------|-------------------------------------------------------------------|
| <span data-ttu-id="38dc9-123">ACP</span><span class="sxs-lookup"><span data-stu-id="38dc9-123">ACP</span></span>                  | [<span data-ttu-id="38dc9-124">**nível de proteção do OPM \_ ACP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="38dc9-124">**OPM\_ACP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| <span data-ttu-id="38dc9-125">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="38dc9-125">CGMS-A</span></span>               | [<span data-ttu-id="38dc9-126">CGMS-um sinalizador de proteção</span><span class="sxs-lookup"><span data-stu-id="38dc9-126">CGMS-A Protection Flags</span></span>](cgms-a-protection-flags.md)            |
| <span data-ttu-id="38dc9-127">DPCP</span><span class="sxs-lookup"><span data-stu-id="38dc9-127">DPCP</span></span>                 | [<span data-ttu-id="38dc9-128">**\_nível de \_ proteção OPM DPCP \_**</span><span class="sxs-lookup"><span data-stu-id="38dc9-128">**OPM\_DPCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| <span data-ttu-id="38dc9-129">HDCP</span><span class="sxs-lookup"><span data-stu-id="38dc9-129">HDCP</span></span>                 | [<span data-ttu-id="38dc9-130">**\_nível de \_ proteção de HDCP de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="38dc9-130">**OPM\_HDCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

<span data-ttu-id="38dc9-131">Essa consulta é equivalente à consulta DXVA \_ COPPQueryGlobalProtectionLevel usada no protocolo de proteção de saída certificado (Copp).</span><span class="sxs-lookup"><span data-stu-id="38dc9-131">This query is equivalent to the DXVA\_COPPQueryGlobalProtectionLevel query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="38dc9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38dc9-132">Requirements</span></span>



| <span data-ttu-id="38dc9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="38dc9-133">Requirement</span></span> | <span data-ttu-id="38dc9-134">Valor</span><span class="sxs-lookup"><span data-stu-id="38dc9-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="38dc9-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38dc9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="38dc9-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38dc9-136">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="38dc9-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38dc9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="38dc9-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="38dc9-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="38dc9-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38dc9-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="38dc9-140"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="38dc9-140"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38dc9-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="38dc9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38dc9-142">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="38dc9-142">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="38dc9-143">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="38dc9-143">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="38dc9-144">Solicitações de status OPM</span><span class="sxs-lookup"><span data-stu-id="38dc9-144">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




