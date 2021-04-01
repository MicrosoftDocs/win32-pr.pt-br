---
description: Solicitações de status OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Solicitações de status OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd994d7cb8d43db23fe59352dba830e741b74b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661485"
---
# <a name="opm-status-requests"></a><span data-ttu-id="8e914-103">Solicitações de status OPM</span><span class="sxs-lookup"><span data-stu-id="8e914-103">OPM Status Requests</span></span>

<span data-ttu-id="8e914-104">Esta seção lista as solicitações de status disponíveis para o [Gerenciador de proteção de saída](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="8e914-104">This section lists the available status requests for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span> <span data-ttu-id="8e914-105">Para enviar uma solicitação de status OPM, chame [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span><span class="sxs-lookup"><span data-stu-id="8e914-105">To send an OPM status request, call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span></span> <span data-ttu-id="8e914-106">Para cada solicitação, as informações a seguir são listadas.</span><span class="sxs-lookup"><span data-stu-id="8e914-106">For each request, the following information is listed.</span></span>



|              |                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e914-107">GUID de solicitação</span><span class="sxs-lookup"><span data-stu-id="8e914-107">Request GUID</span></span> | <span data-ttu-id="8e914-108">Identifica a solicitação.</span><span class="sxs-lookup"><span data-stu-id="8e914-108">Identifies the request.</span></span> <span data-ttu-id="8e914-109">Defina o membro **guidSetting** da estrutura [**de \_ \_ \_ parâmetros obter informações de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) igual a esse valor.</span><span class="sxs-lookup"><span data-stu-id="8e914-109">Set the **guidSetting** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="8e914-110">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="8e914-110">Input data</span></span>   | <span data-ttu-id="8e914-111">Especifica como interpretar a matriz **abParameters** na estrutura de [**\_ parâmetros obter \_ informações \_ de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) .</span><span class="sxs-lookup"><span data-stu-id="8e914-111">Specifies how to interpret the **abParameters** array in the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure.</span></span>                      |
| <span data-ttu-id="8e914-112">Dados de saída</span><span class="sxs-lookup"><span data-stu-id="8e914-112">Output data</span></span>  | <span data-ttu-id="8e914-113">Especifica como interpretar a matriz **abRequestedInformation** na estrutura de [**\_ \_ informações de OPM solicitado**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) .</span><span class="sxs-lookup"><span data-stu-id="8e914-113">Specifies how to interpret the **abRequestedInformation** array in the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span>         |



 

<span data-ttu-id="8e914-114">As seguintes solicitações de status são definidas:</span><span class="sxs-lookup"><span data-stu-id="8e914-114">The following status requests are defined:</span></span>



| <span data-ttu-id="8e914-115">Solicitação de status</span><span class="sxs-lookup"><span data-stu-id="8e914-115">Status request</span></span>                                                                                      | <span data-ttu-id="8e914-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e914-116">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e914-117">**os OPM \_ Get \_ ACP \_ e \_ CGMSA \_ Signaling**</span><span class="sxs-lookup"><span data-stu-id="8e914-117">**OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-get-acp-and-cgmsa-signaling.md)                     | <span data-ttu-id="8e914-118">Retorna as seguintes informações sobre uma saída de vídeo:</span><span class="sxs-lookup"><span data-stu-id="8e914-118">Returns the following information about a video output:</span></span>                                                                                               |
| [<span data-ttu-id="8e914-119">**formato de saída de OPM de \_ obtenção \_ real \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8e914-119">**OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT**</span></span>](opm-get-actual-output-format.md)                            | <span data-ttu-id="8e914-120">Retorna uma descrição do sinal de vídeo que está sendo transmitido pelo conector.</span><span class="sxs-lookup"><span data-stu-id="8e914-120">Returns a description of the video signal that is being transmitted over the connector.</span></span>                                                               |
| [<span data-ttu-id="8e914-121">**nível de proteção do OPM \_ obter \_ real \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8e914-121">**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-actual-protection-level.md)                      | <span data-ttu-id="8e914-122">Retorna o nível de proteção global para um mecanismo de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="8e914-122">Returns the global protection level for a specified protection mechanism.</span></span>                                                                             |
| [<span data-ttu-id="8e914-123">**\_tipo de \_ barramento de adaptador de obtenção de OPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8e914-123">**OPM\_GET\_ADAPTER\_BUS\_TYPE**</span></span>](opm-get-adapter-bus-type.md)                                    | <span data-ttu-id="8e914-124">Retorna o tipo de barramento de e/s usado pela saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e914-124">Returns the type of I/O bus used by the video output.</span></span>                                                                                                 |
| [<span data-ttu-id="8e914-125">**\_informações do \_ codec de obtenção de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="8e914-125">**OPM\_GET\_CODEC\_INFO**</span></span>](opm-get-codec-info.md)                                                 | <span data-ttu-id="8e914-126">Obtém o valor de mérito de um codec de hardware.</span><span class="sxs-lookup"><span data-stu-id="8e914-126">Gets the merit value of a hardware codec.</span></span>                                                                                                             |
| [<span data-ttu-id="8e914-127">**\_informações de \_ dispositivo de HDCP de conexão \_ \_ de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="8e914-127">**OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**</span></span>](opm-get-connected-hdcp-device-information.md) | <span data-ttu-id="8e914-128">Obtém informações sobre um dispositivo de Proteção de Conteúdo High-Bandwidth digital (HDCP) anexado à saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e914-128">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="8e914-129">As seguintes informações são retornadas:</span><span class="sxs-lookup"><span data-stu-id="8e914-129">The following information is returned:</span></span> |
| [<span data-ttu-id="8e914-130">**\_tipo de \_ conector de obtenção de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="8e914-130">**OPM\_GET\_CONNECTOR\_TYPE**</span></span>](opm-get-connector-type.md)                                         | <span data-ttu-id="8e914-131">Retorna o tipo de conector físico da saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e914-131">Returns the physical connector type of the video output.</span></span>                                                                                              |
| [<span data-ttu-id="8e914-132">**OPM \_ obter \_ versão atual do \_ SRM de HDCP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8e914-132">**OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION**</span></span>](opm-get-current-hdcp-srm-version.md)                   | <span data-ttu-id="8e914-133">Retorna o número de versão da mensagem de renovação do sistema (SRM) usada atualmente pela saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e914-133">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>                                               |
| [<span data-ttu-id="8e914-134">**OPM \_ obter \_ características de DVI \_**</span><span class="sxs-lookup"><span data-stu-id="8e914-134">**OPM\_GET\_DVI\_CHARACTERISTICS**</span></span>](opm-get-dvi-characteristics.md)                               | <span data-ttu-id="8e914-135">Consulta se um conector DVI (Digital Video interface) dá suporte a DVI versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8e914-135">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>                                                          |
| [<span data-ttu-id="8e914-136">**\_ID de \_ saída de obtenção de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="8e914-136">**OPM\_GET\_OUTPUT\_ID**</span></span>](opm-get-output-id.md)                                                   | <span data-ttu-id="8e914-137">Retorna o identificador exclusivo do monitor associado a esta saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e914-137">Returns the unique identifier of the monitor associated with this video output.</span></span>                                                                       |
| [<span data-ttu-id="8e914-138">**os \_ tipos de proteção de OPM \_ têm suporte \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8e914-138">**OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES**</span></span>](opm-get-supported-protection-types.md)                | <span data-ttu-id="8e914-139">Retorna a lista de mecanismos de proteção aos quais o conector dá suporte.</span><span class="sxs-lookup"><span data-stu-id="8e914-139">Returns the list of protection mechanisms that are supported by the connector.</span></span>                                                                        |
| [<span data-ttu-id="8e914-140">**OPM \_ obter \_ \_ nível de proteção virtual \_**</span><span class="sxs-lookup"><span data-stu-id="8e914-140">**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-virtual-protection-level.md)                    | <span data-ttu-id="8e914-141">Retorna o nível de proteção virtual para um mecanismo de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="8e914-141">Returns the virtual protection level for a specified protection mechanism.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="8e914-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e914-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e914-143">Referência de programação de OPM</span><span class="sxs-lookup"><span data-stu-id="8e914-143">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="8e914-144">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="8e914-144">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



