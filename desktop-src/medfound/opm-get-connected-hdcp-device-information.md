---
description: 'Saiba mais sobre: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561a348588b1244a6763eb447affa2b330e9c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502266"
---
# <a name="opm_get_connected_hdcp_device_information"></a><span data-ttu-id="64f8c-103">\_informações de \_ dispositivo de HDCP de conexão \_ \_ de OPM \_</span><span class="sxs-lookup"><span data-stu-id="64f8c-103">OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION</span></span>

<span data-ttu-id="64f8c-104">Obtém informações sobre um dispositivo de Proteção de Conteúdo High-Bandwidth digital (HDCP) anexado à saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="64f8c-104">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="64f8c-105">As seguintes informações são retornadas:</span><span class="sxs-lookup"><span data-stu-id="64f8c-105">The following information is returned:</span></span>

-   <span data-ttu-id="64f8c-106">O vetor de seleção de chave de HDCP do dispositivo (KSV).</span><span class="sxs-lookup"><span data-stu-id="64f8c-106">The device's HDCP key selection vector (KSV).</span></span>
-   <span data-ttu-id="64f8c-107">Se o dispositivo é um repetidor HDCP.</span><span class="sxs-lookup"><span data-stu-id="64f8c-107">Whether the device is an HDCP repeater.</span></span>



| <span data-ttu-id="64f8c-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="64f8c-108">Requirement</span></span> | <span data-ttu-id="64f8c-109">Valor</span><span class="sxs-lookup"><span data-stu-id="64f8c-109">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64f8c-110">GUID de solicitação</span><span class="sxs-lookup"><span data-stu-id="64f8c-110">Request GUID</span></span> | <span data-ttu-id="64f8c-111">\_informações de \_ dispositivo de HDCP de conexão \_ \_ de OPM \_</span><span class="sxs-lookup"><span data-stu-id="64f8c-111">OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION</span></span>                                                          |
| <span data-ttu-id="64f8c-112">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="64f8c-112">Input data</span></span>   | <span data-ttu-id="64f8c-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="64f8c-113">None</span></span>                                                                                                    |
| <span data-ttu-id="64f8c-114">Retornar dados</span><span class="sxs-lookup"><span data-stu-id="64f8c-114">Return data</span></span>  | <span data-ttu-id="64f8c-115">Uma estrutura de [**\_ informações de \_ \_ dispositivo \_ de HDCP conectada por OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)</span><span class="sxs-lookup"><span data-stu-id="64f8c-115">An [**OPM\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="64f8c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="64f8c-116">Remarks</span></span>

<span data-ttu-id="64f8c-117">Essa consulta pode ser usada somente com o *modo de emulação Copp*.</span><span class="sxs-lookup"><span data-stu-id="64f8c-117">This query can be used only with *COPP emulation mode*.</span></span> <span data-ttu-id="64f8c-118">Se a interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) usar a semântica de OPM (Gerenciador de proteção de saída), essa solicitação de status não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="64f8c-118">If the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface uses Output Protection Manager (OPM) semantics, this status request is not supported.</span></span>

<span data-ttu-id="64f8c-119">O KSV é um identificador fornecido para o fabricante do dispositivo e é usado no processo de autenticação e configuração de HDCP.</span><span class="sxs-lookup"><span data-stu-id="64f8c-119">The KSV is an identifier provided to the device manufacturer, and is used in the HDCP authentication and setup process.</span></span> <span data-ttu-id="64f8c-120">No modo de emulação COPP, o aplicativo usa o KSV para determinar se o dispositivo HDCP foi revogado.</span><span class="sxs-lookup"><span data-stu-id="64f8c-120">In COPP emulation mode, the application uses the KSV to determine whether the HDCP device is revoked.</span></span> <span data-ttu-id="64f8c-121">Se for, o aplicativo não deverá reproduzir o conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="64f8c-121">If it is, the application should not play protected content.</span></span> <span data-ttu-id="64f8c-122">Além disso, o aplicativo não deve reproduzir conteúdo protegido se o dispositivo for um repetidor HDCP, porque a COPP não dá suporte a repetidores de HDCP.</span><span class="sxs-lookup"><span data-stu-id="64f8c-122">Also, the application should not play protected content if the device is an HDCP repeater, because COPP does not support HDCP repeaters.</span></span>

<span data-ttu-id="64f8c-123">Essa consulta não é necessária quando é usada semântica de OPM, pois o OPM dá suporte à revogação de dispositivo e repetidores de HDCP.</span><span class="sxs-lookup"><span data-stu-id="64f8c-123">This query is not needed when OPM semantics are used, because OPM supports device revocation and HDCP repeaters.</span></span>

<span data-ttu-id="64f8c-124">Essa consulta é equivalente à consulta DXVA \_ COPPQueryHDCPKeyData usada no protocolo de proteção de saída certificado (Copp).</span><span class="sxs-lookup"><span data-stu-id="64f8c-124">This query is equivalent to the DXVA\_COPPQueryHDCPKeyData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="64f8c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64f8c-125">Requirements</span></span>



| <span data-ttu-id="64f8c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="64f8c-126">Requirement</span></span> | <span data-ttu-id="64f8c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="64f8c-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="64f8c-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64f8c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="64f8c-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64f8c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="64f8c-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64f8c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="64f8c-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="64f8c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="64f8c-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64f8c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="64f8c-133"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="64f8c-133"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64f8c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="64f8c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64f8c-135">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="64f8c-135">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="64f8c-136">Solicitações de status OPM</span><span class="sxs-lookup"><span data-stu-id="64f8c-136">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




