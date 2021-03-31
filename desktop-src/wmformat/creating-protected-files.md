---
title: Criando arquivos protegidos
description: Criando arquivos protegidos
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- SDK do Windows Media Format, criando arquivos protegidos
- SDK do Windows Media Format, arquivos protegidos
- ASF (Advanced Systems Format), criando arquivos protegidos
- ASF (formato de sistemas avançados), criando arquivos protegidos
- ASF (Advanced Systems Format), arquivos protegidos
- ASF (formato de sistemas avançados), arquivos protegidos
- ASF (Advanced Systems Format), WMStubDRM. lib
- ASF (formato de sistemas avançados), WMStubDRM. lib
- WMStubDRM. lib, criando arquivos protegidos
- WMStubDRM. lib, arquivos protegidos
- DRM (gerenciamento de direitos digitais), WMStubDRM. lib
- DRM (gerenciamento de direitos digitais), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a14d96da924bdb2a307bc804514a1ec3de083
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293768"
---
# <a name="creating-protected-files"></a><span data-ttu-id="37c0e-115">Criando arquivos protegidos</span><span class="sxs-lookup"><span data-stu-id="37c0e-115">Creating Protected Files</span></span>

<span data-ttu-id="37c0e-116">Para criar arquivos de mídia digital protegidos usando o DRM versão 1 ou o DRM versões 7 e posteriores, vincule ao arquivo WMStubDRM. lib que você obteve da Microsoft e crie o objeto do gravador.</span><span class="sxs-lookup"><span data-stu-id="37c0e-116">To create protected digital media files using either DRM version 1 or DRM versions 7 and later, link to the WMStubDRM.lib file that you obtained from Microsoft, and create the writer object.</span></span> <span data-ttu-id="37c0e-117">Para a proteção da versão 1, use a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) para definir os atributos DRM que você deseja aplicar.</span><span class="sxs-lookup"><span data-stu-id="37c0e-117">For version 1 protection, use the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface to set the DRM attributes you want to apply.</span></span> <span data-ttu-id="37c0e-118">Para as versões 7 e posteriores, use os métodos de interface [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) .</span><span class="sxs-lookup"><span data-stu-id="37c0e-118">For versions 7 and later, use the [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) interface methods.</span></span>

<span data-ttu-id="37c0e-119">Os tópicos a seguir descrevem em detalhes como proteger arquivos.</span><span class="sxs-lookup"><span data-stu-id="37c0e-119">The following topics describe in detail how to protect files.</span></span>

-   [<span data-ttu-id="37c0e-120">Protegendo arquivos com DRM versão 1</span><span class="sxs-lookup"><span data-stu-id="37c0e-120">Protecting Files with DRM Version 1</span></span>](protecting-files-with-drm-version-1.md)
-   [<span data-ttu-id="37c0e-121">Protegendo arquivos com DRM versão 7 ou posterior</span><span class="sxs-lookup"><span data-stu-id="37c0e-121">Protecting Files with DRM Version 7 or Later</span></span>](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> <span data-ttu-id="37c0e-122">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="37c0e-122">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="37c0e-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="37c0e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37c0e-124">**Lista de atributos DRM**</span><span class="sxs-lookup"><span data-stu-id="37c0e-124">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="37c0e-125">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="37c0e-125">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="37c0e-126">**Versões de DRM**</span><span class="sxs-lookup"><span data-stu-id="37c0e-126">**DRM Versions**</span></span>](drm-versions.md)
</dt> <dt>

[<span data-ttu-id="37c0e-127">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="37c0e-127">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="37c0e-128">**Obtendo a biblioteca de DRM necessária**</span><span class="sxs-lookup"><span data-stu-id="37c0e-128">**Obtaining the Required DRM Library**</span></span>](obtaining-the-required-drm-library.md)
</dt> <dt>

[<span data-ttu-id="37c0e-129">**Lendo arquivos protegidos**</span><span class="sxs-lookup"><span data-stu-id="37c0e-129">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




