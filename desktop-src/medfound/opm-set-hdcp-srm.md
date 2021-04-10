---
description: Atualiza a mensagem de renovação do sistema (SRM) para o High-Bandwidth digital Proteção de Conteúdo (HDCP).
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: OPM_SET_HDCP_SRM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9283c493598f22a1715f687eccea985a27e0e6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164899"
---
# <a name="opm_set_hdcp_srm"></a><span data-ttu-id="99b4d-103">OPM \_ definido \_ SRM de HDCP \_</span><span class="sxs-lookup"><span data-stu-id="99b4d-103">OPM\_SET\_HDCP\_SRM</span></span>

<span data-ttu-id="99b4d-104">Atualiza a mensagem de renovação do sistema (SRM) para o High-Bandwidth digital Proteção de Conteúdo (HDCP).</span><span class="sxs-lookup"><span data-stu-id="99b4d-104">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span>



| <span data-ttu-id="99b4d-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="99b4d-105">Requirement</span></span> | <span data-ttu-id="99b4d-106">Valor</span><span class="sxs-lookup"><span data-stu-id="99b4d-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="99b4d-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="99b4d-107">Command GUID</span></span> | <span data-ttu-id="99b4d-108">OPM \_ definido \_ SRM de HDCP \_</span><span class="sxs-lookup"><span data-stu-id="99b4d-108">OPM\_SET\_HDCP\_SRM</span></span>                                                                 |
| <span data-ttu-id="99b4d-109">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="99b4d-109">Input data</span></span>   | <span data-ttu-id="99b4d-110">Uma estrutura de [**\_ parâmetros de \_ \_ SRM \_ de HDCP definido de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)</span><span class="sxs-lookup"><span data-stu-id="99b4d-110">An [**OPM\_SET\_HDCP\_SRM\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) structure</span></span> |



 

<span data-ttu-id="99b4d-111">O parâmetro *pbAdditionalParameters* de [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) deve apontar para um buffer que contém o SRM.</span><span class="sxs-lookup"><span data-stu-id="99b4d-111">The *pbAdditionalParameters* parameter of [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) must point to a buffer that contains the SRM.</span></span> <span data-ttu-id="99b4d-112">O formato de um SRM de HDCP é documentado na especificação de HDCP.</span><span class="sxs-lookup"><span data-stu-id="99b4d-112">The format of an HDCP SRM is documented in the HDCP specification.</span></span> <span data-ttu-id="99b4d-113">Defina o parâmetro *ulAdditionalParametersSize* igual ao tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="99b4d-113">Set the *ulAdditionalParametersSize* parameter equal to the size of the buffer, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="99b4d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="99b4d-114">Remarks</span></span>

<span data-ttu-id="99b4d-115">SRMs são usados para atualizar a lista de dispositivos HDCP revogados.</span><span class="sxs-lookup"><span data-stu-id="99b4d-115">SRMs are used to update the list of revoked HDCP devices.</span></span> <span data-ttu-id="99b4d-116">SRMs são entregues com o conteúdo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="99b4d-116">SRMs are delivered with the video content.</span></span>

<span data-ttu-id="99b4d-117">Esse comando atualiza o SRM atual da saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="99b4d-117">This command updates the video output's current SRM.</span></span> <span data-ttu-id="99b4d-118">Se a HDCP estiver habilitada no momento do comando, a saída de vídeo usará o novo SRM para verificar se algum dos dispositivos de HDCP conectados está revogado.</span><span class="sxs-lookup"><span data-stu-id="99b4d-118">If HDCP is enabled at the time of the command, the video output uses the new SRM to check whether any of the connected HDCP devices are revoked.</span></span> <span data-ttu-id="99b4d-119">Se a saída de vídeo detectar um dispositivo revogado, ele interromperá a exibição do vídeo.</span><span class="sxs-lookup"><span data-stu-id="99b4d-119">If the video output detects a revoked device, it stops displaying video.</span></span> <span data-ttu-id="99b4d-120">Se você enviar esse comando enquanto o HDCP estiver desabilitado, a saída de vídeo validará o SRM e o armazenará.</span><span class="sxs-lookup"><span data-stu-id="99b4d-120">If you send this command while HDCP is disabled, the video output validates the SRM and stores it.</span></span> <span data-ttu-id="99b4d-121">Posteriormente, se o aplicativo habilitar a HDCP, a saída de vídeo usará o novo SRM para verificar o status de revogação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99b4d-121">Later, if the application enables HDCP, the video output uses the new SRM to check the device's revocation status.</span></span>

<span data-ttu-id="99b4d-122">Esse comando pode fazer com que o método **Configure** retorne qualquer um dos códigos de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="99b4d-122">This command can cause the **Configure** method to return any of the following error codes.</span></span>



| <span data-ttu-id="99b4d-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="99b4d-123">Return code</span></span>                                            | <span data-ttu-id="99b4d-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="99b4d-124">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="99b4d-125">gráficos de erro \_ \_ OPM \_ \_ SRM inválido</span><span class="sxs-lookup"><span data-stu-id="99b4d-125">ERROR\_GRAPHICS\_OPM\_INVALID\_SRM</span></span>                     | <span data-ttu-id="99b4d-126">O SRM não é válido.</span><span class="sxs-lookup"><span data-stu-id="99b4d-126">The SRM is not valid.</span></span>                   |
| <span data-ttu-id="99b4d-127">ERRO \_ gráficos \_ de \_ saída \_ OPM \_ não \_ dá suporte a \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="99b4d-127">ERROR\_GRAPHICS\_OPM\_OUTPUT\_DOES\_NOT\_SUPPORT\_HDCP</span></span> | <span data-ttu-id="99b4d-128">A saída de vídeo não oferece suporte a HDCP.</span><span class="sxs-lookup"><span data-stu-id="99b4d-128">The video output does not support HDCP.</span></span> |



 

<span data-ttu-id="99b4d-129">Não há suporte para esse comando quando a interface **IOPMVideoOutput** emula o protocolo Copp (certificado de proteção de saída).</span><span class="sxs-lookup"><span data-stu-id="99b4d-129">This command is not supported when the **IOPMVideoOutput** interface emulates Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="99b4d-130">Quando semântica COPP é usada, o aplicativo é responsável por analisar SRMs e verificar o status de revogação do dispositivo HDCP.</span><span class="sxs-lookup"><span data-stu-id="99b4d-130">When COPP semantics are used, the application is responsible for parsing SRMs and checking the revocation status of the HDCP device.</span></span> <span data-ttu-id="99b4d-131">Use a solicitação de status de [informações do dispositivo OPM- \_ \_ conectado \_ HDCP \_ \_ ](opm-get-connected-hdcp-device-information.md) para obter o vetor de seleção de chave (KSV) do dispositivo, que é necessário para verificar o status de revogação.</span><span class="sxs-lookup"><span data-stu-id="99b4d-131">Use the [OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION](opm-get-connected-hdcp-device-information.md) status request to get the device's key selection vector (KSV), which is needed to check the revocation status.</span></span> <span data-ttu-id="99b4d-132">Para obter mais informações sobre SRMs, consulte a especificação de HDCP.</span><span class="sxs-lookup"><span data-stu-id="99b4d-132">For more information about SRMs, refer to the HDCP specification.</span></span>

## <a name="requirements"></a><span data-ttu-id="99b4d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99b4d-133">Requirements</span></span>



| <span data-ttu-id="99b4d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="99b4d-134">Requirement</span></span> | <span data-ttu-id="99b4d-135">Valor</span><span class="sxs-lookup"><span data-stu-id="99b4d-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="99b4d-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99b4d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="99b4d-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99b4d-137">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="99b4d-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99b4d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="99b4d-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="99b4d-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="99b4d-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99b4d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="99b4d-141"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="99b4d-141"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99b4d-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="99b4d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b4d-143">**IOPMVideoOutput:: Configure**</span><span class="sxs-lookup"><span data-stu-id="99b4d-143">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="99b4d-144">Comandos OPM</span><span class="sxs-lookup"><span data-stu-id="99b4d-144">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




