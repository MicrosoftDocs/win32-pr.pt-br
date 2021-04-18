---
title: DRM_IsDRMCached
description: A \_ Propriedade DRM IsDRMCached indica se as informações de licença do DRM versão 1 foram armazenadas no computador local.
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- DRM_IsDRMCached o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 185a8b2c94ca5ec517eb1a781262e3f988001a01
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105778450"
---
# <a name="drm_isdrmcached"></a><span data-ttu-id="50da7-104">\_ISDRMCACHED DRM</span><span class="sxs-lookup"><span data-stu-id="50da7-104">DRM\_IsDRMCached</span></span>

<span data-ttu-id="50da7-105">A propriedade **DRM \_ IsDRMCached** indica se as informações de licença do DRM versão 1 foram armazenadas no computador local.</span><span class="sxs-lookup"><span data-stu-id="50da7-105">The **DRM\_IsDRMCached** property indicates whether DRM version 1 license information has been stored on the local machine.</span></span>

## <a name="global-constant"></a><span data-ttu-id="50da7-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="50da7-106">Global Constant</span></span>

<span data-ttu-id="50da7-107">g \_ wszWMDRM \_ IsDRMCached</span><span class="sxs-lookup"><span data-stu-id="50da7-107">g\_wszWMDRM\_IsDRMCached</span></span>

## <a name="data-type"></a><span data-ttu-id="50da7-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="50da7-108">Data Type</span></span>

<span data-ttu-id="50da7-109">**WMT \_ tipo \_ bool**</span><span class="sxs-lookup"><span data-stu-id="50da7-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="50da7-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="50da7-110">Remarks</span></span>

<span data-ttu-id="50da7-111">Esta é uma propriedade somente leitura que é recuperada usando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="50da7-111">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="50da7-112">É **verdade** quando a URL de aquisição de licença corresponde a uma das duas URLs conhecidas usadas para aquisição de licença local no DRM versão 1.</span><span class="sxs-lookup"><span data-stu-id="50da7-112">It is **TRUE** when the license acquisition URL matches one of two know URLs used for local license acquisition in DRM version 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="50da7-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="50da7-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50da7-114">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="50da7-114">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




