---
title: Suporte a DRM no DirectShow
description: Suporte a DRM no DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- SDK do Windows Media Format, suporte a DRM no DirectShow
- SDK do Windows Media Format, DirectShow
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- ASF (Advanced Systems Format), suporte a DRM no DirectShow
- ASF (formato de sistemas avançados), suporte a DRM no DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), DRM (gerenciamento de direitos digitais)
- ASF (formato de sistemas avançados), DRM (gerenciamento de direitos digitais)
- DirectShow, suporte a DRM
- DRM (gerenciamento de direitos digitais), DirectShow
- DRM (gerenciamento de direitos digitais), DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a211a3d3b438bac246c0bd90759f648818ac2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916979"
---
# <a name="drm-support-in-directshow"></a><span data-ttu-id="11ad4-115">Suporte a DRM no DirectShow</span><span class="sxs-lookup"><span data-stu-id="11ad4-115">DRM Support in DirectShow</span></span>

<span data-ttu-id="11ad4-116">A leitura e a gravação de arquivos protegidos por DRM no DirectShow é feita basicamente da mesma maneira que quando você usa o SDK do Windows Media Format diretamente.</span><span class="sxs-lookup"><span data-stu-id="11ad4-116">Reading and writing DRM-protected files in DirectShow is done in basically the same way as when you use the Windows Media Format SDK directly.</span></span> <span data-ttu-id="11ad4-117">Para começar, você precisa da biblioteca estática wmstubdrm, que é obtida separadamente da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="11ad4-117">To begin with, you need the wmstubdrm static library, which is obtained separately from Microsoft.</span></span> <span data-ttu-id="11ad4-118">Além disso, você deve implementar a interface **IKeyProvider** para permitir que seu aplicativo acesse os objetos de tempo de execução do Windows Media Format SDK quando o DRM estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="11ad4-118">In addition, you must implement the **IKeyProvider** interface to enable your application to access the Windows Media Format SDK run-time objects when DRM is enabled.</span></span>

<span data-ttu-id="11ad4-119">Ao aplicar a proteção do DRM versão 1, use a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , que é obtida conforme descrito em [lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="11ad4-119">When applying DRM version 1 protection, use the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which is obtained as described in [Reading ASF Files in DirectShow](reading-asf-files-in-directshow.md).</span></span> <span data-ttu-id="11ad4-120">Ao aplicar a proteção do DRM versão 7, obtenha a interface [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) chamando **QueryService** no filtro de [gravador ASF do WM](wm-asf-writer-filter.md) , conforme mostrado no trecho de código mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="11ad4-120">When applying DRM version 7 protection, obtain the [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) interface by calling **QueryService** on the [WM ASF Writer](wm-asf-writer-filter.md) filter, as shown in the code snippet later in this topic.</span></span>

<span data-ttu-id="11ad4-121">Todas as outras configurações específicas de DRM são exatamente as mesmas, conforme descrito em [habilitando o suporte a DRM](enabling-drm-support.md).</span><span class="sxs-lookup"><span data-stu-id="11ad4-121">All other DRM-specific configuration is exactly the same as described in [Enabling DRM Support](enabling-drm-support.md).</span></span> <span data-ttu-id="11ad4-122">Use o **QueryService** para obter a interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) do filtro de [leitor ASF do WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="11ad4-122">Use **QueryService** to obtain the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface from the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>

<span data-ttu-id="11ad4-123">O DirectX 9,0 contém um exemplo de PlayWndASF, um aplicativo de Player DirectShow habilitado para DRM que demonstra a aquisição de licença do DRM versão 1 e versão 7.</span><span class="sxs-lookup"><span data-stu-id="11ad4-123">DirectX 9.0 contains a sample, PlayWndASF, a DRM-enabled DirectShow player application that demonstrates DRM version 1 and version 7 license acquisition.</span></span> <span data-ttu-id="11ad4-124">Este exemplo também inclui uma implementação da classe **CKeyProvider** , que dá suporte à interface **IKeyProvider** .</span><span class="sxs-lookup"><span data-stu-id="11ad4-124">This sample also includes an implementation of the **CKeyProvider** class, which supports the **IKeyProvider** interface.</span></span>

 

 




