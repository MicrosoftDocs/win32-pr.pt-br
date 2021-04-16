---
title: DRM_DRMHeader_IndividualizedVersion
description: O \_ atributo DRM DRMHeaderIndividualizedVersion contém a versão individualizada mínima necessária para reproduzir o arquivo.
ms.assetid: 2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c
keywords:
- DRM_DRMHeader_IndividualizedVersion o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167065f99a72245c6d7cc677ce24fa1ff96dec84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105772700"
---
# <a name="drm_drmheader_individualizedversion"></a><span data-ttu-id="70997-104">\_IndividualizedVersion DRMHEADER \_ DRM</span><span class="sxs-lookup"><span data-stu-id="70997-104">DRM\_DRMHeader\_IndividualizedVersion</span></span>

<span data-ttu-id="70997-105">O atributo **DRM \_ DRMHeaderIndividualizedVersion** contém a versão individualizada mínima necessária para reproduzir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="70997-105">The **DRM\_DRMHeaderIndividualizedVersion** attribute contains the minimum individualized version required to play back the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="70997-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="70997-106">Global Constant</span></span>

<span data-ttu-id="70997-107">g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="70997-107">g\_wszWMDRM\_DRMHeader\_IndividualizedVersion</span></span>

## <a name="data-type"></a><span data-ttu-id="70997-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="70997-108">Data Type</span></span>

<span data-ttu-id="70997-109">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="70997-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="70997-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="70997-110">Remarks</span></span>

<span data-ttu-id="70997-111">Esse atributo está presente somente com conteúdo do DRM versão 7.</span><span class="sxs-lookup"><span data-stu-id="70997-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="70997-112">Ele pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="70997-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="70997-113">Para definir a versão individual (também chamada de versão de segurança) no arquivo usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , você deve usar a [**propriedade \_ IndividualizedVersion do DRM**](drm-individualizedversion.md) .</span><span class="sxs-lookup"><span data-stu-id="70997-113">To set the individualized version (also called the security version) on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_IndividualizedVersion**](drm-individualizedversion.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="70997-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="70997-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70997-115">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="70997-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




