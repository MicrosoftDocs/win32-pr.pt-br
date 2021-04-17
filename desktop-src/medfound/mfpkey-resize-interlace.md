---
description: Especifica se o fluxo de entrada está entrelaçado.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: Propriedade MFPKEY_RESIZE_INTERLACE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a27504bd6da92bc48fee04afc999568a514fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754914"
---
# <a name="mfpkey_resize_interlace-property"></a><span data-ttu-id="e5246-103">MFPKEY \_ redimensionar \_ Propriedade entrelaçar</span><span class="sxs-lookup"><span data-stu-id="e5246-103">MFPKEY\_RESIZE\_INTERLACE Property</span></span>

<span data-ttu-id="e5246-104">Especifica se o fluxo de entrada está entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="e5246-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e5246-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e5246-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e5246-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="e5246-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="e5246-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="e5246-107">Data Type</span></span>

<span data-ttu-id="e5246-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="e5246-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="e5246-109">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="e5246-109">Applies To</span></span>

-   [<span data-ttu-id="e5246-110">DSP de redimensionador de vídeo</span><span class="sxs-lookup"><span data-stu-id="e5246-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="e5246-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5246-111">Remarks</span></span>

<span data-ttu-id="e5246-112">Use um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="e5246-112">Use one of the following values:</span></span>



| <span data-ttu-id="e5246-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e5246-113">Value</span></span>     | <span data-ttu-id="e5246-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5246-114">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="e5246-115">VT \_ falso</span><span class="sxs-lookup"><span data-stu-id="e5246-115">VT\_FALSE</span></span> | <span data-ttu-id="e5246-116">Progressivo</span><span class="sxs-lookup"><span data-stu-id="e5246-116">Progressive</span></span> |
| <span data-ttu-id="e5246-117">VT \_ verdadeiro</span><span class="sxs-lookup"><span data-stu-id="e5246-117">VT\_TRUE</span></span>  | <span data-ttu-id="e5246-118">Interlaced</span><span class="sxs-lookup"><span data-stu-id="e5246-118">Interlaced</span></span>  |



 

<span data-ttu-id="e5246-119">Se essa propriedade não for definida, o DSP usará o tipo de mídia de entrada para determinar se o vídeo está entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="e5246-119">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="e5246-120">Você pode definir essa propriedade para substituir a configuração do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e5246-120">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5246-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5246-121">Requirements</span></span>



| <span data-ttu-id="e5246-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5246-122">Requirement</span></span> | <span data-ttu-id="e5246-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e5246-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5246-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5246-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e5246-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e5246-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e5246-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5246-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e5246-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e5246-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e5246-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5246-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5246-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5246-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5246-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5246-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5246-131">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e5246-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
