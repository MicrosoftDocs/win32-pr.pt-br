---
description: Propriedade MFPKEY_COLORCONV_MODE-especifica se o fluxo de entrada está entrelaçado.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: Propriedade MFPKEY_COLORCONV_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3f2d6256c4d7a9410264fb18703eea251e9c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087574"
---
# <a name="mfpkey_colorconv_mode-property"></a><span data-ttu-id="4ca82-103">\_Propriedade do \_ modo MFPKEY COLORCONV</span><span class="sxs-lookup"><span data-stu-id="4ca82-103">MFPKEY\_COLORCONV\_MODE Property</span></span>

<span data-ttu-id="4ca82-104">Especifica se o fluxo de entrada está entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="4ca82-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4ca82-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="4ca82-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="4ca82-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="4ca82-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="4ca82-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="4ca82-107">Data Type</span></span>

<span data-ttu-id="4ca82-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="4ca82-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="4ca82-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="4ca82-109">Default Value</span></span>

<span data-ttu-id="4ca82-110">Computado pelo DSP do vídeo de origem.</span><span class="sxs-lookup"><span data-stu-id="4ca82-110">Computed by the DSP from the source video.</span></span>

## <a name="applies-to"></a><span data-ttu-id="4ca82-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="4ca82-111">Applies To</span></span>

-   [<span data-ttu-id="4ca82-112">DSP de conversor de cores</span><span class="sxs-lookup"><span data-stu-id="4ca82-112">Color Converter DSP</span></span>](colorconverter.md)

## <a name="remarks"></a><span data-ttu-id="4ca82-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ca82-113">Remarks</span></span>

<span data-ttu-id="4ca82-114">Use um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ca82-114">Use one of the following values.</span></span>



| <span data-ttu-id="4ca82-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4ca82-115">Value</span></span> | <span data-ttu-id="4ca82-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ca82-116">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="4ca82-117">0</span><span class="sxs-lookup"><span data-stu-id="4ca82-117">0</span></span>     | <span data-ttu-id="4ca82-118">Progressivo</span><span class="sxs-lookup"><span data-stu-id="4ca82-118">Progressive</span></span> |
| <span data-ttu-id="4ca82-119">2</span><span class="sxs-lookup"><span data-stu-id="4ca82-119">2</span></span>     | <span data-ttu-id="4ca82-120">Interlaced</span><span class="sxs-lookup"><span data-stu-id="4ca82-120">Interlaced</span></span>  |



 

<span data-ttu-id="4ca82-121">Se essa propriedade não for definida, o DSP usará o tipo de mídia de entrada para determinar se o vídeo está entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="4ca82-121">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="4ca82-122">Você pode definir essa propriedade para substituir a configuração do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="4ca82-122">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ca82-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ca82-123">Requirements</span></span>



| <span data-ttu-id="4ca82-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ca82-124">Requirement</span></span> | <span data-ttu-id="4ca82-125">Valor</span><span class="sxs-lookup"><span data-stu-id="4ca82-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca82-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ca82-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4ca82-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4ca82-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4ca82-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ca82-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4ca82-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4ca82-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4ca82-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ca82-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ca82-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ca82-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ca82-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4ca82-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca82-133">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4ca82-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
