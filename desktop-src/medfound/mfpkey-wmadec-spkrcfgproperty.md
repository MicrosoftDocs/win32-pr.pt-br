---
description: Especifica a configuração do alto-falante no computador cliente.
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: Propriedade MFPKEY_WMADEC_SPKRCFG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ed96e4f722c1b3bd7c98178cd7f93a6c2e01df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505699"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a><span data-ttu-id="70b3b-103">\_Propriedade MFPKEY WMADEC \_ SPKRCFG</span><span class="sxs-lookup"><span data-stu-id="70b3b-103">MFPKEY\_WMADEC\_SPKRCFG Property</span></span>

<span data-ttu-id="70b3b-104">Especifica a configuração do alto-falante no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="70b3b-104">Specifies the speaker configuration on the client computer.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="70b3b-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="70b3b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="70b3b-106">g \_ wszWMACSpeakerConfig</span><span class="sxs-lookup"><span data-stu-id="70b3b-106">g\_wszWMACSpeakerConfig</span></span>

## <a name="data-type"></a><span data-ttu-id="70b3b-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="70b3b-107">Data Type</span></span>

<span data-ttu-id="70b3b-108">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="70b3b-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="70b3b-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="70b3b-109">Default Value</span></span>

<span data-ttu-id="70b3b-110">Nenhuma configuração de alto-falante específica é assumida.</span><span class="sxs-lookup"><span data-stu-id="70b3b-110">No specific speaker configuration is assumed.</span></span>

## <a name="remarks"></a><span data-ttu-id="70b3b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="70b3b-111">Remarks</span></span>

<span data-ttu-id="70b3b-112">Você deve definir esse valor como uma das constantes ou valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="70b3b-112">You should set this value to one of the constants or values in the following table.</span></span> <span data-ttu-id="70b3b-113">As constantes são definidas no Microsoft DirectSound e são listadas aqui para sua conveniência.</span><span class="sxs-lookup"><span data-stu-id="70b3b-113">The constants are defined in Microsoft DirectSound, and are listed here for convenience.</span></span> <span data-ttu-id="70b3b-114">Para resolver esses nomes de constantes para seu compilador, você deve incluir dsound. h.</span><span class="sxs-lookup"><span data-stu-id="70b3b-114">To resolve these constant names for your compiler, you must include dsound.h.</span></span>



| <span data-ttu-id="70b3b-115">Constante</span><span class="sxs-lookup"><span data-stu-id="70b3b-115">Constant</span></span>             | <span data-ttu-id="70b3b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="70b3b-116">Value</span></span>      | <span data-ttu-id="70b3b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="70b3b-117">Description</span></span>                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="70b3b-118">DSSPEAKER \_ directout</span><span class="sxs-lookup"><span data-stu-id="70b3b-118">DSSPEAKER\_DIRECTOUT</span></span> | <span data-ttu-id="70b3b-119">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70b3b-119">0x00000000</span></span> | <span data-ttu-id="70b3b-120">O áudio é transmitido diretamente, sem ser configurado para os alto-falantes.</span><span class="sxs-lookup"><span data-stu-id="70b3b-120">The audio is passed through directly, without being configured for speakers.</span></span> |
| <span data-ttu-id="70b3b-121">\_fone de ouvido DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="70b3b-121">DSSPEAKER\_HEADPHONE</span></span> | <span data-ttu-id="70b3b-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="70b3b-122">0x00000001</span></span> | <span data-ttu-id="70b3b-123">O computador cliente está equipado com fones de ouvido.</span><span class="sxs-lookup"><span data-stu-id="70b3b-123">The client computer is equipped with headphones.</span></span>                             |
| <span data-ttu-id="70b3b-124">DSSPEAKER \_ mono</span><span class="sxs-lookup"><span data-stu-id="70b3b-124">DSSPEAKER\_MONO</span></span>      | <span data-ttu-id="70b3b-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="70b3b-125">0x00000002</span></span> | <span data-ttu-id="70b3b-126">O computador cliente está equipado com um monoaural palestrante.</span><span class="sxs-lookup"><span data-stu-id="70b3b-126">The client computer is equipped with a monoaural speaker.</span></span>                    |
| <span data-ttu-id="70b3b-127">DSSPEAKER \_ Quad</span><span class="sxs-lookup"><span data-stu-id="70b3b-127">DSSPEAKER\_QUAD</span></span>      | <span data-ttu-id="70b3b-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="70b3b-128">0x00000003</span></span> | <span data-ttu-id="70b3b-129">O computador cliente está equipado com alto-falantes Quadraphonic.</span><span class="sxs-lookup"><span data-stu-id="70b3b-129">The client computer is equipped with quadraphonic speakers.</span></span>                  |
| <span data-ttu-id="70b3b-130">estéreo de DSSPEAKER \_</span><span class="sxs-lookup"><span data-stu-id="70b3b-130">DSSPEAKER\_STEREO</span></span>    | <span data-ttu-id="70b3b-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="70b3b-131">0x00000004</span></span> | <span data-ttu-id="70b3b-132">O computador cliente está equipado com alto-falantes estéreo.</span><span class="sxs-lookup"><span data-stu-id="70b3b-132">The client computer is equipped with stereo speakers.</span></span>                        |
| <span data-ttu-id="70b3b-133">\_surround DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="70b3b-133">DSSPEAKER\_SURROUND</span></span>  | <span data-ttu-id="70b3b-134">0x00000005</span><span class="sxs-lookup"><span data-stu-id="70b3b-134">0x00000005</span></span> | <span data-ttu-id="70b3b-135">O computador cliente está equipado com alto-falantes surround-sound.</span><span class="sxs-lookup"><span data-stu-id="70b3b-135">The client computer is equipped with four-channel surround-sound speakers.</span></span>   |
| <span data-ttu-id="70b3b-136">DSSPEAKER \_ 5POINT1</span><span class="sxs-lookup"><span data-stu-id="70b3b-136">DSSPEAKER\_5POINT1</span></span>   | <span data-ttu-id="70b3b-137">0x00000006</span><span class="sxs-lookup"><span data-stu-id="70b3b-137">0x00000006</span></span> | <span data-ttu-id="70b3b-138">O computador cliente é equipado com cinco alto-falantes e um subwoofer.</span><span class="sxs-lookup"><span data-stu-id="70b3b-138">The client computer is equipped with five speakers and a subwoofer.</span></span>          |
| <span data-ttu-id="70b3b-139">DSSPEAKER \_ 7POINT1</span><span class="sxs-lookup"><span data-stu-id="70b3b-139">DSSPEAKER\_7POINT1</span></span>   | <span data-ttu-id="70b3b-140">0x00000007</span><span class="sxs-lookup"><span data-stu-id="70b3b-140">0x00000007</span></span> | <span data-ttu-id="70b3b-141">O computador cliente está equipado com sete palestrantes e um subwoofer.</span><span class="sxs-lookup"><span data-stu-id="70b3b-141">The client computer is equipped with seven speakers and a subwoofer.</span></span>         |



 

<span data-ttu-id="70b3b-142">O valor definido para essa propriedade determina os formatos de saída enumerados pelo codec para áudio multicanal.</span><span class="sxs-lookup"><span data-stu-id="70b3b-142">The value set for this property determines the output formats enumerated by the codec for multichannel audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="70b3b-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70b3b-143">Requirements</span></span>



| <span data-ttu-id="70b3b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="70b3b-144">Requirement</span></span> | <span data-ttu-id="70b3b-145">Valor</span><span class="sxs-lookup"><span data-stu-id="70b3b-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70b3b-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70b3b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="70b3b-147">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="70b3b-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="70b3b-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70b3b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="70b3b-149">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="70b3b-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="70b3b-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70b3b-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="70b3b-151"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="70b3b-151"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70b3b-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="70b3b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70b3b-153">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="70b3b-153">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




