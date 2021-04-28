---
description: Propriedade MFPKEY_RESIZE_INTERLACE-especifica se o fluxo de entrada está entrelaçado.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: Propriedade MFPKEY_RESIZE_INTERLACE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d0efe93901a08322a05dbed2515f76b04a214b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092874"
---
# <a name="mfpkey_resize_interlace-property"></a><span data-ttu-id="72b75-103">MFPKEY \_ redimensionar \_ Propriedade entrelaçar</span><span class="sxs-lookup"><span data-stu-id="72b75-103">MFPKEY\_RESIZE\_INTERLACE Property</span></span>

<span data-ttu-id="72b75-104">Especifica se o fluxo de entrada está entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="72b75-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="72b75-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="72b75-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="72b75-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="72b75-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="72b75-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="72b75-107">Data Type</span></span>

<span data-ttu-id="72b75-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="72b75-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="72b75-109">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="72b75-109">Applies To</span></span>

-   [<span data-ttu-id="72b75-110">DSP de redimensionador de vídeo</span><span class="sxs-lookup"><span data-stu-id="72b75-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="72b75-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="72b75-111">Remarks</span></span>

<span data-ttu-id="72b75-112">Use um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="72b75-112">Use one of the following values:</span></span>



| <span data-ttu-id="72b75-113">Valor</span><span class="sxs-lookup"><span data-stu-id="72b75-113">Value</span></span>     | <span data-ttu-id="72b75-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="72b75-114">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="72b75-115">VT \_ falso</span><span class="sxs-lookup"><span data-stu-id="72b75-115">VT\_FALSE</span></span> | <span data-ttu-id="72b75-116">Progressivo</span><span class="sxs-lookup"><span data-stu-id="72b75-116">Progressive</span></span> |
| <span data-ttu-id="72b75-117">VT \_ verdadeiro</span><span class="sxs-lookup"><span data-stu-id="72b75-117">VT\_TRUE</span></span>  | <span data-ttu-id="72b75-118">Interlaced</span><span class="sxs-lookup"><span data-stu-id="72b75-118">Interlaced</span></span>  |



 

<span data-ttu-id="72b75-119">Se essa propriedade não for definida, o DSP usará o tipo de mídia de entrada para determinar se o vídeo está entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="72b75-119">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="72b75-120">Você pode definir essa propriedade para substituir a configuração do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="72b75-120">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="72b75-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72b75-121">Requirements</span></span>



| <span data-ttu-id="72b75-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="72b75-122">Requirement</span></span> | <span data-ttu-id="72b75-123">Valor</span><span class="sxs-lookup"><span data-stu-id="72b75-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72b75-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72b75-124">Minimum supported client</span></span><br/> | <span data-ttu-id="72b75-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="72b75-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="72b75-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72b75-126">Minimum supported server</span></span><br/> | <span data-ttu-id="72b75-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="72b75-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="72b75-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72b75-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="72b75-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72b75-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72b75-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="72b75-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b75-131">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="72b75-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
