---
description: Especifica se a origem de mídia ASF usa busca aproximada.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: Propriedade MFPKEY_ASFMediaSource_ApproxSeek (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253a18ebbdf78e3aa0ef0e79f41c4bf180a04b48
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105797594"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a><span data-ttu-id="fddd5-103">\_Propriedade MFPKEY ASFMediaSource \_ ApproxSeek</span><span class="sxs-lookup"><span data-stu-id="fddd5-103">MFPKEY\_ASFMediaSource\_ApproxSeek property</span></span>

<span data-ttu-id="fddd5-104">Especifica se a origem de mídia ASF usa busca aproximada.</span><span class="sxs-lookup"><span data-stu-id="fddd5-104">Specifies whether the ASF media source uses approximate seeking.</span></span>



<span data-ttu-id="fddd5-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fddd5-105">Data type</span></span>

<span data-ttu-id="fddd5-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="fddd5-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="fddd5-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="fddd5-107">PROPVARIANT member</span></span>

<span data-ttu-id="fddd5-108">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="fddd5-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="fddd5-109">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="fddd5-109">VT\_BOOL</span></span>

<span data-ttu-id="fddd5-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="fddd5-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="fddd5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fddd5-111">Remarks</span></span>

<span data-ttu-id="fddd5-112">Os aplicativos podem usar essa propriedade para configurar a origem da mídia ASF.</span><span class="sxs-lookup"><span data-stu-id="fddd5-112">Applications can use this property to configure the ASF media source.</span></span> <span data-ttu-id="fddd5-113">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="fddd5-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="fddd5-114">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="fddd5-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="fddd5-115">A fonte de mídia do ASF trata da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="fddd5-115">The ASF media source handles seeking as follows:</span></span>

-   <span data-ttu-id="fddd5-116">Se o valor dessa propriedade for **Variant \_ true**, a origem da mídia usará a busca aproximada, que é menos precisa, mas mais rápida do que a procura exata.</span><span class="sxs-lookup"><span data-stu-id="fddd5-116">If the value of this property is **VARIANT\_TRUE**, the media source uses approximate seeking, which is less accurate but faster than exact seeking.</span></span>
-   <span data-ttu-id="fddd5-117">Se o valor for **Variant \_ false** e o arquivo ASF tiver um índice, a origem da mídia usará a busca exata.</span><span class="sxs-lookup"><span data-stu-id="fddd5-117">If the value is **VARIANT\_FALSE** and the ASF file has an index, the media source uses exact seeking.</span></span>
-   <span data-ttu-id="fddd5-118">Se o arquivo ASF não contiver um índice, a origem da mídia usará approxmate procurando, a menos que a propriedade [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) esteja definida como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="fddd5-118">If the ASF file does not contain an index, the media source uses approxmate seeking unless the [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) property is set to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="fddd5-119">Se o arquivo ASF não contiver um índice e a propriedade [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) for **Variant \_ true**, a origem de mídia usará a busca iterativa.</span><span class="sxs-lookup"><span data-stu-id="fddd5-119">If the ASF file does not contain an index and the [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) property is **VARIANT\_TRUE**, the media source uses iterative seeking.</span></span> <span data-ttu-id="fddd5-120">A busca iterativa é mais precisa, mas mais lenta que a busca aproximada (mas geralmente menos precisa do que a procura exata).</span><span class="sxs-lookup"><span data-stu-id="fddd5-120">Iterative seeking is more accurate but slower than approximate seeking (but generally less accurate than exact seeking).</span></span>
    > [!Note]  
    > <span data-ttu-id="fddd5-121">Requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fddd5-121">Requires Windows 7.</span></span>

     

<span data-ttu-id="fddd5-122">O valor padrão dessa propriedade é **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="fddd5-122">The default value of this property is **VARIANT\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fddd5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fddd5-123">Requirements</span></span>



| <span data-ttu-id="fddd5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fddd5-124">Requirement</span></span> | <span data-ttu-id="fddd5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fddd5-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fddd5-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fddd5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fddd5-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fddd5-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fddd5-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fddd5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fddd5-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fddd5-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fddd5-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fddd5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fddd5-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fddd5-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fddd5-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="fddd5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fddd5-133">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fddd5-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




