---
description: Contém o GUID de categoria para uma Media Foundation transformação (MFT).
ms.assetid: 3c0948fc-42ea-4e43-a312-c98038020214
title: Propriedade MFPKEY_CATEGORY (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbb83ab2c824ff9a4510e520b13c49ae5b3a52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828618"
---
# <a name="mfpkey_category-property"></a><span data-ttu-id="f7cc3-103">\_Propriedade de categoria MFPKEY</span><span class="sxs-lookup"><span data-stu-id="f7cc3-103">MFPKEY\_CATEGORY property</span></span>

<span data-ttu-id="f7cc3-104">Contém o GUID de categoria para uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="f7cc3-104">Contains the category GUID for a Media Foundation transform (MFT).</span></span>



<span data-ttu-id="f7cc3-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f7cc3-105">Data type</span></span>

<span data-ttu-id="f7cc3-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="f7cc3-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f7cc3-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="f7cc3-107">PROPVARIANT member</span></span>

<span data-ttu-id="f7cc3-108">**GUID** (**CLSID** \* )</span><span class="sxs-lookup"><span data-stu-id="f7cc3-108">**GUID** (**CLSID**\*)</span></span>

<span data-ttu-id="f7cc3-109">CLSID do VT \_</span><span class="sxs-lookup"><span data-stu-id="f7cc3-109">VT\_CLSID</span></span>

<span data-ttu-id="f7cc3-110">**puuid**</span><span class="sxs-lookup"><span data-stu-id="f7cc3-110">**puuid**</span></span>



## <a name="remarks"></a><span data-ttu-id="f7cc3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7cc3-111">Remarks</span></span>

<span data-ttu-id="f7cc3-112">O valor dessa propriedade é um GUID que identifica a categoria de MFT.</span><span class="sxs-lookup"><span data-stu-id="f7cc3-112">The value of this property is a GUID that identifies the MFT category.</span></span> <span data-ttu-id="f7cc3-113">Para obter uma lista de categorias, consulte a [**\_ categoria MFT**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="f7cc3-113">For a list of categories, see [**MFT\_CATEGORY**](mft-category.md).</span></span>

<span data-ttu-id="f7cc3-114">Essa propriedade é opcional e é apenas informativa.</span><span class="sxs-lookup"><span data-stu-id="f7cc3-114">This property is optional and is informational only.</span></span> <span data-ttu-id="f7cc3-115">Uma MFT pode usar essa propriedade para relatar a categoria sob a qual ela está registrada.</span><span class="sxs-lookup"><span data-stu-id="f7cc3-115">An MFT can use this property to report the category under which it is registered.</span></span> <span data-ttu-id="f7cc3-116">Para obter essa propriedade, consulte o MFT para a interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="f7cc3-116">To get this property, query the MFT for the **IPropertyStore** interface.</span></span>

<span data-ttu-id="f7cc3-117">Para enumerar uma categoria de MFT, chame a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .</span><span class="sxs-lookup"><span data-stu-id="f7cc3-117">To enumerate an MFT category, call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function.</span></span> <span data-ttu-id="f7cc3-118">Não há nenhum vínculo direto entre a função **MFTEnum** e essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f7cc3-118">There is no direct link between the **MFTEnum** function and this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7cc3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7cc3-119">Requirements</span></span>



| <span data-ttu-id="f7cc3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7cc3-120">Requirement</span></span> | <span data-ttu-id="f7cc3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f7cc3-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7cc3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7cc3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f7cc3-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7cc3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f7cc3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7cc3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f7cc3-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f7cc3-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f7cc3-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f7cc3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7cc3-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7cc3-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7cc3-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7cc3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7cc3-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f7cc3-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f7cc3-130">Transformações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f7cc3-130">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




