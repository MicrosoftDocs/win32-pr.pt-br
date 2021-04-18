---
description: Os sinalizadores na tabela a seguir especificam mecanismos de proteção de saída para o Gerenciador de proteção de saída (OPM).
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: Sinalizadores de tipo de proteção OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc8b30a18f5c7bf68fb01775751aa56e1e619f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812016"
---
# <a name="opm-protection-type-flags"></a><span data-ttu-id="beb1a-103">Sinalizadores de tipo de proteção OPM</span><span class="sxs-lookup"><span data-stu-id="beb1a-103">OPM Protection Type Flags</span></span>

<span data-ttu-id="beb1a-104">Os sinalizadores na tabela a seguir especificam mecanismos de proteção de saída para o Gerenciador de proteção de saída (OPM).</span><span class="sxs-lookup"><span data-stu-id="beb1a-104">The flags in the following table specify output protection mechanisms for Output Protection Manager (OPM).</span></span>



| <span data-ttu-id="beb1a-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="beb1a-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="beb1a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="beb1a-106">Description</span></span>                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <span data-ttu-id="beb1a-107"><dt>**OPM \_ Tipo de proteção \_ \_ outro**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="beb1a-107"><dt>**OPM\_PROTECTION\_TYPE\_OTHER**</dt> <dt>0x80000000</dt></span></span> </dl>                                                | <span data-ttu-id="beb1a-108">Mecanismo de proteção desconhecido.</span><span class="sxs-lookup"><span data-stu-id="beb1a-108">Unknown protection mechanism.</span></span><br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <span data-ttu-id="beb1a-109"><dt>**OPM \_ Tipo de proteção \_ \_ nenhum**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="beb1a-109"><dt>**OPM\_PROTECTION\_TYPE\_NONE**</dt> <dt>0x00000000</dt></span></span> </dl>                                                   | <span data-ttu-id="beb1a-110">Nenhum mecanismo de proteção.</span><span class="sxs-lookup"><span data-stu-id="beb1a-110">No protection mechanisms.</span></span><br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <span data-ttu-id="beb1a-111"><dt>**OPM \_ Tipo de proteção de \_ \_ \_ \_ HDCP compatível com a Copp**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="beb1a-111"><dt>**OPM\_PROTECTION\_TYPE\_COPP\_COMPATIBLE\_HDCP**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="beb1a-112">High-Bandwidth Proteção de Conteúdo Digital (HDCP).</span><span class="sxs-lookup"><span data-stu-id="beb1a-112">High-Bandwidth Digital Content Protection (HDCP).</span></span> <span data-ttu-id="beb1a-113">Esse sinalizador é usado ao emular o protocolo de proteção de saída certificado (COPP).</span><span class="sxs-lookup"><span data-stu-id="beb1a-113">This flag is used when emulating Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="beb1a-114">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="beb1a-114">For more information, see Remarks.</span></span> <span data-ttu-id="beb1a-115">Esse sinalizador não tem suporte para semântica OPM.</span><span class="sxs-lookup"><span data-stu-id="beb1a-115">This flag is not supported for OPM semantics.</span></span><br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <span data-ttu-id="beb1a-116"><dt>**OPM \_ Tipo de proteção \_ \_ ACP**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="beb1a-116"><dt>**OPM\_PROTECTION\_TYPE\_ACP**</dt> <dt>0x00000002</dt></span></span> </dl>                                                      | <span data-ttu-id="beb1a-117">Proteção de cópia analógica (ACP).</span><span class="sxs-lookup"><span data-stu-id="beb1a-117">Analog Copy Protection (ACP).</span></span><br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <span data-ttu-id="beb1a-118"><dt>**OPM \_ Tipo de proteção \_ \_ CGMSA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="beb1a-118"><dt>**OPM\_PROTECTION\_TYPE\_CGMSA**</dt> <dt>0x00000004</dt></span></span> </dl>                                                | <span data-ttu-id="beb1a-119">Sistema de gerenciamento de geração de cópia — analógico (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="beb1a-119">Copy Generation Management System—Analog (CGMS-A).</span></span><br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <span data-ttu-id="beb1a-120"><dt>**OPM \_ Tipo de proteção de \_ \_ HDCP**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="beb1a-120"><dt>**OPM\_PROTECTION\_TYPE\_HDCP**</dt> <dt>0x00000008</dt></span></span> </dl>                                                   | <span data-ttu-id="beb1a-121">HDCP.</span><span class="sxs-lookup"><span data-stu-id="beb1a-121">HDCP.</span></span> <span data-ttu-id="beb1a-122">Esse sinalizador é usado quando o objeto OPM tem semântica OPM.</span><span class="sxs-lookup"><span data-stu-id="beb1a-122">This flag is used when the OPM object has OPM semantics.</span></span> <span data-ttu-id="beb1a-123">Não há suporte para semântica COPP.</span><span class="sxs-lookup"><span data-stu-id="beb1a-123">It is not supported for COPP semantics.</span></span><br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <span data-ttu-id="beb1a-124"><dt>**OPM \_ Tipo de proteção \_ \_ DPCP**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="beb1a-124"><dt>**OPM\_PROTECTION\_TYPE\_DPCP**</dt> <dt>0x00000010</dt></span></span> </dl>                                                   | <span data-ttu-id="beb1a-125">Proteção de Conteúdo DisplayPort (DPCP).</span><span class="sxs-lookup"><span data-stu-id="beb1a-125">DisplayPort Content Protection (DPCP).</span></span><br/>                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="beb1a-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="beb1a-126">Remarks</span></span>

<span data-ttu-id="beb1a-127">Esses sinalizadores são usados nos seguintes comandos de OPM e solicitações de status.</span><span class="sxs-lookup"><span data-stu-id="beb1a-127">These flags are used in the following OPM commands and status requests.</span></span>

-   [<span data-ttu-id="beb1a-128">OPM \_ definir \_ nível de proteção \_</span><span class="sxs-lookup"><span data-stu-id="beb1a-128">OPM\_SET\_PROTECTION\_LEVEL</span></span>](opm-set-protection-level.md)
-   [<span data-ttu-id="beb1a-129">OPM \_ obter \_ \_ nível de proteção virtual \_</span><span class="sxs-lookup"><span data-stu-id="beb1a-129">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>](opm-get-virtual-protection-level.md)
-   [<span data-ttu-id="beb1a-130">nível de proteção do OPM \_ obter \_ real \_ \_</span><span class="sxs-lookup"><span data-stu-id="beb1a-130">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>](opm-get-actual-protection-level.md)

### <a name="hdcp"></a><span data-ttu-id="beb1a-131">HDCP</span><span class="sxs-lookup"><span data-stu-id="beb1a-131">HDCP</span></span>

<span data-ttu-id="beb1a-132">Os dois sinalizadores a seguir são definidos para HDCP.</span><span class="sxs-lookup"><span data-stu-id="beb1a-132">The following two flags are defined for HDCP.</span></span>



| <span data-ttu-id="beb1a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="beb1a-133">Value</span></span>                                         | <span data-ttu-id="beb1a-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="beb1a-134">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beb1a-135">tipo de proteção OPM de \_ \_ \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="beb1a-135">OPM\_PROTECTION\_TYPE\_HDCP</span></span>                   | <span data-ttu-id="beb1a-136">Use esse sinalizador se o ponteiro [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) tiver sido criado com semântica OPM.</span><span class="sxs-lookup"><span data-stu-id="beb1a-136">Use this flag if the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer was created with OPM semantics.</span></span>                                                                        |
| <span data-ttu-id="beb1a-137">tipo de proteção OPM de \_ \_ \_ \_ HDCP compatível com Copp \_</span><span class="sxs-lookup"><span data-stu-id="beb1a-137">OPM\_PROTECTION\_TYPE\_COPP\_COMPATIBLE\_HDCP</span></span> | <span data-ttu-id="beb1a-138">Use esse sinalizador se o ponteiro [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) tiver sido criado com semântica COPP.</span><span class="sxs-lookup"><span data-stu-id="beb1a-138">Use this flag if the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer was created with COPP semantics.</span></span> <span data-ttu-id="beb1a-139">Esse sinalizador corresponde ao sinalizador de \_ HDCP de proteção de Copp \_ em COPP.</span><span class="sxs-lookup"><span data-stu-id="beb1a-139">This flag corresponds to the COPP\_ProtectionType\_HDCP flag in COPP.</span></span> |



 

<span data-ttu-id="beb1a-140">Ambos os modos (semântica de OPM e semânticos de COPP) dão suporte às seguintes operações para HDCP:</span><span class="sxs-lookup"><span data-stu-id="beb1a-140">Both modes (OPM semantics and COPP semantics) support the following operations for HDCP:</span></span>

-   <span data-ttu-id="beb1a-141">Habilitar ou desabilitar o HDCP usando o comando de [nível de proteção de OPM \_ set \_ Protection \_ ](opm-set-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="beb1a-141">Enable or disable HDCP by using the [OPM\_SET\_PROTECTION\_LEVEL](opm-set-protection-level.md) command.</span></span>
-   <span data-ttu-id="beb1a-142">Consulte se a HDCP está habilitada usando a solicitação de status de [nível de \_ \_ \_ proteção \_ ](opm-get-actual-protection-level.md) do [OPM \_ \_ \_ \_ ](opm-get-virtual-protection-level.md)</span><span class="sxs-lookup"><span data-stu-id="beb1a-142">Query whether HDCP is enabled by using the [OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL](opm-get-virtual-protection-level.md) or [OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL](opm-get-actual-protection-level.md) status request.</span></span>

<span data-ttu-id="beb1a-143">A semântica de OPM também oferece suporte ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="beb1a-143">OPM semantics also support the following:</span></span>

-   <span data-ttu-id="beb1a-144">Repetidores de HDCP.</span><span class="sxs-lookup"><span data-stu-id="beb1a-144">HDCP repeaters.</span></span> <span data-ttu-id="beb1a-145">Um *repetidor HDCP* é um dispositivo HDCP que pode receber conteúdo HDCP e também criptografar novamente e transmitir o mesmo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="beb1a-145">An *HDCP repeater* is an HDCP device that can receive HDCP content and also re-encrypt and transmit the same content.</span></span>
-   <span data-ttu-id="beb1a-146">Revogação de HDCP.</span><span class="sxs-lookup"><span data-stu-id="beb1a-146">HDCP revocation.</span></span> <span data-ttu-id="beb1a-147">Se um dispositivo HDCP revogado for anexado à saída de vídeo OPM, a saída de vídeo não transmitirá o vídeo.</span><span class="sxs-lookup"><span data-stu-id="beb1a-147">If a revoked HDCP device is attached to the OPM video output, the video output will not transmit the video.</span></span> <span data-ttu-id="beb1a-148">O aplicativo não precisa analisar SRMs (mensagens de renovação do sistema HDCP) ou determinar se o dispositivo de saída foi revogado.</span><span class="sxs-lookup"><span data-stu-id="beb1a-148">The application does not need to parse HDCP system renewability messages (SRMs) or determine whether the output device has been revoked.</span></span> <span data-ttu-id="beb1a-149">Para obter mais informações, consulte o comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .</span><span class="sxs-lookup"><span data-stu-id="beb1a-149">For more information, see the [**OPM\_SET\_HDCP\_SRM**](opm-set-hdcp-srm.md) command.</span></span>

<span data-ttu-id="beb1a-150">Quando a semântica COPP é usada, a interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) não dá suporte a repetidores de HDCP.</span><span class="sxs-lookup"><span data-stu-id="beb1a-150">When COPP semantics are used, the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface does not support HDCP repeaters.</span></span> <span data-ttu-id="beb1a-151">Além disso, ele não trata a revogação de HDCP.</span><span class="sxs-lookup"><span data-stu-id="beb1a-151">Also, it does not handle HDCP revocation.</span></span> <span data-ttu-id="beb1a-152">Em vez disso, o aplicativo deve analisar o SRM para determinar se um dispositivo HDCP foi revogado.</span><span class="sxs-lookup"><span data-stu-id="beb1a-152">Instead, the application must parse the SRM to determine whether an HDCP device has been revoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="beb1a-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beb1a-153">Requirements</span></span>



| <span data-ttu-id="beb1a-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="beb1a-154">Requirement</span></span> | <span data-ttu-id="beb1a-155">Valor</span><span class="sxs-lookup"><span data-stu-id="beb1a-155">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="beb1a-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="beb1a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="beb1a-157">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="beb1a-157">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="beb1a-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="beb1a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="beb1a-159">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="beb1a-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="beb1a-160">parâmetro</span><span class="sxs-lookup"><span data-stu-id="beb1a-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="beb1a-161"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="beb1a-161"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beb1a-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="beb1a-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb1a-163">Enumerações de OPM</span><span class="sxs-lookup"><span data-stu-id="beb1a-163">OPM Enumerations</span></span>](opm-enumerations.md)
</dt> </dl>

 

 




