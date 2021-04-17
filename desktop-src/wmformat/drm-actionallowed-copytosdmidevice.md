---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: O \_ atributo DRM ActionAllowed \_ CopyToSDMIDevice indica se o conteúdo pode ser copiado para um dispositivo SDMI.
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- DRM_ActionAllowed_CopyToSDMIDevice o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f61da53fd060bd4fb06dbbb7586d923ac17fc0f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365516"
---
# <a name="drm_actionallowed_copytosdmidevice"></a><span data-ttu-id="72617-104">\_CopyToSDMIDevice ACTIONALLOWED \_ DRM</span><span class="sxs-lookup"><span data-stu-id="72617-104">DRM\_ActionAllowed\_CopyToSDMIDevice</span></span>

<span data-ttu-id="72617-105">O atributo **DRM \_ ActionAllowed \_ CopyToSDMIDevice** indica se o conteúdo pode ser copiado para um dispositivo SDMI.</span><span class="sxs-lookup"><span data-stu-id="72617-105">The **DRM\_ActionAllowed\_CopyToSDMIDevice** attribute indicates whether the content is allowed to be copied to an SDMI device.</span></span>

## <a name="global-constant"></a><span data-ttu-id="72617-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="72617-106">Global Constant</span></span>

<span data-ttu-id="72617-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="72617-107">g\_wszWMDRM\_ActionAllowed\_CopyToSDMIDevice</span></span>

## <a name="data-type"></a><span data-ttu-id="72617-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="72617-108">Data Type</span></span>

<span data-ttu-id="72617-109">**WMT \_ tipo \_ bool**</span><span class="sxs-lookup"><span data-stu-id="72617-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="72617-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="72617-110">Remarks</span></span>

<span data-ttu-id="72617-111">As licenças do Windows Media DRM 10 usam a ação de cópia para restringir a cópia em dispositivos.</span><span class="sxs-lookup"><span data-stu-id="72617-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to devices.</span></span> <span data-ttu-id="72617-112">Você deve verificar a propriedade de [**\_ \_ cópia do DRM ActionAllowed**](drm-actionallowed-copy.md) para determinar se a cópia é permitida.</span><span class="sxs-lookup"><span data-stu-id="72617-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="72617-113">Esta é uma propriedade somente leitura que é recuperada usando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="72617-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="72617-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="72617-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72617-115">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="72617-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




