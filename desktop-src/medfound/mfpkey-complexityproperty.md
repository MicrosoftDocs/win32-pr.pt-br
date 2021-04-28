---
description: Propriedade MFPKEY_COMPLEXITY-especifica a complexidade do algoritmo do codificador.
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: Propriedade MFPKEY_COMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042e3158b43efb5a4a82542f000d137fa0c195e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092934"
---
# <a name="mfpkey_complexity-property"></a><span data-ttu-id="62492-103">\_Propriedade de complexidade MFPKEY</span><span class="sxs-lookup"><span data-stu-id="62492-103">MFPKEY\_COMPLEXITY Property</span></span>

<span data-ttu-id="62492-104">\[[**MFPKEY \_ A complexidade**](mfpkey-complexityexproperty.md) está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="62492-104">\[[**MFPKEY\_COMPLEXITY**](mfpkey-complexityexproperty.md) is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="62492-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="62492-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="62492-106">Em vez disso, use **MFPKEY \_ COMPLEXITYEX**.\]</span><span class="sxs-lookup"><span data-stu-id="62492-106">Instead, use **MFPKEY\_COMPLEXITYEX**.\]</span></span>

<span data-ttu-id="62492-107">Especifica a complexidade do algoritmo do codificador.</span><span class="sxs-lookup"><span data-stu-id="62492-107">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="62492-108">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="62492-108">Constant for IPropertyBag</span></span>

<span data-ttu-id="62492-109">g \_ wszWMVCComplexityMode</span><span class="sxs-lookup"><span data-stu-id="62492-109">g\_wszWMVCComplexityMode</span></span>

## <a name="data-type"></a><span data-ttu-id="62492-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="62492-110">Data Type</span></span>

<span data-ttu-id="62492-111">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="62492-111">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="62492-112">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="62492-112">Default Value</span></span>

<span data-ttu-id="62492-113">O valor padrão depende da versão do codificador de vídeo, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="62492-113">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="62492-114">Versão do codificador</span><span class="sxs-lookup"><span data-stu-id="62492-114">Encoder version</span></span>                 | <span data-ttu-id="62492-115">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="62492-115">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="62492-116">Codificador do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="62492-116">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="62492-117">3</span><span class="sxs-lookup"><span data-stu-id="62492-117">3</span></span>             |
| <span data-ttu-id="62492-118">Codificador de vídeo 7/8 do Windows Media</span><span class="sxs-lookup"><span data-stu-id="62492-118">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="62492-119">1</span><span class="sxs-lookup"><span data-stu-id="62492-119">1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="62492-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="62492-120">Remarks</span></span>

<span data-ttu-id="62492-121">Esse valor inteiro varia de 0 a 3.</span><span class="sxs-lookup"><span data-stu-id="62492-121">This integer value ranges from 0 to 3.</span></span> <span data-ttu-id="62492-122">Valores mais baixos fazem com que o codec use algoritmos de codificação menos complicados.</span><span class="sxs-lookup"><span data-stu-id="62492-122">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="62492-123">Embora os algoritmos mais simples produzam uma saída de qualidade inferior, o processo de codificação é mais rápido e requer menos capacidade de processamento.</span><span class="sxs-lookup"><span data-stu-id="62492-123">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span>

## <a name="requirements"></a><span data-ttu-id="62492-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62492-124">Requirements</span></span>



| <span data-ttu-id="62492-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="62492-125">Requirement</span></span> | <span data-ttu-id="62492-126">Valor</span><span class="sxs-lookup"><span data-stu-id="62492-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62492-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62492-127">Minimum supported client</span></span><br/> | <span data-ttu-id="62492-128">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="62492-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="62492-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62492-129">Minimum supported server</span></span><br/> | <span data-ttu-id="62492-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62492-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62492-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62492-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="62492-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="62492-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62492-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="62492-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62492-134">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62492-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




