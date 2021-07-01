---
description: Solicitações de status do OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Solicitações de status do OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf7338fe1309feb49fd191e3f4a1a22f3639b4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120171"
---
# <a name="opm-status-requests"></a><span data-ttu-id="caf44-103">Solicitações de status do OPM</span><span class="sxs-lookup"><span data-stu-id="caf44-103">OPM Status Requests</span></span>

<span data-ttu-id="caf44-104">Esta seção lista as solicitações de status disponíveis para o OPM (Gerenciador de Proteção de [Saída).](output-protection-manager.md)</span><span class="sxs-lookup"><span data-stu-id="caf44-104">This section lists the available status requests for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span> <span data-ttu-id="caf44-105">Para enviar uma solicitação de status do OPM, chame [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span><span class="sxs-lookup"><span data-stu-id="caf44-105">To send an OPM status request, call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span></span> <span data-ttu-id="caf44-106">Para cada solicitação, as informações a seguir são listadas.</span><span class="sxs-lookup"><span data-stu-id="caf44-106">For each request, the following information is listed.</span></span>



| <span data-ttu-id="caf44-107">Valor</span><span class="sxs-lookup"><span data-stu-id="caf44-107">Value</span></span>             | <span data-ttu-id="caf44-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="caf44-108">Description</span></span>                                                                                                                                                           |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caf44-109">GUID de solicitação</span><span class="sxs-lookup"><span data-stu-id="caf44-109">Request GUID</span></span> | <span data-ttu-id="caf44-110">Identifica a solicitação.</span><span class="sxs-lookup"><span data-stu-id="caf44-110">Identifies the request.</span></span> <span data-ttu-id="caf44-111">De definir **o membro guidSetting** da estrutura [**GET INFO \_ \_ \_ PARAMETERS do OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) igual a esse valor.</span><span class="sxs-lookup"><span data-stu-id="caf44-111">Set the **guidSetting** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="caf44-112">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="caf44-112">Input data</span></span>   | <span data-ttu-id="caf44-113">Especifica como interpretar a matriz **abParameters** na estrutura [**GET INFO \_ \_ \_ PARAMETERS do OPM.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)</span><span class="sxs-lookup"><span data-stu-id="caf44-113">Specifies how to interpret the **abParameters** array in the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure.</span></span>                      |
| <span data-ttu-id="caf44-114">Dados de saída</span><span class="sxs-lookup"><span data-stu-id="caf44-114">Output data</span></span>  | <span data-ttu-id="caf44-115">Especifica como interpretar a **matriz abRequestedInformation** na estrutura [**\_ OPM REQUESTED \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)</span><span class="sxs-lookup"><span data-stu-id="caf44-115">Specifies how to interpret the **abRequestedInformation** array in the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span>         |



 

<span data-ttu-id="caf44-116">As seguintes solicitações de status são definidas:</span><span class="sxs-lookup"><span data-stu-id="caf44-116">The following status requests are defined:</span></span>



| <span data-ttu-id="caf44-117">Solicitação de status</span><span class="sxs-lookup"><span data-stu-id="caf44-117">Status request</span></span>                                                                                      | <span data-ttu-id="caf44-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="caf44-118">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="caf44-119">**OPM \_ OBTER \_ SINALIZAÇÃO ACP \_ E \_ CGMSA \_**</span><span class="sxs-lookup"><span data-stu-id="caf44-119">**OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-get-acp-and-cgmsa-signaling.md)                     | <span data-ttu-id="caf44-120">Retorna as seguintes informações sobre uma saída de vídeo:</span><span class="sxs-lookup"><span data-stu-id="caf44-120">Returns the following information about a video output:</span></span>                                                                                               |
| [<span data-ttu-id="caf44-121">**OBTER FORMATO \_ \_ DE SAÍDA \_ \_ REAL DO OPM**</span><span class="sxs-lookup"><span data-stu-id="caf44-121">**OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT**</span></span>](opm-get-actual-output-format.md)                            | <span data-ttu-id="caf44-122">Retorna uma descrição do sinal de vídeo que está sendo transmitido pelo conector.</span><span class="sxs-lookup"><span data-stu-id="caf44-122">Returns a description of the video signal that is being transmitted over the connector.</span></span>                                                               |
| [<span data-ttu-id="caf44-123">**OBTER NÍVEL DE \_ \_ PROTEÇÃO REAL DO \_ OPM \_**</span><span class="sxs-lookup"><span data-stu-id="caf44-123">**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-actual-protection-level.md)                      | <span data-ttu-id="caf44-124">Retorna o nível de proteção global para um mecanismo de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="caf44-124">Returns the global protection level for a specified protection mechanism.</span></span>                                                                             |
| [<span data-ttu-id="caf44-125">**OBTER TIPO DE \_ \_ BARRAMENTO \_ DO ADAPTADOR \_ DO OPM**</span><span class="sxs-lookup"><span data-stu-id="caf44-125">**OPM\_GET\_ADAPTER\_BUS\_TYPE**</span></span>](opm-get-adapter-bus-type.md)                                    | <span data-ttu-id="caf44-126">Retorna o tipo de barramento de E/S usado pela saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="caf44-126">Returns the type of I/O bus used by the video output.</span></span>                                                                                                 |
| [<span data-ttu-id="caf44-127">**OBTER \_ INFORMAÇÕES \_ DO CODEC DO OPM \_**</span><span class="sxs-lookup"><span data-stu-id="caf44-127">**OPM\_GET\_CODEC\_INFO**</span></span>](opm-get-codec-info.md)                                                 | <span data-ttu-id="caf44-128">Obtém o valor de um codec de hardware.</span><span class="sxs-lookup"><span data-stu-id="caf44-128">Gets the merit value of a hardware codec.</span></span>                                                                                                             |
| [<span data-ttu-id="caf44-129">**OBTER INFORMAÇÕES DE \_ \_ DISPOSITIVO \_ HDCP \_ \_ CONECTADAS DO OPM**</span><span class="sxs-lookup"><span data-stu-id="caf44-129">**OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**</span></span>](opm-get-connected-hdcp-device-information.md) | <span data-ttu-id="caf44-130">Obtém informações sobre um High-Bandwidth HDCP (Proteção de Conteúdo digital) anexado à saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="caf44-130">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="caf44-131">As seguintes informações são retornadas:</span><span class="sxs-lookup"><span data-stu-id="caf44-131">The following information is returned:</span></span> |
| [<span data-ttu-id="caf44-132">**TIPO DE \_ CONECTOR GET \_ DO OPM \_**</span><span class="sxs-lookup"><span data-stu-id="caf44-132">**OPM\_GET\_CONNECTOR\_TYPE**</span></span>](opm-get-connector-type.md)                                         | <span data-ttu-id="caf44-133">Retorna o tipo de conector físico da saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="caf44-133">Returns the physical connector type of the video output.</span></span>                                                                                              |
| [<span data-ttu-id="caf44-134">**OBTER \_ A \_ VERSÃO ATUAL DO \_ \_ HDCP SRM \_ DO OPM**</span><span class="sxs-lookup"><span data-stu-id="caf44-134">**OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION**</span></span>](opm-get-current-hdcp-srm-version.md)                   | <span data-ttu-id="caf44-135">Retorna o número de versão da SRM (mensagem de renovação do sistema) usada atualmente pela saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="caf44-135">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>                                               |
| [<span data-ttu-id="caf44-136">**CARACTERÍSTICAS DO OPM \_ \_ GET \_ DVI**</span><span class="sxs-lookup"><span data-stu-id="caf44-136">**OPM\_GET\_DVI\_CHARACTERISTICS**</span></span>](opm-get-dvi-characteristics.md)                               | <span data-ttu-id="caf44-137">Consulta se um conector DVI (interface de vídeo digital) dá suporte à DVI versão 1.1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="caf44-137">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>                                                          |
| [<span data-ttu-id="caf44-138">**OPM \_ GET \_ OUTPUT \_ ID**</span><span class="sxs-lookup"><span data-stu-id="caf44-138">**OPM\_GET\_OUTPUT\_ID**</span></span>](opm-get-output-id.md)                                                   | <span data-ttu-id="caf44-139">Retorna o identificador exclusivo do monitor associado a esta saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="caf44-139">Returns the unique identifier of the monitor associated with this video output.</span></span>                                                                       |
| [<span data-ttu-id="caf44-140">**OBTER TIPOS \_ \_ DE PROTEÇÃO COM \_ \_ SUPORTE DO OPM**</span><span class="sxs-lookup"><span data-stu-id="caf44-140">**OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES**</span></span>](opm-get-supported-protection-types.md)                | <span data-ttu-id="caf44-141">Retorna a lista de mecanismos de proteção compatíveis com o conector.</span><span class="sxs-lookup"><span data-stu-id="caf44-141">Returns the list of protection mechanisms that are supported by the connector.</span></span>                                                                        |
| [<span data-ttu-id="caf44-142">**OBTER NÍVEL DE \_ \_ PROTEÇÃO VIRTUAL \_ DO OPM \_**</span><span class="sxs-lookup"><span data-stu-id="caf44-142">**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-virtual-protection-level.md)                    | <span data-ttu-id="caf44-143">Retorna o nível de proteção virtual para um mecanismo de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="caf44-143">Returns the virtual protection level for a specified protection mechanism.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="caf44-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="caf44-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caf44-145">Referência de programação do OPM</span><span class="sxs-lookup"><span data-stu-id="caf44-145">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="caf44-146">Gerenciador de Proteção de Saída</span><span class="sxs-lookup"><span data-stu-id="caf44-146">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



