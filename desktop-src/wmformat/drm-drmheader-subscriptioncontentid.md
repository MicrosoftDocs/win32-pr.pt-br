---
title: DRM_DRMHeader_SubscriptionContentID
description: O \_ atributo DRM DRMHeader \_ SubscriptionContentID contém a ID de conteúdo da assinatura.
ms.assetid: e582d841-4865-40d3-889e-847d3aac0a7c
keywords:
- DRM_DRMHeader_SubscriptionContentID o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151665777aa6b68078361eb6e063e374a52f30bf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916988"
---
# <a name="drm_drmheader_subscriptioncontentid"></a><span data-ttu-id="06145-104">\_SubscriptionContentID DRMHEADER \_ DRM</span><span class="sxs-lookup"><span data-stu-id="06145-104">DRM\_DRMHeader\_SubscriptionContentID</span></span>

<span data-ttu-id="06145-105">O atributo **DRM \_ DRMHeader \_ SUBSCRIPTIONCONTENTID** contém a ID de conteúdo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="06145-105">The **DRM\_DRMHeader\_SubscriptionContentID** attribute contains the subscription content ID.</span></span>

## <a name="global-constant"></a><span data-ttu-id="06145-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="06145-106">Global Constant</span></span>

<span data-ttu-id="06145-107">g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID</span><span class="sxs-lookup"><span data-stu-id="06145-107">g\_wszWMDRM\_DRMHeader\_SubscriptionContentID</span></span>

## <a name="data-type"></a><span data-ttu-id="06145-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="06145-108">Data Type</span></span>

<span data-ttu-id="06145-109">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="06145-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="06145-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="06145-110">Remarks</span></span>

<span data-ttu-id="06145-111">Esse atributo está presente somente com conteúdo do DRM versão 7.</span><span class="sxs-lookup"><span data-stu-id="06145-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="06145-112">A ID do conteúdo da assinatura é opcional e é determinada exclusivamente pelo criador do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="06145-112">The subscription content ID is optional and is determined solely by the content creator.</span></span> <span data-ttu-id="06145-113">O objeto gravador não faz nada com esse atributo.</span><span class="sxs-lookup"><span data-stu-id="06145-113">The writer object does nothing with this attribute.</span></span> <span data-ttu-id="06145-114">Ele pode ser definido usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="06145-114">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="06145-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="06145-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06145-116">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="06145-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




