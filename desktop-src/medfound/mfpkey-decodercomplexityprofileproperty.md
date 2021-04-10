---
description: Especifica o perfil de complexidade do conteúdo codificado.
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: Propriedade MFPKEY_DECODERCOMPLEXITYPROFILE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39544830a0a05e21779a637da61d3bcb310fcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827917"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a><span data-ttu-id="f2d64-103">\_Propriedade MFPKEY DECODERCOMPLEXITYPROFILE</span><span class="sxs-lookup"><span data-stu-id="f2d64-103">MFPKEY\_DECODERCOMPLEXITYPROFILE Property</span></span>

<span data-ttu-id="f2d64-104">Especifica o perfil de complexidade do conteúdo codificado.</span><span class="sxs-lookup"><span data-stu-id="f2d64-104">Specifies the complexity profile of the encoded content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f2d64-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f2d64-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f2d64-106">g \_ wszWMVCDecoderComplexityProfile</span><span class="sxs-lookup"><span data-stu-id="f2d64-106">g\_wszWMVCDecoderComplexityProfile</span></span>

## <a name="data-type"></a><span data-ttu-id="f2d64-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="f2d64-107">Data Type</span></span>

<span data-ttu-id="f2d64-108">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="f2d64-108">**VT\_BSTR**</span></span>

## <a name="remarks"></a><span data-ttu-id="f2d64-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2d64-109">Remarks</span></span>

<span data-ttu-id="f2d64-110">Você pode ler esse valor somente após a conclusão da codificação.</span><span class="sxs-lookup"><span data-stu-id="f2d64-110">You can read this value only after encoding is completed.</span></span>

<span data-ttu-id="f2d64-111">Para áudio, essa propriedade tem um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2d64-111">For audio, this property has one of the following values.</span></span>



| <span data-ttu-id="f2d64-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f2d64-112">Value</span></span> | <span data-ttu-id="f2d64-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2d64-113">Description</span></span>                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2d64-114">L1</span><span class="sxs-lookup"><span data-stu-id="f2d64-114">"L1"</span></span>  | <span data-ttu-id="f2d64-115">Codificação padrão com uma taxa de amostragem de 44,1 KHz e uma taxa de bits máxima de 161 kbps.</span><span class="sxs-lookup"><span data-stu-id="f2d64-115">Standard encoding with a sampling rate of 44.1 KHz and a maximum bit rate of 161 Kbps.</span></span>         |
| <span data-ttu-id="f2d64-116">Cache</span><span class="sxs-lookup"><span data-stu-id="f2d64-116">"L2"</span></span>  | <span data-ttu-id="f2d64-117">Codificação padrão com taxas de amostragem de até 48 KHz e uma taxa de bits máxima de 161 kbps.</span><span class="sxs-lookup"><span data-stu-id="f2d64-117">Standard encoding with sampling rates up to 48 KHz and a maximum bit rate of 161 Kbps.</span></span>         |
| <span data-ttu-id="f2d64-118">MB</span><span class="sxs-lookup"><span data-stu-id="f2d64-118">"L3"</span></span>  | <span data-ttu-id="f2d64-119">Codificação padrão com taxas de amostragem de até 48 KHz e uma taxa de bits máxima de 385 kbps.</span><span class="sxs-lookup"><span data-stu-id="f2d64-119">Standard encoding with sampling rates up to 48 KHz and a maximum bit rate of 385 Kbps.</span></span>         |
| <span data-ttu-id="f2d64-120">"M0a"</span><span class="sxs-lookup"><span data-stu-id="f2d64-120">"M0a"</span></span> | <span data-ttu-id="f2d64-121">Codificação profissional com taxas de amostragem de até 48 KHz e taxas de bits entre 48 e 192 kbps.</span><span class="sxs-lookup"><span data-stu-id="f2d64-121">Professional encoding with sampling rates up to 48 KHz and bit rates between 48 and 192 Kbps.</span></span>  |
| <span data-ttu-id="f2d64-122">"M0b"</span><span class="sxs-lookup"><span data-stu-id="f2d64-122">"M0b"</span></span> | <span data-ttu-id="f2d64-123">Codificação profissional com taxas de amostragem de até 48 KHz e uma taxa de bits máxima de 192 kbps.</span><span class="sxs-lookup"><span data-stu-id="f2d64-123">Professional encoding with sampling rates up to 48 KHz and a maximum bitrate of 192 Kbps.</span></span>      |
| <span data-ttu-id="f2d64-124">M1</span><span class="sxs-lookup"><span data-stu-id="f2d64-124">"M1"</span></span>  | <span data-ttu-id="f2d64-125">Codificação profissional com taxas de amostragem de até 48 KHz e uma taxa de bits máxima de 384 kbps.</span><span class="sxs-lookup"><span data-stu-id="f2d64-125">Professional encoding with sampling rates up to 48 KHz and a maximum bitrate of 384 Kbps.</span></span>      |
| <span data-ttu-id="f2d64-126">M2</span><span class="sxs-lookup"><span data-stu-id="f2d64-126">"M2"</span></span>  | <span data-ttu-id="f2d64-127">Codificação profissional com taxas de amostragem de até 96 KHz e uma taxa de bits máxima de 768 Kbps.</span><span class="sxs-lookup"><span data-stu-id="f2d64-127">Professional encoding with sampling rates up to 96 KHz and a maximum bitrate of 768 Kbps.</span></span>      |
| <span data-ttu-id="f2d64-128">M3</span><span class="sxs-lookup"><span data-stu-id="f2d64-128">"M3"</span></span>  | <span data-ttu-id="f2d64-129">Codificação profissional com taxas de amostragem de até 96 KHz e uma taxa de bits máxima de 1,5 Mbps.</span><span class="sxs-lookup"><span data-stu-id="f2d64-129">Professional encoding with sampling rates up to 96 KHz and a maximum bitrate of 1.5 Mbps.</span></span>      |
| <span data-ttu-id="f2d64-130">Múltiplos</span><span class="sxs-lookup"><span data-stu-id="f2d64-130">"N1"</span></span>  | <span data-ttu-id="f2d64-131">Codificação sem perdas com taxas de amostragem de até 48 KHz e um máximo de 2 canais.</span><span class="sxs-lookup"><span data-stu-id="f2d64-131">Lossless encoding with sampling rates up to 48 KHz and a maximum of 2 channels.</span></span>                |
| <span data-ttu-id="f2d64-132">N2</span><span class="sxs-lookup"><span data-stu-id="f2d64-132">"N2"</span></span>  | <span data-ttu-id="f2d64-133">Codificação sem perdas com taxas de amostragem de até 96 KHz e um máximo de 6 canais (5,1 surround).</span><span class="sxs-lookup"><span data-stu-id="f2d64-133">Lossless encoding with sampling rates up to 96 KHz and a maximum of 6 channels (5.1 surround).</span></span> |
| <span data-ttu-id="f2d64-134">N3</span><span class="sxs-lookup"><span data-stu-id="f2d64-134">"N3"</span></span>  | <span data-ttu-id="f2d64-135">Codificação sem perdas com taxas de amostragem de até 96 KHz e um máximo de 8 canais (7,1 surround).</span><span class="sxs-lookup"><span data-stu-id="f2d64-135">Lossless encoding with sampling rates up to 96 KHz and a maximum of 8 channels (7.1 surround).</span></span> |



 

<span data-ttu-id="f2d64-136">Para vídeo, essa propriedade tem um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="f2d64-136">For video, this property has one of the following values:</span></span>



| <span data-ttu-id="f2d64-137">Valor</span><span class="sxs-lookup"><span data-stu-id="f2d64-137">Value</span></span> | <span data-ttu-id="f2d64-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2d64-138">Description</span></span>                                                                       |
|-------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f2d64-139">PONTOS</span><span class="sxs-lookup"><span data-stu-id="f2d64-139">"AP"</span></span>  | <span data-ttu-id="f2d64-140">perfil avançado (disponível somente no codec de perfil avançado do vídeo do Windows Media 9)</span><span class="sxs-lookup"><span data-stu-id="f2d64-140">advanced profile (available only on Windows Media Video 9 Advanced Profile codec)</span></span> |
| <span data-ttu-id="f2d64-141">CP</span><span class="sxs-lookup"><span data-stu-id="f2d64-141">"CP"</span></span>  | <span data-ttu-id="f2d64-142">Não tem mais suporte</span><span class="sxs-lookup"><span data-stu-id="f2d64-142">no longer supported</span></span>                                                               |
| <span data-ttu-id="f2d64-143">MP</span><span class="sxs-lookup"><span data-stu-id="f2d64-143">"MP"</span></span>  | <span data-ttu-id="f2d64-144">Perfil principal</span><span class="sxs-lookup"><span data-stu-id="f2d64-144">main profile</span></span>                                                                      |
| <span data-ttu-id="f2d64-145">SP3</span><span class="sxs-lookup"><span data-stu-id="f2d64-145">"SP"</span></span>  | <span data-ttu-id="f2d64-146">Perfil simples</span><span class="sxs-lookup"><span data-stu-id="f2d64-146">simple profile</span></span>                                                                    |



 

<span data-ttu-id="f2d64-147">Para conteúdo de vídeo, você pode solicitar um nível de perfil definindo [MFPKEY \_ DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) antes de começar a codificação.</span><span class="sxs-lookup"><span data-stu-id="f2d64-147">For video content, you can request a profile level by setting [MFPKEY\_DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) before you begin encoding.</span></span> <span data-ttu-id="f2d64-148">O codec tentará codificar dentro dos parâmetros do nível de complexidade solicitado, mas as outras configurações que você configurar terão precedência.</span><span class="sxs-lookup"><span data-stu-id="f2d64-148">The codec will attempt to encode within the parameters of the requested complexity level, but the other settings that you configure will take precedence.</span></span> <span data-ttu-id="f2d64-149">Você sempre deve verificar o valor do perfil de complexidade real após a codificação, caso sua solicitação não possa ser respeitada.</span><span class="sxs-lookup"><span data-stu-id="f2d64-149">You should always check the actual complexity profile value after encoding in case your request could not be honored.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2d64-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2d64-150">Requirements</span></span>



| <span data-ttu-id="f2d64-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2d64-151">Requirement</span></span> | <span data-ttu-id="f2d64-152">Valor</span><span class="sxs-lookup"><span data-stu-id="f2d64-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2d64-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2d64-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f2d64-154">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f2d64-154">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f2d64-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2d64-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f2d64-156">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2d64-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2d64-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2d64-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2d64-158"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2d64-158"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2d64-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2d64-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2d64-160">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f2d64-160">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




