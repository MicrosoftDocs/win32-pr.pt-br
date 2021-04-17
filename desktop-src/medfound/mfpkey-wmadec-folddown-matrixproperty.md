---
description: Especifica os coeficientes de dobra fornecidos pelo autor para decodificação de áudio multicanal para menos canais do que o fluxo codificado contém.
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: Propriedade MFPKEY_WMADEC_FOLDDOWN_MATRIX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92cb2495863d319c7f755d7d72f475ccf1eda75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766504"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a><span data-ttu-id="c4c1f-103">\_Propriedade MFPKEY WMADEC \_ FOLDDOWN \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="c4c1f-103">MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX Property</span></span>

<span data-ttu-id="c4c1f-104">Especifica os coeficientes de dobra fornecidos pelo autor para decodificação de áudio multicanal para menos canais do que o fluxo codificado contém.</span><span class="sxs-lookup"><span data-stu-id="c4c1f-104">Specifies the author-supplied fold-down coefficients for decoding multichannel audio for fewer channels than the encoded stream contains.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c4c1f-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c4c1f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c4c1f-106">g \_ wszWMACFoldDownXToYChannels</span><span class="sxs-lookup"><span data-stu-id="c4c1f-106">g\_wszWMACFoldDownXToYChannels</span></span>

<span data-ttu-id="c4c1f-107">g \_ wszWMACFoldXToYChannelsZ</span><span class="sxs-lookup"><span data-stu-id="c4c1f-107">g\_wszWMACFoldXToYChannelsZ</span></span>

## <a name="data-type"></a><span data-ttu-id="c4c1f-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="c4c1f-108">Data Type</span></span>

<span data-ttu-id="c4c1f-109">**\_I4 da matriz VT \| \_**</span><span class="sxs-lookup"><span data-stu-id="c4c1f-109">**VT\_ARRAY \| VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="c4c1f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4c1f-110">Remarks</span></span>

<span data-ttu-id="c4c1f-111">Um decodificador de áudio pode atuar como um objeto de mídia DirectX (DMO) ou como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="c4c1f-111">An audio decoder can act as a DirectX Media Object (DMO) or as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="c4c1f-112">Para obter informações sobre quando um decodificador atua como um DMO ou uma MFT, consulte as páginas de referência do codec individual em [objetos de codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="c4c1f-112">For information on when a decoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="c4c1f-113">Quando você usa um decodificador como DMO, o decodificador pode executar a dobra do canal e você pode enumerar os tipos de mídia de saída dobrados, chamando [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span><span class="sxs-lookup"><span data-stu-id="c4c1f-113">When you use a decoder as a DMO, the decoder can perform channel fold down, and you can enumerate folded down output media types by calling [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span></span>

<span data-ttu-id="c4c1f-114">Quando você usa um decodificador como um MFT, o decodificador por padrão não executará nenhuma dobra para baixo e não oferecerá tipos de mídia de saída dobrados.</span><span class="sxs-lookup"><span data-stu-id="c4c1f-114">When you use a decoder as an MFT, the decoder by default will not perform any fold down, and will not offer folded down output media types.</span></span> <span data-ttu-id="c4c1f-115">Um decodificador agindo como MFT executará a dobra somente se os coeficientes de dobra personalizada forem definidos usando a propriedade de **\_ \_ \_ matriz MFPKEY WMADEC FOLDDOWN** .</span><span class="sxs-lookup"><span data-stu-id="c4c1f-115">A decoder acting as an MFT will perform fold down only if custom fold-down coefficients are set using the **MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX** property.</span></span>

<span data-ttu-id="c4c1f-116">Se a propriedade **MFPKEY \_ WMADEC \_ FOLDDOWN \_ Matrix** não estiver definida na MFT do decodificador de áudio e você desejar executar uma dobra, poderá usar (como MFT) o processador de sinal digital do reamostrador de áudio.</span><span class="sxs-lookup"><span data-stu-id="c4c1f-116">If the **MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX** property is not set on the audio decoder MFT, and you want to perform a fold down, you can use (as an MFT) the Audio Resampler digital signal processor.</span></span>

<span data-ttu-id="c4c1f-117">O valor dessa propriedade é uma cadeia de caracteres que contém coeficientes dobrados em uma lista separada por vírgulas de valores inteiros.</span><span class="sxs-lookup"><span data-stu-id="c4c1f-117">The value for this property is a string containing fold-down coefficients in a comma-separated list of integer values.</span></span> <span data-ttu-id="c4c1f-118">A lista deve conter um número de inteiros para cada canal no conteúdo codificado igual ao número de canais no conteúdo decodificado.</span><span class="sxs-lookup"><span data-stu-id="c4c1f-118">The list must contain a number of integers for each channel in the encoded content equal to the number of channels in the decoded content.</span></span>

<span data-ttu-id="c4c1f-119">Se o coeficiente for zero, o valor a ser usado na cadeia de caracteres deverá ser "-2147483648"; caso contrário, o valor será computado usando a equação: 20 \* 65536 \* log10 (x).</span><span class="sxs-lookup"><span data-stu-id="c4c1f-119">If the coefficient is zero, the value to be used in the string must be "-2147483648";otherwise the value is computed using the equation: 20 \* 65536 \* log10(x).</span></span>

<span data-ttu-id="c4c1f-120">Os coeficientes são listados na ordem de máscara de canal, conforme definido pelas constantes de máscara de canal que são incluídas no arquivo de cabeçalho Mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="c4c1f-120">Coefficients are listed in channel mask order, as defined by the channel mask constants that are included in the mmreg.h header file.</span></span> <span data-ttu-id="c4c1f-121">Portanto, os dois primeiros valores em uma dobra de canal de 6 para 2 representam as partes do canal de saída à esquerda e o canal de saída à direita que são compostos do canal Center esquerdo no fluxo de 6 canais.</span><span class="sxs-lookup"><span data-stu-id="c4c1f-121">Therefore, the first two values in a 6-to-2 channel fold-down represent the portions of the left output channel and the right output channel that are made up of the center left channel in the 6 channel stream.</span></span>

<span data-ttu-id="c4c1f-122">Você deve definir essa propriedade somente se os valores de dobra fornecidos pelo autor forem persistidos com o conteúdo codificado.</span><span class="sxs-lookup"><span data-stu-id="c4c1f-122">You should set this property only if author-supplied fold-down values are persisted with the encoded content.</span></span> <span data-ttu-id="c4c1f-123">Caso contrário, permita que o decodificador faça seus próprios cálculos.</span><span class="sxs-lookup"><span data-stu-id="c4c1f-123">Otherwise, let the decoder make its own calculations.</span></span>

<span data-ttu-id="c4c1f-124">O codec Windows Media Audio 10 Professional atualmente dá suporte apenas à dobra para dois canais.</span><span class="sxs-lookup"><span data-stu-id="c4c1f-124">The Windows Media Audio 10 Professional codec currently only supports fold-down to two channels.</span></span>

<span data-ttu-id="c4c1f-125">Se a propriedade [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) for definida como **DSSPEAKER \_ surround**, o codec ignorará os coeficientes de dobrado fornecidos pelo autor e dobrará para um sinal de 2 canais que pode ser processado pelo decodificador de matriz do receptor.</span><span class="sxs-lookup"><span data-stu-id="c4c1f-125">If the [MFPKEY\_WMADEC\_SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) property is set to **DSSPEAKER\_SURROUND**, the codec will ignore author-supplied fold-down coefficients and fold down to a 2-channel signal that can be processed by the matrix decoder of the receiver.</span></span> <span data-ttu-id="c4c1f-126">Isso permite que o equipamento surround forneça quatro canais.</span><span class="sxs-lookup"><span data-stu-id="c4c1f-126">This enables surround equipment to deliver four channels.</span></span> <span data-ttu-id="c4c1f-127">Esse modo só terá suporte se a origem for 5,1.</span><span class="sxs-lookup"><span data-stu-id="c4c1f-127">This mode is supported only if the source is 5.1.</span></span> <span data-ttu-id="c4c1f-128">O codec só pode dobrar 8 canais para 2 canais.</span><span class="sxs-lookup"><span data-stu-id="c4c1f-128">The codec can only fold 8 channels to 2 channels.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4c1f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4c1f-129">Requirements</span></span>



| <span data-ttu-id="c4c1f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4c1f-130">Requirement</span></span> | <span data-ttu-id="c4c1f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c4c1f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c1f-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4c1f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c4c1f-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c4c1f-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c4c1f-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4c1f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c4c1f-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c4c1f-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c4c1f-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4c1f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4c1f-137"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4c1f-137"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4c1f-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4c1f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4c1f-139">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c4c1f-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
