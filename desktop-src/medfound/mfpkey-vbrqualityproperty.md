---
description: Especifica o nível de qualidade real para codificação de taxa de bits de variável (VBR) com base na qualidade (1-passagem).
ms.assetid: e45d583a-323b-4394-9df3-949a3f713708
title: Propriedade MFPKEY_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dff57fc27b952780737d63fa8f04faf722ed8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921391"
---
# <a name="mfpkey_vbrquality-property"></a><span data-ttu-id="a5155-103">\_Propriedade MFPKEY VBRQUALITY</span><span class="sxs-lookup"><span data-stu-id="a5155-103">MFPKEY\_VBRQUALITY Property</span></span>

<span data-ttu-id="a5155-104">Especifica o nível de qualidade real para codificação de taxa de bits de variável (VBR) com base na qualidade (1-passagem).</span><span class="sxs-lookup"><span data-stu-id="a5155-104">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a5155-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a5155-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a5155-106">g \_ wszWMVCVBRQuality, g \_ wszWMCPAudioVBRQuality</span><span class="sxs-lookup"><span data-stu-id="a5155-106">g\_wszWMVCVBRQuality, g\_wszWMCPAudioVBRQuality</span></span>

## <a name="data-type"></a><span data-ttu-id="a5155-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="a5155-107">Data Type</span></span>

<span data-ttu-id="a5155-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="a5155-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="a5155-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5155-109">Remarks</span></span>

<span data-ttu-id="a5155-110">Nem todos os valores no intervalo têm um significado exclusivo.</span><span class="sxs-lookup"><span data-stu-id="a5155-110">Not all of the values in the range have a unique meaning.</span></span> <span data-ttu-id="a5155-111">Os valores que representam um Step up na qualidade do nível anterior são: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, e 100.</span><span class="sxs-lookup"><span data-stu-id="a5155-111">The values that represent a step up in quality from the previous level are: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, and 100.</span></span>

<span data-ttu-id="a5155-112">Para objetos do codificador de áudio, os modos de qualidade são fornecidos na estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) dos tipos de saída que você recupera usando [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span><span class="sxs-lookup"><span data-stu-id="a5155-112">For audio encoder objects, the quality modes are provided in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure of the output types that you retrieve using the [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5155-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5155-113">Requirements</span></span>



| <span data-ttu-id="a5155-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5155-114">Requirement</span></span> | <span data-ttu-id="a5155-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a5155-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5155-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5155-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a5155-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a5155-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a5155-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5155-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a5155-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a5155-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a5155-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5155-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5155-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5155-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5155-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5155-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5155-123">Enumerando tipos de áudio para modos de codificação específicos</span><span class="sxs-lookup"><span data-stu-id="a5155-123">Enumerating Audio Types for Specific Encoding Modes</span></span>](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> <dt>

[<span data-ttu-id="a5155-124">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a5155-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
