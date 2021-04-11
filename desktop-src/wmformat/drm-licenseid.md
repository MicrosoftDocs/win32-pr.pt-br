---
title: DRM_LicenseID
description: A \_ Propriedade DRM licenseid contém uma cadeia de caracteres recuperada da licença associada ao arquivo aberto no momento que identifica exclusivamente essa licença.
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293796"
---
# <a name="drm_licenseid"></a><span data-ttu-id="e1503-104">\_Licenseid DRM</span><span class="sxs-lookup"><span data-stu-id="e1503-104">DRM\_LicenseID</span></span>

<span data-ttu-id="e1503-105">A propriedade **DRM \_ licenseid** contém uma cadeia de caracteres recuperada da licença associada ao arquivo aberto no momento que identifica exclusivamente essa licença.</span><span class="sxs-lookup"><span data-stu-id="e1503-105">The **DRM\_LicenseID** property contains a string retrieved from the license associated with the currently open file that uniquely identifies that license.</span></span>

## <a name="global-constant"></a><span data-ttu-id="e1503-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="e1503-106">Global Constant</span></span>

<span data-ttu-id="e1503-107">\_licença de wszWMDRM g \_</span><span class="sxs-lookup"><span data-stu-id="e1503-107">g\_wszWMDRM\_LicenseID</span></span>

## <a name="data-type"></a><span data-ttu-id="e1503-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="e1503-108">Data Type</span></span>

<span data-ttu-id="e1503-109">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="e1503-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="e1503-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1503-110">Remarks</span></span>

<span data-ttu-id="e1503-111">Esse atributo está presente somente com conteúdo do DRM versão 7.</span><span class="sxs-lookup"><span data-stu-id="e1503-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="e1503-112">Ele pode ser definido usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e pode ser recuperado com [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="e1503-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

<span data-ttu-id="e1503-113">A ID da licença é armazenada em uma licença, não em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="e1503-113">The license ID is stored in a license, not in an ASF file.</span></span> <span data-ttu-id="e1503-114">Cada licença individual tem uma ID exclusiva que é atribuída pelo gerador de licença no momento em que a licença é criada.</span><span class="sxs-lookup"><span data-stu-id="e1503-114">Each individual license has a unique ID which is assigned by the license generator at the time the license is created.</span></span> <span data-ttu-id="e1503-115">Por exemplo, se você obtiver duas licenças para o mesmo conteúdo, cada uma terá um atributo Licenseid diferente.</span><span class="sxs-lookup"><span data-stu-id="e1503-115">For example, if you obtain two licenses for the same content, each one will have a different LicenseID attribute.</span></span> <span data-ttu-id="e1503-116">Normalmente, os aplicativos não precisam recuperar esse valor.</span><span class="sxs-lookup"><span data-stu-id="e1503-116">Typically, applications have no need to retrieve this value.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1503-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1503-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1503-118">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="e1503-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




