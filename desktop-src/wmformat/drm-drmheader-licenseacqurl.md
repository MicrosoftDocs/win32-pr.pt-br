---
title: DRM_DRMHeader_LicenseAcqURL
description: O \_ atributo DRM DRMHeader \_ LicenseAcqURL contém a URL de aquisição de licença para uma licença do DRM versão 7.
ms.assetid: 00c788b4-b291-4df5-9926-0badc7357faf
keywords:
- DRM_DRMHeader_LicenseAcqURL o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c394df01703befbb17c61b340b8ea4239740ac3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007108"
---
# <a name="drm_drmheader_licenseacqurl"></a><span data-ttu-id="d6963-104">\_LicenseAcqURL DRMHEADER \_ DRM</span><span class="sxs-lookup"><span data-stu-id="d6963-104">DRM\_DRMHeader\_LicenseAcqURL</span></span>

<span data-ttu-id="d6963-105">O atributo **DRM \_ DRMHeader \_ LICENSEACQURL** contém a URL de aquisição de licença para uma licença do DRM versão 7.</span><span class="sxs-lookup"><span data-stu-id="d6963-105">The **DRM\_DRMHeader\_LicenseAcqURL** attribute contains the license acquisition URL for a DRM version 7 license.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d6963-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="d6963-106">Global Constant</span></span>

<span data-ttu-id="d6963-107">g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="d6963-107">g\_wszWMDRM\_DRMHeader\_LicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="d6963-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="d6963-108">Data Type</span></span>

<span data-ttu-id="d6963-109">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d6963-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="d6963-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6963-110">Remarks</span></span>

<span data-ttu-id="d6963-111">Esse atributo está presente somente com conteúdo do DRM versão 7.</span><span class="sxs-lookup"><span data-stu-id="d6963-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="d6963-112">Ele pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="d6963-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="d6963-113">Para definir a URL de aquisição de licença no arquivo usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , você deve usar a propriedade [**\_ LicenseAcqURL do DRM**](drm-licenseacqurl.md) .</span><span class="sxs-lookup"><span data-stu-id="d6963-113">To set the license acquisition URL on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_LicenseAcqURL**](drm-licenseacqurl.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6963-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6963-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6963-115">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="d6963-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




