---
title: DRM_DRMHeader_ContentDistributor
description: O \_ atributo DRM DRMHeader \_ ContentDistributor contém uma cadeia de caracteres identifiying o distribuidor de conteúdo.
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- DRM_DRMHeader_ContentDistributor o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2494f80e612e03f9d25372d38e875c1df814fd7d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105772638"
---
# <a name="drm_drmheader_contentdistributor"></a><span data-ttu-id="adf89-104">\_ContentDistributor DRMHEADER \_ DRM</span><span class="sxs-lookup"><span data-stu-id="adf89-104">DRM\_DRMHeader\_ContentDistributor</span></span>

<span data-ttu-id="adf89-105">O atributo **DRM \_ DRMHeader \_ ContentDistributor** contém uma cadeia de caracteres identifiying o distribuidor de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="adf89-105">The **DRM\_DRMHeader\_ContentDistributor** attribute contains a string identifiying the content distributor.</span></span>

## <a name="global-constant"></a><span data-ttu-id="adf89-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="adf89-106">Global Constant</span></span>

<span data-ttu-id="adf89-107">g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor</span><span class="sxs-lookup"><span data-stu-id="adf89-107">g\_wszWMDRM\_DRMHeader\_ContentDistributor</span></span>

## <a name="data-type"></a><span data-ttu-id="adf89-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="adf89-108">Data Type</span></span>

<span data-ttu-id="adf89-109">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="adf89-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="adf89-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="adf89-110">Remarks</span></span>

<span data-ttu-id="adf89-111">A ID de conteúdo é opcional e é determinada exclusivamente pelo criador de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="adf89-111">The content ID is optional and is determined solely by the content creator.</span></span> <span data-ttu-id="adf89-112">O objeto gravador não faz nada com esse atributo.</span><span class="sxs-lookup"><span data-stu-id="adf89-112">The writer object does nothing with this attribute.</span></span> <span data-ttu-id="adf89-113">Esse atributo está presente somente com conteúdo do DRM versão 7.</span><span class="sxs-lookup"><span data-stu-id="adf89-113">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="adf89-114">Ele pode ser definido usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="adf89-114">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="adf89-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="adf89-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf89-116">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="adf89-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




