---
description: Especifica se o codec deve usar a filtragem mediana durante a codificação.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: Propriedade MFPKEY_FORCEMEDIANSETTING (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d0aa154798e2ed42a7373a6e85a4b46f8eeb7b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837657"
---
# <a name="mfpkey_forcemediansetting-property"></a><span data-ttu-id="51e36-103">\_Propriedade MFPKEY FORCEMEDIANSETTING</span><span class="sxs-lookup"><span data-stu-id="51e36-103">MFPKEY\_FORCEMEDIANSETTING Property</span></span>

<span data-ttu-id="51e36-104">Especifica se o codec deve usar a filtragem mediana durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="51e36-104">Specifies whether the codec should use median filtering during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="51e36-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="51e36-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="51e36-106">g \_ wszWMVCForceMedianSetting</span><span class="sxs-lookup"><span data-stu-id="51e36-106">g\_wszWMVCForceMedianSetting</span></span>

## <a name="data-type"></a><span data-ttu-id="51e36-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="51e36-107">Data Type</span></span>

<span data-ttu-id="51e36-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="51e36-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="51e36-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="51e36-109">Default Value</span></span>

<span data-ttu-id="51e36-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="51e36-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="51e36-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="51e36-111">Remarks</span></span>

<span data-ttu-id="51e36-112">A filtragem mediana informa o codec para ignorar o ruído e a granulação ao calcular o movimento entre os quadros.</span><span class="sxs-lookup"><span data-stu-id="51e36-112">Median filtering tells the codec to ignore noise and grain when calculating motion between frames.</span></span> <span data-ttu-id="51e36-113">Isso pode melhorar a qualidade de vídeo muito ruidosa, mas pode levar a trilhas de movimento (também conhecidas como artefatos à direita) quando aplicado a um vídeo de origem limpo.</span><span class="sxs-lookup"><span data-stu-id="51e36-113">This can improve the quality of very noisy video, but can lead to motion trails (also known as trailing artifacts) when applied to clean source video.</span></span>

<span data-ttu-id="51e36-114">Por padrão, o codec usa a lógica interna para determinar se a filtragem mediana deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="51e36-114">By default, the codec uses internal logic to determine whether median filtering should be used.</span></span> <span data-ttu-id="51e36-115">Se você definir essa propriedade, essa lógica será substituída.</span><span class="sxs-lookup"><span data-stu-id="51e36-115">If you set this property, that logic will be overridden.</span></span>

> [!Note]  
> <span data-ttu-id="51e36-116">Esse filtro não é o mesmo que os filtros de desfoque medianos encontrados em muitos aplicativos de processamento de vídeo e pós-processamento.</span><span class="sxs-lookup"><span data-stu-id="51e36-116">This filter is not the same as median blur filters found in many video editing and post-processing applications.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="51e36-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51e36-117">Requirements</span></span>



| <span data-ttu-id="51e36-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="51e36-118">Requirement</span></span> | <span data-ttu-id="51e36-119">Valor</span><span class="sxs-lookup"><span data-stu-id="51e36-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51e36-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51e36-120">Minimum supported client</span></span><br/> | <span data-ttu-id="51e36-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="51e36-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="51e36-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51e36-122">Minimum supported server</span></span><br/> | <span data-ttu-id="51e36-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51e36-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="51e36-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51e36-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="51e36-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="51e36-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51e36-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="51e36-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51e36-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="51e36-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




