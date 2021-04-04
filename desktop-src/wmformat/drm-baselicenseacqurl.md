---
title: DRM_BaseLicenseAcqURL
description: O \_ atributo DRM BaseLicenseAcqURL contém uma URL base parcial para a qual um aplicativo de Player deve navegar para obter uma licença para o conteúdo.
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- DRM_BaseLicenseAcqURL o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 128a65eb51d9051243dd439e208207aaf98d5caf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084346"
---
# <a name="drm_baselicenseacqurl"></a><span data-ttu-id="3fcfe-104">\_BASELICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="3fcfe-104">DRM\_BaseLicenseAcqURL</span></span>

<span data-ttu-id="3fcfe-105">O atributo **DRM \_ BaseLicenseAcqURL** contém uma URL base parcial para a qual um aplicativo de Player deve navegar para obter uma licença para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3fcfe-105">The **DRM\_BaseLicenseAcqURL** attribute contains a partial, base URL to which a player application must navigate to obtain a license for the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="3fcfe-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="3fcfe-106">Global Constant</span></span>

<span data-ttu-id="3fcfe-107">g \_ wszWMDRM \_ BaseLicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="3fcfe-107">g\_wszWMDRM\_BaseLicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="3fcfe-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="3fcfe-108">Data Type</span></span>

<span data-ttu-id="3fcfe-109">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="3fcfe-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="3fcfe-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fcfe-110">Remarks</span></span>

<span data-ttu-id="3fcfe-111">Essa é uma propriedade opcional de leitura/gravação que é definida e recuperada usando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="3fcfe-111">This is an optional read-write property that is set and retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="3fcfe-112">Ele é fornecido para habilitar os sistemas de distribuição de licenças para usarem caminhos relativos nas propriedades da URL de aquisição de licença.</span><span class="sxs-lookup"><span data-stu-id="3fcfe-112">It is provided to enable license distribution systems to use relative paths in the license acquisition URL properties.</span></span>

<span data-ttu-id="3fcfe-113">Depois de definir essa propriedade, todas as URLs de aquisição de licença parcial nos cabeçalhos de conteúdo terão a URL base adicionada à frente da URL parcial para formar uma URL completa para o aplicativo de Player navegar.</span><span class="sxs-lookup"><span data-stu-id="3fcfe-113">After setting this property, all partial license acquisition URLs in content headers will have the base URL added to the front of the partial URL to form a full URL for the player application to navigate to.</span></span> <span data-ttu-id="3fcfe-114">Chamar **IWMDRMReader:: GetDRMProperty** para **DRM \_ BaseLicenseAcqURL** só funcionará na mesma sessão que foi definido.</span><span class="sxs-lookup"><span data-stu-id="3fcfe-114">Calling **IWMDRMReader::GetDRMProperty** for **DRM\_BaseLicenseAcqURL** will only work only in the same session as it was set.</span></span> <span data-ttu-id="3fcfe-115">A propriedade não é armazenada no cabeçalho de conteúdo; Ele é dinâmico e apenas a URL relativa é armazenada no conteúdo.</span><span class="sxs-lookup"><span data-stu-id="3fcfe-115">The property is not stored in the content header; it is dynamic, and only the relative URL is stored in the content.</span></span>

## <a name="see-also"></a><span data-ttu-id="3fcfe-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fcfe-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fcfe-117">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="3fcfe-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




