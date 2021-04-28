---
description: Propriedade MFPKEY_COMPLEXITYEX-especifica a complexidade do algoritmo do codificador.
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: Propriedade MFPKEY_COMPLEXITYEX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20579bcf7a06dc11f47cbef6a53629f3a36b48dc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087603"
---
# <a name="mfpkey_complexityex-property"></a><span data-ttu-id="5f2bc-103">\_Propriedade MFPKEY COMPLEXITYEX</span><span class="sxs-lookup"><span data-stu-id="5f2bc-103">MFPKEY\_COMPLEXITYEX Property</span></span>

<span data-ttu-id="5f2bc-104">Especifica a complexidade do algoritmo do codificador.</span><span class="sxs-lookup"><span data-stu-id="5f2bc-104">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5f2bc-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5f2bc-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5f2bc-106">g \_ wszWMVCComplexityEx</span><span class="sxs-lookup"><span data-stu-id="5f2bc-106">g\_wszWMVCComplexityEx</span></span>

## <a name="data-type"></a><span data-ttu-id="5f2bc-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="5f2bc-107">Data Type</span></span>

<span data-ttu-id="5f2bc-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="5f2bc-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="5f2bc-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="5f2bc-109">Default Value</span></span>

<span data-ttu-id="5f2bc-110">O valor padrão depende da versão do codificador de vídeo, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f2bc-110">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="5f2bc-111">Versão do codificador</span><span class="sxs-lookup"><span data-stu-id="5f2bc-111">Encoder version</span></span>                 | <span data-ttu-id="5f2bc-112">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="5f2bc-112">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="5f2bc-113">Codificador do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="5f2bc-113">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="5f2bc-114">3</span><span class="sxs-lookup"><span data-stu-id="5f2bc-114">3</span></span>             |
| <span data-ttu-id="5f2bc-115">Codificador de vídeo 7/8 do Windows Media</span><span class="sxs-lookup"><span data-stu-id="5f2bc-115">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="5f2bc-116">1</span><span class="sxs-lookup"><span data-stu-id="5f2bc-116">1</span></span>             |



 

## <a name="possible-values"></a><span data-ttu-id="5f2bc-117">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5f2bc-117">Possible Values</span></span>

<span data-ttu-id="5f2bc-118">Os valores possíveis dependem da versão do codificador de vídeo, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f2bc-118">The possible values depend on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="5f2bc-119">Versão do codificador</span><span class="sxs-lookup"><span data-stu-id="5f2bc-119">Encoder version</span></span>                 | <span data-ttu-id="5f2bc-120">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5f2bc-120">Possible values</span></span>  |
|---------------------------------|------------------|
| <span data-ttu-id="5f2bc-121">Codificador do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="5f2bc-121">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="5f2bc-122">0, 1, 2, 3, 4, 5</span><span class="sxs-lookup"><span data-stu-id="5f2bc-122">0, 1, 2, 3, 4, 5</span></span> |
| <span data-ttu-id="5f2bc-123">Codificador de vídeo 7/8 do Windows Media</span><span class="sxs-lookup"><span data-stu-id="5f2bc-123">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="5f2bc-124">0, 1</span><span class="sxs-lookup"><span data-stu-id="5f2bc-124">0, 1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="5f2bc-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f2bc-125">Remarks</span></span>

<span data-ttu-id="5f2bc-126">Valores mais baixos fazem com que o codec use algoritmos de codificação menos complicados.</span><span class="sxs-lookup"><span data-stu-id="5f2bc-126">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="5f2bc-127">Embora os algoritmos mais simples produzam uma saída de qualidade inferior, o processo de codificação é mais rápido e requer menos capacidade de processamento.</span><span class="sxs-lookup"><span data-stu-id="5f2bc-127">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span> <span data-ttu-id="5f2bc-128">Isso pode ser importante ao codificar o conteúdo de uma fonte dinâmica porque o codificador deve processar entradas com rapidez suficiente para acompanhar a origem.</span><span class="sxs-lookup"><span data-stu-id="5f2bc-128">This can be important when encoding content from a live source because the encoder must process inputs fast enough to keep up with the source.</span></span>

<span data-ttu-id="5f2bc-129">Qualquer valor atribuído a essa propriedade será ignorado se a propriedade [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) for definida como 1.</span><span class="sxs-lookup"><span data-stu-id="5f2bc-129">Any value assigned to this property will be ignored if the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property is set to 1.</span></span> <span data-ttu-id="5f2bc-130">Nesse caso, MFPKEY \_ COMPLEXITYEX é definido automaticamente como 3.</span><span class="sxs-lookup"><span data-stu-id="5f2bc-130">In that case, MFPKEY\_COMPLEXITYEX is automatically set to 3.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f2bc-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f2bc-131">Requirements</span></span>



| <span data-ttu-id="5f2bc-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f2bc-132">Requirement</span></span> | <span data-ttu-id="5f2bc-133">Valor</span><span class="sxs-lookup"><span data-stu-id="5f2bc-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f2bc-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f2bc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5f2bc-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f2bc-135">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5f2bc-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f2bc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5f2bc-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5f2bc-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f2bc-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f2bc-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f2bc-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f2bc-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f2bc-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5f2bc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f2bc-141">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5f2bc-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




