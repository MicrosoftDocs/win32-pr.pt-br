---
description: Especifica a categoria de uma Media Foundation de transformação (MFT).
ms.assetid: cebd64ea-b20f-4ccc-805f-0deab3096bc3
title: Atributo MF_TRANSFORM_CATEGORY_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3c64fd5e19bba10646957e7c247294b6d82a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164754"
---
# <a name="mf_transform_category_attribute-attribute"></a><span data-ttu-id="5d43a-103">\_Atributo de \_ atributo de categoria de transformação MF \_</span><span class="sxs-lookup"><span data-stu-id="5d43a-103">MF\_TRANSFORM\_CATEGORY\_Attribute attribute</span></span>

<span data-ttu-id="5d43a-104">Especifica a categoria de uma Media Foundation de transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="5d43a-104">Specifies the category for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="5d43a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5d43a-105">Data type</span></span>

<span data-ttu-id="5d43a-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="5d43a-106">**GUID**</span></span>

<span data-ttu-id="5d43a-107">Para obter uma lista de valores possíveis, consulte a [**\_ categoria MFT**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="5d43a-107">For a list of possible values, see [**MFT\_CATEGORY**](mft-category.md).</span></span>

## <a name="getset"></a><span data-ttu-id="5d43a-108">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="5d43a-108">Get/set</span></span>

<span data-ttu-id="5d43a-109">Para obter esse atributo, chame [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="5d43a-109">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="5d43a-110">Para definir esse atributo, chame [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="5d43a-110">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="5d43a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d43a-111">Remarks</span></span>

<span data-ttu-id="5d43a-112">Esse atributo é definido nos ponteiros do [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="5d43a-112">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d43a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d43a-113">Requirements</span></span>



| <span data-ttu-id="5d43a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d43a-114">Requirement</span></span> | <span data-ttu-id="5d43a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5d43a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d43a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d43a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5d43a-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5d43a-117">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="5d43a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d43a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5d43a-119">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="5d43a-119">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5d43a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d43a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d43a-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d43a-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d43a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d43a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d43a-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5d43a-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5d43a-124">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="5d43a-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




