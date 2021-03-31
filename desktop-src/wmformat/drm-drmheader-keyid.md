---
title: DRM_DRMHeader_KeyID
description: O \_ atributo keyid DRMHeader do DRM \_ contém a ID da chave para o arquivo.
ms.assetid: cf9fe829-8473-4dd5-9a99-48b709fec0d8
keywords:
- DRM_DRMHeader_KeyID o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebbf2f548725309717993bf29e48de2bf78ed17
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293776"
---
# <a name="drm_drmheader_keyid"></a><span data-ttu-id="8cc07-104">\_Keyid DRMHEADER \_ DRM</span><span class="sxs-lookup"><span data-stu-id="8cc07-104">DRM\_DRMHeader\_KeyID</span></span>

<span data-ttu-id="8cc07-105">O **atributo \_ \_ keyid DRMHeader do DRM** contém a ID da chave para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="8cc07-105">The **DRM\_DRMHeader\_KeyID** attribute contains the key ID for the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="8cc07-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="8cc07-106">Global Constant</span></span>

<span data-ttu-id="8cc07-107">\_keyid g wszWMDRM \_ DRMHeader \_</span><span class="sxs-lookup"><span data-stu-id="8cc07-107">g\_wszWMDRM\_DRMHeader\_KeyID</span></span>

## <a name="data-type"></a><span data-ttu-id="8cc07-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="8cc07-108">Data Type</span></span>

<span data-ttu-id="8cc07-109">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="8cc07-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="8cc07-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cc07-110">Remarks</span></span>

<span data-ttu-id="8cc07-111">Esse atributo está presente somente com conteúdo do DRM versão 7.</span><span class="sxs-lookup"><span data-stu-id="8cc07-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="8cc07-112">Ele pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="8cc07-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="8cc07-113">Para definir a ID da chave no arquivo usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , você deve usar a propriedade [**\_ keyid do DRM**](drm-keyid.md) .</span><span class="sxs-lookup"><span data-stu-id="8cc07-113">To set the key ID on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_KeyID**](drm-keyid.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="8cc07-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cc07-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc07-115">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="8cc07-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




