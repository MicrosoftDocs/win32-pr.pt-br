---
description: 'Saiba mais sobre: OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf6294c3f1d90ac8a2292c65b3c1b8558e69220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793618"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a><span data-ttu-id="e489e-103">os OPM \_ Get \_ ACP \_ e \_ CGMSA \_ Signaling</span><span class="sxs-lookup"><span data-stu-id="e489e-103">OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>

<span data-ttu-id="e489e-104">Retorna as seguintes informações sobre uma saída de vídeo:</span><span class="sxs-lookup"><span data-stu-id="e489e-104">Returns the following information about a video output:</span></span>

-   <span data-ttu-id="e489e-105">Uma lista de padrões de proteção de televisão com suporte pelo driver.</span><span class="sxs-lookup"><span data-stu-id="e489e-105">A list of television protection standards supported by the driver.</span></span>
-   <span data-ttu-id="e489e-106">O padrão que está ativo no momento.</span><span class="sxs-lookup"><span data-stu-id="e489e-106">The standard that is currently active.</span></span>
-   <span data-ttu-id="e489e-107">A taxa de proporção atual ou outros dados de sinalização.</span><span class="sxs-lookup"><span data-stu-id="e489e-107">The current aspect ratio or other signaling data.</span></span>



| <span data-ttu-id="e489e-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="e489e-108">Requirement</span></span> | <span data-ttu-id="e489e-109">Valor</span><span class="sxs-lookup"><span data-stu-id="e489e-109">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e489e-110">GUID de solicitação</span><span class="sxs-lookup"><span data-stu-id="e489e-110">Request GUID</span></span> | <span data-ttu-id="e489e-111">os OPM \_ Get \_ ACP \_ e \_ CGMSA \_ Signaling</span><span class="sxs-lookup"><span data-stu-id="e489e-111">OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>                                                |
| <span data-ttu-id="e489e-112">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="e489e-112">Input data</span></span>   | <span data-ttu-id="e489e-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e489e-113">None</span></span>                                                                                |
| <span data-ttu-id="e489e-114">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="e489e-114">Return data</span></span>  | <span data-ttu-id="e489e-115">Uma estrutura de [**\_ \_ \_ \_ sinalização de erro OPM e CGMSA**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)</span><span class="sxs-lookup"><span data-stu-id="e489e-115">An [**OPM\_ACP\_AND\_CGMSA\_SIGNALING**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e489e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e489e-116">Remarks</span></span>

<span data-ttu-id="e489e-117">Essa consulta é equivalente à consulta DXVA \_ COPPQuerySignaling usada no protocolo de proteção de saída certificado (Copp).</span><span class="sxs-lookup"><span data-stu-id="e489e-117">This query is equivalent to the DXVA\_COPPQuerySignaling query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="e489e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e489e-118">Requirements</span></span>



| <span data-ttu-id="e489e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e489e-119">Requirement</span></span> | <span data-ttu-id="e489e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e489e-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e489e-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e489e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e489e-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e489e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e489e-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e489e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e489e-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e489e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e489e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e489e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e489e-126"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e489e-126"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e489e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e489e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e489e-128">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="e489e-128">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="e489e-129">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="e489e-129">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="e489e-130">Solicitações de status OPM</span><span class="sxs-lookup"><span data-stu-id="e489e-130">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




