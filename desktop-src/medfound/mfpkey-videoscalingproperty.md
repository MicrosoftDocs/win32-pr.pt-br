---
description: Especifica se o codec usará a otimização de escala de vídeo.
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: Propriedade MFPKEY_VIDEOSCALING (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555cec22533b7817c509d5419391039b10c92576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827821"
---
# <a name="mfpkey_videoscaling-property"></a><span data-ttu-id="cac67-103">\_Propriedade MFPKEY VIDEOSCALING</span><span class="sxs-lookup"><span data-stu-id="cac67-103">MFPKEY\_VIDEOSCALING Property</span></span>

<span data-ttu-id="cac67-104">Especifica se o codec usará a otimização de escala de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cac67-104">Specifies whether the codec will use video scaling optimization.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="cac67-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="cac67-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="cac67-106">g \_ wszWMVCVideoScaling</span><span class="sxs-lookup"><span data-stu-id="cac67-106">g\_wszWMVCVideoScaling</span></span>

## <a name="data-type"></a><span data-ttu-id="cac67-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="cac67-107">Data Type</span></span>

<span data-ttu-id="cac67-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="cac67-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="cac67-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="cac67-109">Default Value</span></span>

<span data-ttu-id="cac67-110">0</span><span class="sxs-lookup"><span data-stu-id="cac67-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="cac67-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cac67-111">Remarks</span></span>

<span data-ttu-id="cac67-112">O dimensionamento de vídeo é um tipo de otimização perceptiva que pode melhorar a qualidade visual do vídeo codificado em taxas de bits baixas.</span><span class="sxs-lookup"><span data-stu-id="cac67-112">Video scaling is a type of perceptual optimization that can improve the visual quality of video encoded at low bit rates.</span></span> <span data-ttu-id="cac67-113">A otimização de escala de vídeo reduz os artefatos pronunciados, mas pode sacrificar os detalhes da imagem.</span><span class="sxs-lookup"><span data-stu-id="cac67-113">The video scaling optimization reduces pronounced artifacts, but can sacrifice image detail.</span></span> <span data-ttu-id="cac67-114">Essa otimização afeta o intervalo Luma do vídeo codificado conforme descrito abaixo, mas não afeta a resolução física do vídeo de saída.</span><span class="sxs-lookup"><span data-stu-id="cac67-114">This optimization affects the luma range of the encoded video as described below but does not affect the physical resolution of the output video.</span></span>

<span data-ttu-id="cac67-115">Essa propriedade pode ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="cac67-115">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="cac67-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cac67-116">Value</span></span> | <span data-ttu-id="cac67-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="cac67-117">Description</span></span>                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac67-118">0</span><span class="sxs-lookup"><span data-stu-id="cac67-118">0</span></span>     | <span data-ttu-id="cac67-119">O dimensionamento de vídeo não será usado.</span><span class="sxs-lookup"><span data-stu-id="cac67-119">Video scaling will not be used.</span></span>                                                                                       |
| <span data-ttu-id="cac67-120">1</span><span class="sxs-lookup"><span data-stu-id="cac67-120">1</span></span>     | <span data-ttu-id="cac67-121">O codificador usará otimização de escala de vídeo conservadora.</span><span class="sxs-lookup"><span data-stu-id="cac67-121">The encoder will use conservative video scaling optimization.</span></span> <span data-ttu-id="cac67-122">O intervalo de Luma será dimensionado de 0... 255 para 26... 229.</span><span class="sxs-lookup"><span data-stu-id="cac67-122">The luma range will be scaled from 0...255 to 26...229.</span></span> |
| <span data-ttu-id="cac67-123">2</span><span class="sxs-lookup"><span data-stu-id="cac67-123">2</span></span>     | <span data-ttu-id="cac67-124">O codificador usará otimização agressiva de escala de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cac67-124">The encoder will use aggressive video scaling optimization.</span></span> <span data-ttu-id="cac67-125">O intervalo de Luma será dimensionado de 0... 255 para 31... 224.</span><span class="sxs-lookup"><span data-stu-id="cac67-125">The luma range will be scaled from 0...255 to 31...224.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="cac67-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cac67-126">Requirements</span></span>



| <span data-ttu-id="cac67-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cac67-127">Requirement</span></span> | <span data-ttu-id="cac67-128">Valor</span><span class="sxs-lookup"><span data-stu-id="cac67-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cac67-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cac67-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cac67-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cac67-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cac67-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cac67-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cac67-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cac67-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cac67-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cac67-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cac67-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cac67-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cac67-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="cac67-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac67-136">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cac67-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




