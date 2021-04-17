---
description: Especifica o grau para o qual o codec deve reduzir o intervalo de cores efetivo do vídeo.
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: Propriedade MFPKEY_RANGEREDUX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec326e5d21a72792aab38f08d8c8c9207ab867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782704"
---
# <a name="mfpkey_rangeredux-property"></a><span data-ttu-id="b3b1f-103">\_Propriedade MFPKEY RANGEREDUX</span><span class="sxs-lookup"><span data-stu-id="b3b1f-103">MFPKEY\_RANGEREDUX Property</span></span>

<span data-ttu-id="b3b1f-104">Especifica o grau para o qual o codec deve reduzir o intervalo de cores efetivo do vídeo.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-104">Specifies the degree to which the codec should reduce the effective color range of the video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b3b1f-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b3b1f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b3b1f-106">g \_ wszWMVCRangeRedux</span><span class="sxs-lookup"><span data-stu-id="b3b1f-106">g\_wszWMVCRangeRedux</span></span>

## <a name="data-type"></a><span data-ttu-id="b3b1f-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="b3b1f-107">Data Type</span></span>

<span data-ttu-id="b3b1f-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="b3b1f-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="b3b1f-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="b3b1f-109">Default Value</span></span>

<span data-ttu-id="b3b1f-110">0</span><span class="sxs-lookup"><span data-stu-id="b3b1f-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="b3b1f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3b1f-111">Remarks</span></span>

<span data-ttu-id="b3b1f-112">A redução de intervalo especifica o grau até o qual o codec deve reduzir o intervalo de Luma e croma do vídeo.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-112">Range reduction specifies the degree to which the codec should reduce luma and chroma range of the video.</span></span> <span data-ttu-id="b3b1f-113">Reduzir o intervalo reduz o tamanho dos quadros de vídeo codificados, mas também reduz os detalhes de cores do vídeo.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-113">Reducing range reduces the size of encoded video frames but also reduces the color detail of the video.</span></span>

<span data-ttu-id="b3b1f-114">A redução de intervalo consiste em redução durante a codificação e a expansão durante a decodificação.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-114">Range reduction consists of reduction during encoding and expansion during decoding.</span></span> <span data-ttu-id="b3b1f-115">É possível tornar os fatores de expansão diferentes dos fatores de redução, mas isso não é recomendado na maioria dos cenários em que o remapeamento de intervalo é útil.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-115">It is possible to make the expansion factors different than the reduction factors, but this is not recommended in most scenarios where range remapping is useful.</span></span>

<span data-ttu-id="b3b1f-116">A redução e a expansão do intervalo são executadas separadamente nos canais Luma e croma.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-116">Range reduction and expansion is performed separately on luma and chroma channels.</span></span> <span data-ttu-id="b3b1f-117">A redução do intervalo pode ser uma maneira eficiente de reduzir a complexidade do vídeo de taxa de bits baixa sem sacrificar os detalhes da imagem.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-117">Reducing range can be an efficient way to reduce the complexity of low bit-rate video without sacrificing image detail.</span></span> <span data-ttu-id="b3b1f-118">Definir todos os quatro valores como 8 reduz a quantidade de informações de Luma e croma pela metade, deixando mais bits a serem direcionados para preservar os detalhes da imagem.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-118">Setting all four values to 8 reduces the amount of luma and chroma information by half, leaving more bits to be directed to preserving image detail.</span></span>

<span data-ttu-id="b3b1f-119">O codec pode optar por usar automaticamente a redução de intervalo ao codificar o vídeo em taxas de bits muito baixas.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-119">The codec can choose to automatically use range reduction when encoding video at very low bit-rates.</span></span> <span data-ttu-id="b3b1f-120">Definir todos os quatro valores como 0 desabilita completamente a redução de intervalo, mesmo em cenários de taxa de bits baixa.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-120">Setting all four values to 0 completely disables range reduction even in low bit-rate scenarios.</span></span>

<span data-ttu-id="b3b1f-121">A redução do intervalo de cores reduz o tamanho codificado dos quadros de vídeo, mas pode introduzir desfoque nos quadros decodificados.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-121">Reducing the color range reduces the encoded size of video frames but can introduce blurriness in the decoded frames.</span></span>

<span data-ttu-id="b3b1f-122">Se essa propriedade não for definida, o codec determinará se a redução de intervalo deve ser usada no momento da codificação.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-122">If this property is not set, the codec determines whether to use range reduction at encoding time.</span></span> <span data-ttu-id="b3b1f-123">Normalmente, essa opção é selecionada pelo codec somente em taxas de bits baixas.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-123">Typically this option is selected by the codec only at low bit rates.</span></span>

<span data-ttu-id="b3b1f-124">O valor dessa propriedade é uma combinação de quatro componentes, separados por zeros, formatados como 0x0M0m0N0n, em que:</span><span class="sxs-lookup"><span data-stu-id="b3b1f-124">The value of this property is a combination of four components, separated by zeros, formatted as 0x0M0m0N0n, where:</span></span>

-   <span data-ttu-id="b3b1f-125">M é o fator de redução do intervalo de codificação para o componente Y.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-125">M is the encoding range reduction factor for the Y component.</span></span>
-   <span data-ttu-id="b3b1f-126">m é o fator de expansão do intervalo de decodificação para o componente Y (geralmente o mesmo que M).</span><span class="sxs-lookup"><span data-stu-id="b3b1f-126">m is the decoding range expansion factor for the Y component (usually the same as M).</span></span>
-   <span data-ttu-id="b3b1f-127">N é o fator de redução do intervalo de codificação para o componente UV.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-127">N is the encoding range reduction factor for the UV component.</span></span>
-   <span data-ttu-id="b3b1f-128">n é o fator de expansão do intervalo de decodificação para o componente UV (geralmente o mesmo que N).</span><span class="sxs-lookup"><span data-stu-id="b3b1f-128">n is the decoding range expansion factor for the UV component (usually the same as N).</span></span>

<span data-ttu-id="b3b1f-129">Cada fator é um dígito de 0 a 8, em que 0 não é uma redução ou expansão e 8 é a redução ou expansão máxima.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-129">Each factor is a digit from 0 to 8, where 0 is no reduction or expansion and 8 is the maximum reduction or expansion.</span></span>

<span data-ttu-id="b3b1f-130">Se você definir o valor como 0x00000000, a redução de intervalo será completamente desabilitada.</span><span class="sxs-lookup"><span data-stu-id="b3b1f-130">If you set the value to 0x00000000, range reduction is completely disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3b1f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3b1f-131">Requirements</span></span>



| <span data-ttu-id="b3b1f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3b1f-132">Requirement</span></span> | <span data-ttu-id="b3b1f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b3b1f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3b1f-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3b1f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b3b1f-135">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b3b1f-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b3b1f-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3b1f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b3b1f-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b3b1f-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3b1f-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3b1f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3b1f-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3b1f-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3b1f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3b1f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3b1f-141">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b3b1f-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




