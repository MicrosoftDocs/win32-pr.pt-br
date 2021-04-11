---
description: Especifica a estrutura WAVEFORMATEX que descreve o conteúdo de áudio de entrada.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: Propriedade MFPKEY_WMAENC_ORIGWAVEFORMAT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3475e5578124b8f0a762beddf713f701a5695110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165298"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a><span data-ttu-id="eb613-103">\_Propriedade MFPKEY WMAENC \_ ORIGWAVEFORMAT</span><span class="sxs-lookup"><span data-stu-id="eb613-103">MFPKEY\_WMAENC\_ORIGWAVEFORMAT Property</span></span>

<span data-ttu-id="eb613-104">Especifica a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) que descreve o conteúdo de áudio de entrada.</span><span class="sxs-lookup"><span data-stu-id="eb613-104">Specifies the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure describing the input audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="eb613-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="eb613-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="eb613-106">g \_ wszWMACOriginalWaveFormat</span><span class="sxs-lookup"><span data-stu-id="eb613-106">g\_wszWMACOriginalWaveFormat</span></span>

## <a name="data-type"></a><span data-ttu-id="eb613-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="eb613-107">Data Type</span></span>

<span data-ttu-id="eb613-108">\_ \| \_ UI1 da matriz VT ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) como uma matriz de bytes)</span><span class="sxs-lookup"><span data-stu-id="eb613-108">VT\_ARRAY \| VT\_UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) as an array of bytes)</span></span>

## <a name="remarks"></a><span data-ttu-id="eb613-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb613-109">Remarks</span></span>

<span data-ttu-id="eb613-110">Ao transcodificar o conteúdo baseado em áudio do Windows Media para uma taxa de bits inferior, você pode passar a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) do conteúdo para o codec a fim de habilitar o codec para otimizar seus algoritmos.</span><span class="sxs-lookup"><span data-stu-id="eb613-110">When transcoding Windows Media Audio-based content to a lower bit rate, you can pass the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure of the content to the codec to enable the codec to optimize its algorithms.</span></span> <span data-ttu-id="eb613-111">Esse recurso, chamado de recompactação inteligente, fornece resultados melhores do que descompactar o conteúdo e, em seguida, alimentar os exemplos de PCM reconstruídos de volta pelo codec.</span><span class="sxs-lookup"><span data-stu-id="eb613-111">This feature, called smart recompression, provides better results than decompressing the content and then feeding the reconstructed PCM samples back through the codec.</span></span>

<span data-ttu-id="eb613-112">Ao passar a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) , inclua os bytes extras no final da estrutura especificada por **WAVEFORMATEX. cbSize**.</span><span class="sxs-lookup"><span data-stu-id="eb613-112">When passing the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure, include any extra bytes at the end of the structure specified by **WAVEFORMATEX.cbSize**.</span></span>

<span data-ttu-id="eb613-113">O codificador de áudio aceita apenas entradas e saídas para as quais o número de canais, bits por amostra e taxa de amostragem são idênticos.</span><span class="sxs-lookup"><span data-stu-id="eb613-113">The audio encoder accepts only inputs and outputs for which the number of channels, bits per sample, and sample rate are identical.</span></span> <span data-ttu-id="eb613-114">Você pode transcodificar o conteúdo somente para uma taxa de bits inferior dentro desses parâmetros.</span><span class="sxs-lookup"><span data-stu-id="eb613-114">You can transcode content only to a lower bit rate within those parameters.</span></span> <span data-ttu-id="eb613-115">Em qualquer caso, você deve decodificar o conteúdo e passar os exemplos não compactados como entrada para o codificador.</span><span class="sxs-lookup"><span data-stu-id="eb613-115">In any case, you must decode the content and pass the uncompressed samples as input to the encoder.</span></span> <span data-ttu-id="eb613-116">Definir essa propriedade fornece ao codificador algumas informações sobre o processamento que já foi realizado no conteúdo.</span><span class="sxs-lookup"><span data-stu-id="eb613-116">Setting this property gives the encoder some information about the processing that has already been performed on the content.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb613-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb613-117">Requirements</span></span>



| <span data-ttu-id="eb613-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb613-118">Requirement</span></span> | <span data-ttu-id="eb613-119">Valor</span><span class="sxs-lookup"><span data-stu-id="eb613-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb613-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb613-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eb613-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="eb613-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="eb613-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb613-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eb613-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eb613-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eb613-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb613-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb613-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb613-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb613-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb613-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb613-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eb613-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
