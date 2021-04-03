---
title: DRM_ActionAllowed_CopyToNonSDMIDevice
description: O \_ atributo DRM ActionAllowed \_ CopyToNonSDMIDevice indica se o conteúdo pode ser copiado para um dispositivo não SDMI.
ms.assetid: 517ceeb5-4979-4667-ba54-8b9b1c6069f2
keywords:
- DRM_ActionAllowed_CopyToNonSDMIDevice o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8043c6384fbe0ce57ba56fc9799810d7b6a126b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007140"
---
# <a name="drm_actionallowed_copytononsdmidevice"></a><span data-ttu-id="7b09f-104">\_CopyToNonSDMIDevice ACTIONALLOWED \_ DRM</span><span class="sxs-lookup"><span data-stu-id="7b09f-104">DRM\_ActionAllowed\_CopyToNonSDMIDevice</span></span>

<span data-ttu-id="7b09f-105">O atributo **DRM \_ ActionAllowed \_ CopyToNonSDMIDevice** indica se o conteúdo pode ser copiado para um dispositivo não SDMI</span><span class="sxs-lookup"><span data-stu-id="7b09f-105">The **DRM\_ActionAllowed\_CopyToNonSDMIDevice** attribute indicates whether the content is allowed to be copied to a non-SDMI device</span></span>

## <a name="global-constant"></a><span data-ttu-id="7b09f-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="7b09f-106">Global Constant</span></span>

<span data-ttu-id="7b09f-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="7b09f-107">g\_wszWMDRM\_ActionAllowed\_CopyToNonSDMIDevice</span></span>

## <a name="data-type"></a><span data-ttu-id="7b09f-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="7b09f-108">Data Type</span></span>

<span data-ttu-id="7b09f-109">**WMT \_ tipo \_ bool**</span><span class="sxs-lookup"><span data-stu-id="7b09f-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="7b09f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b09f-110">Remarks</span></span>

<span data-ttu-id="7b09f-111">As licenças do Windows Media DRM 10 usam a ação de cópia para restringir a cópia em dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7b09f-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to devices.</span></span> <span data-ttu-id="7b09f-112">Você deve verificar a propriedade de [**\_ \_ cópia do DRM ActionAllowed**](drm-actionallowed-copy.md) para determinar se a cópia é permitida.</span><span class="sxs-lookup"><span data-stu-id="7b09f-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="7b09f-113">Esta é uma propriedade somente leitura que é recuperada usando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="7b09f-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="7b09f-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b09f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b09f-115">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="7b09f-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




