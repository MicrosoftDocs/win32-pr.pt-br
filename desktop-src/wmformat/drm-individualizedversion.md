---
title: DRM_IndividualizedVersion
description: O \_ atributo DRM IndividualizedVersion é armazenado no cabeçalho DRM e contém a versão individual, necessária para acessar o conteúdo.
ms.assetid: ed3e165c-c6b0-4eea-be79-a715abd4dd0a
keywords:
- DRM_IndividualizedVersion o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ecde48ef3d68e30116cdd7fc8a77179f2282c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293800"
---
# <a name="drm_individualizedversion"></a><span data-ttu-id="46b0e-104">\_INDIVIDUALIZEDVERSION DRM</span><span class="sxs-lookup"><span data-stu-id="46b0e-104">DRM\_IndividualizedVersion</span></span>

<span data-ttu-id="46b0e-105">O atributo **DRM \_ IndividualizedVersion** é armazenado no cabeçalho DRM e contém a versão individual, necessária para acessar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="46b0e-105">The **DRM\_IndividualizedVersion** attribute is stored in the DRM header and contains the minimum individualized version required to access the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="46b0e-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="46b0e-106">Global Constant</span></span>

<span data-ttu-id="46b0e-107">g \_ wszWMDRM \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="46b0e-107">g\_wszWMDRM\_IndividualizedVersion</span></span>

## <a name="data-type"></a><span data-ttu-id="46b0e-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="46b0e-108">Data Type</span></span>

<span data-ttu-id="46b0e-109">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="46b0e-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="46b0e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="46b0e-110">Remarks</span></span>

<span data-ttu-id="46b0e-111">Esse atributo está presente somente com conteúdo do DRM versão 7.</span><span class="sxs-lookup"><span data-stu-id="46b0e-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="46b0e-112">Ele pode ser definido usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="46b0e-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="46b0e-113">O mesmo atributo de arquivo pode ser recuperado usando [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md).</span><span class="sxs-lookup"><span data-stu-id="46b0e-113">The same file attribute can be retrieved using [**DRM\_DRMHeader\_IndividualizedVersion**](drm-drmheader-individualizedversion.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="46b0e-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="46b0e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46b0e-115">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="46b0e-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




