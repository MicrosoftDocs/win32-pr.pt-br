---
description: Especifica o número de quadros de previsão bidirecionais (quadros B).
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: Propriedade MFPKEY_NUMBFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3b0655a4a5e24b92f9699b198f10232de8edf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748919"
---
# <a name="mfpkey_numbframes-property"></a><span data-ttu-id="3caa8-103">\_Propriedade MFPKEY NUMBFRAMES</span><span class="sxs-lookup"><span data-stu-id="3caa8-103">MFPKEY\_NUMBFRAMES Property</span></span>

<span data-ttu-id="3caa8-104">Especifica o número de quadros de previsão bidirecionais (quadros B).</span><span class="sxs-lookup"><span data-stu-id="3caa8-104">Specifies the number of bidirectional predictive frames (B-frames).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3caa8-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3caa8-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3caa8-106">g \_ wszWMVCNumBFrames</span><span class="sxs-lookup"><span data-stu-id="3caa8-106">g\_wszWMVCNumBFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="3caa8-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="3caa8-107">Data Type</span></span>

<span data-ttu-id="3caa8-108">VT-I4</span><span class="sxs-lookup"><span data-stu-id="3caa8-108">VT-I4</span></span>

## <a name="default-value"></a><span data-ttu-id="3caa8-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="3caa8-109">Default Value</span></span>

<span data-ttu-id="3caa8-110">0</span><span class="sxs-lookup"><span data-stu-id="3caa8-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="3caa8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3caa8-111">Remarks</span></span>

<span data-ttu-id="3caa8-112">Por padrão, o Windows Media Video 9 usa apenas intraframes (I-frames), também conhecido como quadros-chave ou quadros de ancoragem, que são quadros totalmente codificados e quadros de previsão (quadros P), que são codificados como uma diferença do I-frame anterior.</span><span class="sxs-lookup"><span data-stu-id="3caa8-112">By default, Windows Media Video 9 uses only intraframes (I-frames), also known as key frames or anchor frames, which are fully encoded frames, and predictive frames (P-frames), which are encoded as a difference from the previous I-frame.</span></span> <span data-ttu-id="3caa8-113">Os quadros B são diferentes dos quadros P porque armazenam as diferenças do quadro anterior e as diferenças do quadro a seguir.</span><span class="sxs-lookup"><span data-stu-id="3caa8-113">B-frames are different from P-frames because they store both the differences from the previous frame and the differences from the following frame.</span></span>

<span data-ttu-id="3caa8-114">Quando você configura o codec para usar os quadros B, ele usará o número especificado de quadros B entre cada par de quadros do tipo I ou P.</span><span class="sxs-lookup"><span data-stu-id="3caa8-114">When you configure the codec to uses B-frames, it will use the specified number of B-frames between each pair of frames of either I or P type.</span></span>

<span data-ttu-id="3caa8-115">Por exemplo, se uma sequência de quadros sem quadros B for "IPPPPPPPPI", a mesma codificação de sequência com dois quadros B seria "IBBPBBPBBI".</span><span class="sxs-lookup"><span data-stu-id="3caa8-115">For example, if a sequence of frames without B-frames is "IPPPPPPPPI" then the same sequence encoding with two B-frames would be "IBBPBBPBBI".</span></span>

<span data-ttu-id="3caa8-116">Para a maior parte do conteúdo, um ou dois quadros B são apropriados.</span><span class="sxs-lookup"><span data-stu-id="3caa8-116">For most content either one or two B-frames are appropriate.</span></span> <span data-ttu-id="3caa8-117">Em taxas de dados mais altas, um quadro B normalmente é a melhor opção.</span><span class="sxs-lookup"><span data-stu-id="3caa8-117">At higher data rates, one B-frame is normally the optimal choice.</span></span> <span data-ttu-id="3caa8-118">Três ou mais raramente são úteis.</span><span class="sxs-lookup"><span data-stu-id="3caa8-118">Three or more are rarely useful.</span></span>

<span data-ttu-id="3caa8-119">O intervalo válido de valores para essa propriedade é de 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="3caa8-119">The valid range of values for this property is 0 to 7.</span></span>

## <a name="requirements"></a><span data-ttu-id="3caa8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3caa8-120">Requirements</span></span>



| <span data-ttu-id="3caa8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3caa8-121">Requirement</span></span> | <span data-ttu-id="3caa8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3caa8-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3caa8-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3caa8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3caa8-124">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3caa8-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3caa8-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3caa8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3caa8-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3caa8-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3caa8-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3caa8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3caa8-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3caa8-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3caa8-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="3caa8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3caa8-130">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3caa8-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




