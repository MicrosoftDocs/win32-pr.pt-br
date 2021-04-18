---
title: DRM_ActionAllowed_CopyToCD
description: O \_ atributo DRM ActionAllowed \_ CopyToCD indica se o conteúdo pode ser copiado para um CD.
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- DRM_ActionAllowed_CopyToCD o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba214fb2f067ba523222f92211bf7a9412a1634
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105768214"
---
# <a name="drm_actionallowed_copytocd"></a><span data-ttu-id="c62e4-104">\_CopyToCD ACTIONALLOWED \_ DRM</span><span class="sxs-lookup"><span data-stu-id="c62e4-104">DRM\_ActionAllowed\_CopyToCD</span></span>

<span data-ttu-id="c62e4-105">O atributo **DRM \_ ActionAllowed \_ CopyToCD** indica se o conteúdo pode ser copiado para um CD.</span><span class="sxs-lookup"><span data-stu-id="c62e4-105">The **DRM\_ActionAllowed\_CopyToCD** attribute indicates whether the content is allowed to be copied to a CD.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c62e4-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="c62e4-106">Global Constant</span></span>

<span data-ttu-id="c62e4-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="c62e4-107">g\_wszWMDRM\_ActionAllowed\_CopyToCD</span></span>

## <a name="data-type"></a><span data-ttu-id="c62e4-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="c62e4-108">Data Type</span></span>

<span data-ttu-id="c62e4-109">**WMT \_ tipo \_ bool**</span><span class="sxs-lookup"><span data-stu-id="c62e4-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="c62e4-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c62e4-110">Remarks</span></span>

<span data-ttu-id="c62e4-111">As licenças do Windows Media DRM 10 usam a ação de cópia para restringir a cópia em CD.</span><span class="sxs-lookup"><span data-stu-id="c62e4-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to CD.</span></span> <span data-ttu-id="c62e4-112">Você deve verificar a propriedade de [**\_ \_ cópia do DRM ActionAllowed**](drm-actionallowed-copy.md) para determinar se a cópia é permitida.</span><span class="sxs-lookup"><span data-stu-id="c62e4-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="c62e4-113">Esta é uma propriedade somente leitura que é recuperada usando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="c62e4-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="c62e4-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="c62e4-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c62e4-115">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="c62e4-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




