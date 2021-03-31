---
description: Especifica se o fluxo de entrada está entrelaçado.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: Propriedade MFPKEY_COLORCONV_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8c01a6dce595eb270b734947492deea014259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661880"
---
# <a name="mfpkey_colorconv_mode-property"></a><span data-ttu-id="be257-103">\_Propriedade do \_ modo MFPKEY COLORCONV</span><span class="sxs-lookup"><span data-stu-id="be257-103">MFPKEY\_COLORCONV\_MODE Property</span></span>

<span data-ttu-id="be257-104">Especifica se o fluxo de entrada está entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="be257-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="be257-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="be257-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="be257-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="be257-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="be257-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="be257-107">Data Type</span></span>

<span data-ttu-id="be257-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="be257-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="be257-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="be257-109">Default Value</span></span>

<span data-ttu-id="be257-110">Computado pelo DSP do vídeo de origem.</span><span class="sxs-lookup"><span data-stu-id="be257-110">Computed by the DSP from the source video.</span></span>

## <a name="applies-to"></a><span data-ttu-id="be257-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="be257-111">Applies To</span></span>

-   [<span data-ttu-id="be257-112">DSP de conversor de cores</span><span class="sxs-lookup"><span data-stu-id="be257-112">Color Converter DSP</span></span>](colorconverter.md)

## <a name="remarks"></a><span data-ttu-id="be257-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="be257-113">Remarks</span></span>

<span data-ttu-id="be257-114">Use um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="be257-114">Use one of the following values.</span></span>



| <span data-ttu-id="be257-115">Valor</span><span class="sxs-lookup"><span data-stu-id="be257-115">Value</span></span> | <span data-ttu-id="be257-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="be257-116">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="be257-117">0</span><span class="sxs-lookup"><span data-stu-id="be257-117">0</span></span>     | <span data-ttu-id="be257-118">Progressivo</span><span class="sxs-lookup"><span data-stu-id="be257-118">Progressive</span></span> |
| <span data-ttu-id="be257-119">2</span><span class="sxs-lookup"><span data-stu-id="be257-119">2</span></span>     | <span data-ttu-id="be257-120">Interlaced</span><span class="sxs-lookup"><span data-stu-id="be257-120">Interlaced</span></span>  |



 

<span data-ttu-id="be257-121">Se essa propriedade não for definida, o DSP usará o tipo de mídia de entrada para determinar se o vídeo está entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="be257-121">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="be257-122">Você pode definir essa propriedade para substituir a configuração do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="be257-122">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="be257-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be257-123">Requirements</span></span>



| <span data-ttu-id="be257-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="be257-124">Requirement</span></span> | <span data-ttu-id="be257-125">Valor</span><span class="sxs-lookup"><span data-stu-id="be257-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be257-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be257-126">Minimum supported client</span></span><br/> | <span data-ttu-id="be257-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="be257-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="be257-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be257-128">Minimum supported server</span></span><br/> | <span data-ttu-id="be257-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be257-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="be257-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be257-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="be257-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="be257-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be257-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="be257-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be257-133">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="be257-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
