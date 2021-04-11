---
description: Especifica uma altura intermediária de quadro para vídeo codificado.
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: Propriedade MFPKEY_FORCEFRAMEHEIGHT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e4662ce56ea4c20d44abdd05641219bc6b94ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165392"
---
# <a name="mfpkey_forceframeheight-property"></a><span data-ttu-id="538b2-103">\_Propriedade MFPKEY FORCEFRAMEHEIGHT</span><span class="sxs-lookup"><span data-stu-id="538b2-103">MFPKEY\_FORCEFRAMEHEIGHT Property</span></span>

<span data-ttu-id="538b2-104">Especifica uma altura intermediária de quadro para vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="538b2-104">Specifies an intermediate frame height for encoded video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="538b2-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="538b2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="538b2-106">g \_ wszWMVCForceFrameHeight</span><span class="sxs-lookup"><span data-stu-id="538b2-106">g\_wszWMVCForceFrameHeight</span></span>

## <a name="data-type"></a><span data-ttu-id="538b2-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="538b2-107">Data Type</span></span>

<span data-ttu-id="538b2-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="538b2-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="538b2-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="538b2-109">Remarks</span></span>

<span data-ttu-id="538b2-110">Você pode definir esse valor e a propriedade [MFPKEY \_ FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md) para forçar o codificador a codificar o fluxo de vídeo com um tamanho de quadro menor do que os tamanhos de quadro de entrada ou de saída.</span><span class="sxs-lookup"><span data-stu-id="538b2-110">You can set this value and the [MFPKEY\_FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md) property to force the encoder to encode the video stream with a frame size that is smaller than the input or output frame sizes.</span></span> <span data-ttu-id="538b2-111">Quando decodificado, o vídeo será redimensionado para sua resolução de entrada original.</span><span class="sxs-lookup"><span data-stu-id="538b2-111">When decoded, the video will be resized to its original input resolution.</span></span>

<span data-ttu-id="538b2-112">As dimensões de quadro válidas em qualquer eixo são de 2 a 8192 pixels.</span><span class="sxs-lookup"><span data-stu-id="538b2-112">Valid frame dimensions on either axis are 2 to 8192 pixels.</span></span> <span data-ttu-id="538b2-113">As dimensões do quadro devem ser divisíveis por 2.</span><span class="sxs-lookup"><span data-stu-id="538b2-113">Frame dimensions must be divisible by 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="538b2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="538b2-114">Requirements</span></span>



| <span data-ttu-id="538b2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="538b2-115">Requirement</span></span> | <span data-ttu-id="538b2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="538b2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="538b2-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="538b2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="538b2-118">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="538b2-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="538b2-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="538b2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="538b2-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="538b2-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="538b2-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="538b2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="538b2-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="538b2-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="538b2-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="538b2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="538b2-124">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="538b2-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




