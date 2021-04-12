---
description: Retorna uma descrição do sinal de vídeo que está sendo transmitido pelo conector.
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: OPM_GET_ACTUAL_OUTPUT_FORMAT (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eeca9bcf8fde670447afe4268a86ffa31b6a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296533"
---
# <a name="opm_get_actual_output_format"></a><span data-ttu-id="68fe9-103">formato de saída de OPM de \_ obtenção \_ real \_ \_</span><span class="sxs-lookup"><span data-stu-id="68fe9-103">OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT</span></span>

<span data-ttu-id="68fe9-104">Retorna uma descrição do sinal de vídeo que está sendo transmitido pelo conector.</span><span class="sxs-lookup"><span data-stu-id="68fe9-104">Returns a description of the video signal that is being transmitted over the connector.</span></span>



| <span data-ttu-id="68fe9-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="68fe9-105">Requirement</span></span> | <span data-ttu-id="68fe9-106">Valor</span><span class="sxs-lookup"><span data-stu-id="68fe9-106">Value</span></span> |
|--------------|------------------------------------------------------------------------------|
| <span data-ttu-id="68fe9-107">GUID de solicitação</span><span class="sxs-lookup"><span data-stu-id="68fe9-107">Request GUID</span></span> | <span data-ttu-id="68fe9-108">formato de saída de OPM de \_ obtenção \_ real \_ \_</span><span class="sxs-lookup"><span data-stu-id="68fe9-108">OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT</span></span>                                             |
| <span data-ttu-id="68fe9-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="68fe9-109">Input data</span></span>   | <span data-ttu-id="68fe9-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="68fe9-110">None</span></span>                                                                         |
| <span data-ttu-id="68fe9-111">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="68fe9-111">Return data</span></span>  | <span data-ttu-id="68fe9-112">Uma estrutura de [**\_ formato de \_ saída \_ de OPM real**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)</span><span class="sxs-lookup"><span data-stu-id="68fe9-112">An [**OPM\_ACTUAL\_OUTPUT\_FORMAT**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="68fe9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="68fe9-113">Remarks</span></span>

<span data-ttu-id="68fe9-114">O sinal de vídeo transmitido pelo conector não necessariamente tem o mesmo formato que o modo de exibição da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="68fe9-114">The video signal that is transmitted over the connector does not necessarily have the same format as the desktop display mode.</span></span> <span data-ttu-id="68fe9-115">Por exemplo, o modo de exibição de área de trabalho pode ser 1024 x 768 pixels às 85 Hz, enquanto o conector pode ser um conector de S-video que transmite um sinal de vídeo em 720 x 480 pixels, 60/1.01 Hz entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="68fe9-115">For example, the desktop display mode might be 1024 x 768 pixels at 85 Hz, while the connector might be an S-Video connector that transmits a video signal at 720 x 480 pixels, 60/1.01 Hz interlaced.</span></span> <span data-ttu-id="68fe9-116">Nesse caso, o driver retornaria a resolução do sinal S-Video, não a resolução da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="68fe9-116">In that case, the driver would return the resolution of the S-Video signal, not the desktop resolution.</span></span>

<span data-ttu-id="68fe9-117">Essa consulta é equivalente à consulta DXVA \_ COPPQueryDisplayData usada no protocolo de proteção de saída certificado (Copp).</span><span class="sxs-lookup"><span data-stu-id="68fe9-117">This query is equivalent to the DXVA\_COPPQueryDisplayData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="68fe9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68fe9-118">Requirements</span></span>



| <span data-ttu-id="68fe9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="68fe9-119">Requirement</span></span> | <span data-ttu-id="68fe9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="68fe9-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="68fe9-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68fe9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="68fe9-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68fe9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="68fe9-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68fe9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="68fe9-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68fe9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="68fe9-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68fe9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="68fe9-126"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="68fe9-126"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68fe9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="68fe9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68fe9-128">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="68fe9-128">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="68fe9-129">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="68fe9-129">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="68fe9-130">Solicitações de status OPM</span><span class="sxs-lookup"><span data-stu-id="68fe9-130">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




