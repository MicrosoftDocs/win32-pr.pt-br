---
title: DRM_Level
description: '\_O nível de DRM é um atributo de licença que o Windows Media Format SDK define ao criar uma licença local para arquivos protegidos com o DRM versão 1.'
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3177197b9c149c2fca2c7678a8fe03c6b412e2d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293797"
---
# <a name="drm_level"></a><span data-ttu-id="f37d1-104">Nível de DRM \_</span><span class="sxs-lookup"><span data-stu-id="f37d1-104">DRM\_Level</span></span>

<span data-ttu-id="f37d1-105">**DRM \_ Nível** é um atributo de licença que o SDK do Windows Media Format define ao criar uma licença local para arquivos protegidos com o DRM versão 1.</span><span class="sxs-lookup"><span data-stu-id="f37d1-105">**DRM\_Level** is a license attribute that the Windows Media Format SDK sets when it creates a local license for files protected with DRM version 1.</span></span> <span data-ttu-id="f37d1-106">Ele contém o nível de segurança que o aplicativo de chamada deve ter para acessar o conteúdo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="f37d1-106">It contains the security level that the calling application must have to access the content in the file.</span></span> <span data-ttu-id="f37d1-107">O valor padrão é 150.</span><span class="sxs-lookup"><span data-stu-id="f37d1-107">The default value is 150.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f37d1-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="f37d1-108">Global Constant</span></span>

<span data-ttu-id="f37d1-109">\_nível g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="f37d1-109">g\_wszWMDRM\_Level</span></span>

## <a name="data-type"></a><span data-ttu-id="f37d1-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="f37d1-110">Data Type</span></span>

<span data-ttu-id="f37d1-111">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f37d1-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="f37d1-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f37d1-112">Remarks</span></span>

<span data-ttu-id="f37d1-113">O nível de segurança do DRM de um aplicativo é determinado pela biblioteca wmstubdrm específica a que ele se vincula no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="f37d1-113">An application's DRM security level is determined by the particular wmstubdrm library that it links to at compile time.</span></span> <span data-ttu-id="f37d1-114">Para obter mais informações sobre esses níveis de segurança, consulte [obtendo a biblioteca de DRM necessária](obtaining-the-required-drm-library.md).</span><span class="sxs-lookup"><span data-stu-id="f37d1-114">For more information on these security levels, see [Obtaining the Required DRM Library](obtaining-the-required-drm-library.md).</span></span> <span data-ttu-id="f37d1-115">Use [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) para definir essa propriedade ao proteger arquivos ASF com o DRM versão 1.</span><span class="sxs-lookup"><span data-stu-id="f37d1-115">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property when protecting ASF files with DRM version 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="f37d1-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="f37d1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f37d1-117">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="f37d1-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




