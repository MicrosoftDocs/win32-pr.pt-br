---
description: Especifica se o decodificador de áudio deve fornecer saída de alta resolução.
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: Propriedade MFPKEY_WMADEC_HIRESOUTPUT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd59bc6b8b0e74be1daaea4a61ca82c810a0ca79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762345"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a><span data-ttu-id="01cf3-103">\_Propriedade MFPKEY WMADEC \_ HIRESOUTPUT</span><span class="sxs-lookup"><span data-stu-id="01cf3-103">MFPKEY\_WMADEC\_HIRESOUTPUT Property</span></span>

<span data-ttu-id="01cf3-104">Especifica se o decodificador de áudio deve fornecer saída de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="01cf3-104">Specifies whether the audio decoder should deliver high-resolution output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="01cf3-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="01cf3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="01cf3-106">g \_ wszWMACHiResOutput</span><span class="sxs-lookup"><span data-stu-id="01cf3-106">g\_wszWMACHiResOutput</span></span>

## <a name="data-type"></a><span data-ttu-id="01cf3-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="01cf3-107">Data Type</span></span>

<span data-ttu-id="01cf3-108">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="01cf3-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="01cf3-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="01cf3-109">Default Value</span></span>

<span data-ttu-id="01cf3-110">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="01cf3-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="01cf3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="01cf3-111">Remarks</span></span>

<span data-ttu-id="01cf3-112">Defina essa propriedade como VARIANT \_ true para decodificar o conteúdo de áudio de multicanais ou de 24 bits, ou áudio com uma taxa de exemplo maior que 48.000 Hz.</span><span class="sxs-lookup"><span data-stu-id="01cf3-112">Set this property to VARIANT\_TRUE to decode multichannel or 24-bit audio content, or audio with a sample rate greater than 48,000 Hz.</span></span> <span data-ttu-id="01cf3-113">Se o conteúdo for codificado em alta resolução, mas essa propriedade for VARIANT \_ false, os seguintes comportamentos se aplicarão:</span><span class="sxs-lookup"><span data-stu-id="01cf3-113">If the content is encoded in high resolution, but this property is VARIANT\_FALSE, the following behaviors apply:</span></span>

-   <span data-ttu-id="01cf3-114">A saída de DMO será limitada a estéreo de 16 bits, 48-KHz.</span><span class="sxs-lookup"><span data-stu-id="01cf3-114">The DMO output will be limited to 16-bit, 48-KHz stereo.</span></span>
-   <span data-ttu-id="01cf3-115">O MFT enumerará modos de saída limitados a 16 bits e não envolverá alterações na contagem de canais ou na taxa de amostragem.</span><span class="sxs-lookup"><span data-stu-id="01cf3-115">The MFT will enumerate output modes that are limited to 16 bits and do not involve changes in channel count or sampling rate.</span></span>

<span data-ttu-id="01cf3-116">As propriedades de áudio de alta resolução são passadas em uma estrutura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) , não [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="01cf3-116">The properties of high-resolution audio are passed in a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure, not [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).</span></span>

<span data-ttu-id="01cf3-117">A saída de alta resolução estará disponível somente se o decodificador estiver em execução no Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="01cf3-117">High-resolution output is available only if the decoder is running on Windows XP or later.</span></span> <span data-ttu-id="01cf3-118">Você pode definir essa propriedade independentemente do sistema operacional no qual seu aplicativo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="01cf3-118">You can set this property regardless of the operating system on which your application is running.</span></span> <span data-ttu-id="01cf3-119">Nas versões do Windows anteriores ao Windows XP, o decodificador ignorará essa configuração e entregará a saída padrão.</span><span class="sxs-lookup"><span data-stu-id="01cf3-119">On versions of Windows earlier than Windows XP, the decoder will ignore this setting and deliver standard output.</span></span>

<span data-ttu-id="01cf3-120">Muitos players (incluindo o Windows Media Player 9 Series e posterior) definem esse valor para todo o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="01cf3-120">Many players (including Windows Media Player 9 Series and later) set this value for all content.</span></span>

## <a name="requirements"></a><span data-ttu-id="01cf3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01cf3-121">Requirements</span></span>



| <span data-ttu-id="01cf3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="01cf3-122">Requirement</span></span> | <span data-ttu-id="01cf3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="01cf3-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01cf3-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01cf3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="01cf3-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="01cf3-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="01cf3-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01cf3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="01cf3-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01cf3-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="01cf3-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01cf3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="01cf3-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="01cf3-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01cf3-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="01cf3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01cf3-131">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01cf3-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
