---
title: Criando licenças localmente
description: Criando licenças localmente
ms.assetid: 151dd231-26a9-4203-84e1-446a07c1e07a
keywords:
- SDK do Windows Media Format, criando licenças localmente
- SDK do Windows Media Format, licenças
- DRM (gerenciamento de direitos digitais), criando licenças localmente
- DRM (gerenciamento de direitos digitais), criando licenças localmente
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- APIs estendidas do cliente DRM, criando licenças localmente
- APIs estendidas do cliente, criando licenças localmente
- licenças, criando licenças localmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fc4305c77be2132611df925ae08458fe2bb4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006137"
---
# <a name="creating-licenses-locally"></a><span data-ttu-id="0be88-112">Criando licenças localmente</span><span class="sxs-lookup"><span data-stu-id="0be88-112">Creating Licenses Locally</span></span>

<span data-ttu-id="0be88-113">Em determinadas circunstâncias, como durante a [importação de DRM](drm-import.md), você pode criar suas próprias licenças.</span><span class="sxs-lookup"><span data-stu-id="0be88-113">In certain circumstances, such as during [DRM Import](drm-import.md), you can create your own licenses.</span></span> <span data-ttu-id="0be88-114">As licenças do Windows Media DRM podem ser escritas de algumas maneiras diferentes, mas para fazer sua própria licença, você deve usar o esquema binário XMR (direitos de mídia extensível).</span><span class="sxs-lookup"><span data-stu-id="0be88-114">Windows Media DRM licenses can be written a few different ways, but to make your own license, you must use the Extensible Media Rights (XMR) binary schema.</span></span> <span data-ttu-id="0be88-115">Para obter mais informações, consulte [criando uma licença do XMR](building-an-xmr-license.md).</span><span class="sxs-lookup"><span data-stu-id="0be88-115">For more information, see [Building an XMR License](building-an-xmr-license.md).</span></span>

<span data-ttu-id="0be88-116">Ao criar uma licença, você pode adicioná-la ao repositório de licenças local chamando o método [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="0be88-116">When you create a license, you can add it to the local license store by calling the [**IWMDRMLicenseManagement::StoreLicense**](iwmdrmlicensemanagement-storelicense.md) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0be88-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0be88-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0be88-118">**Adquirindo licenças**</span><span class="sxs-lookup"><span data-stu-id="0be88-118">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="0be88-119">**Criando uma licença do XMR**</span><span class="sxs-lookup"><span data-stu-id="0be88-119">**Building an XMR License**</span></span>](building-an-xmr-license.md)
</dt> </dl>

 

 




