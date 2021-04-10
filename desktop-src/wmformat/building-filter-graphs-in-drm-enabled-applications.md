---
title: Criando gráficos de filtro em aplicativos DRM-Enabled
description: Criando gráficos de filtro em aplicativos DRM-Enabled
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- SDK do Windows Media Format, criando gráficos de filtro
- SDK do Windows Media Format, DirectShow
- SDK do Windows Media Format, aplicativos habilitados para DRM
- ASF (Advanced Systems Format), criando gráficos de filtro
- ASF (formato de sistemas avançados), criando gráficos de filtro
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), aplicativos habilitados para DRM
- ASF (formato de sistemas avançados), aplicativos habilitados para DRM
- DirectShow, criando gráficos de filtro
- Aplicativos habilitados para DRM e DirectShow
- DRM (gerenciamento de direitos digitais), DirectShow
- DRM (gerenciamento de direitos digitais), DirectShow
- DRM (gerenciamento de direitos digitais), criando gráficos de filtro
- DRM (gerenciamento de direitos digitais), criando gráficos de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944037a00c208e1427d3d19aa6c9dc0a352ec5fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293791"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a><span data-ttu-id="877a3-118">Criando gráficos de filtro em aplicativos DRM-Enabled</span><span class="sxs-lookup"><span data-stu-id="877a3-118">Building Filter Graphs in DRM-Enabled Applications</span></span>

<span data-ttu-id="877a3-119">Se seu aplicativo do DirectShow der suporte à reprodução de arquivos protegidos por DRM, em geral, você não deve usar o **RenderFile** para criar o grafo de filtro porque não há como especificar quais direitos de DRM você está solicitando antes de o arquivo ser aberto.</span><span class="sxs-lookup"><span data-stu-id="877a3-119">If your DirectShow application supports playback of DRM-protected files, then you generally should not use **RenderFile** to create the filter graph because there is no way to specify which DRM rights you are requesting before the file is opened.</span></span> <span data-ttu-id="877a3-120">O leitor ASF do WM, por padrão, solicita apenas direitos de reprodução.</span><span class="sxs-lookup"><span data-stu-id="877a3-120">The WM ASF Reader by default asks for only playback rights.</span></span> <span data-ttu-id="877a3-121">O filtro não é adicionado ao grafo e, portanto, não é detectável por aplicativos, até que um arquivo seja aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="877a3-121">The filter is not added to the graph, and is therefore not discoverable by applications, until a file is successfully opened.</span></span>

<span data-ttu-id="877a3-122">Para criar um grafo de reprodução habilitado para DRM usando o [leitor ASF do WM](wm-asf-reader-filter.md), você deve criar uma instância do filtro usando **CoCreateInstance**, adicioná-lo ao grafo de filtro usando **IGraphBuilder:: AddFilter**, configurá-lo e renderizar seus PINs de saída.</span><span class="sxs-lookup"><span data-stu-id="877a3-122">To build a DRM-enabled playback graph using the [WM ASF Reader](wm-asf-reader-filter.md), you must instantiate the filter using **CoCreateInstance**, add it to the filter graph using **IGraphBuilder::AddFilter**, configure it, and then render its output pins.</span></span> <span data-ttu-id="877a3-123">Essa técnica é demonstrada no exemplo de PlayWndASF.</span><span class="sxs-lookup"><span data-stu-id="877a3-123">This technique is demonstrated in the PlayWndASF sample.</span></span> <span data-ttu-id="877a3-124">Ao criar o grafo dessa forma, você já tem o ponteiro **IBaseFilter** que pode ser usado para chamar o **QueryService** para obter o **IWMDRMWriter**.</span><span class="sxs-lookup"><span data-stu-id="877a3-124">When you build the graph in this way, you already have the **IBaseFilter** pointer that can be used to call **QueryService** to obtain **IWMDRMWriter**.</span></span> <span data-ttu-id="877a3-125">No entanto, essa interface não estará disponível até que o objeto leitor do Windows Media Format SDK seja criado internamente pelo leitor ASF do WM.</span><span class="sxs-lookup"><span data-stu-id="877a3-125">However, this interface is not available until the Windows Media Format SDK reader object is created internally by the WM ASF Reader.</span></span> <span data-ttu-id="877a3-126">A primeira oportunidade que o aplicativo tem para definir direitos de DRM está em seu \_ manipulador de eventos WMT no \_ Rights \_ ex, como mostrado neste trecho de código:</span><span class="sxs-lookup"><span data-stu-id="877a3-126">The first opportunity the application has to set DRM rights is in its WMT\_NO\_RIGHTS\_EX event handler, as shown in this code snippet:</span></span>


```C++
case WMT_NO_RIGHTS_EX:

    IServiceProvider *pServiceProvider;
    IWMDRMReader pWMDRMReader;
    JIF(g_pReader->QueryInterface(IID_IServiceProvider, (void **) &pServiceProvider));
    JIF(pServiceProvider->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader)); 
    SAFE_RELEASE(pServiceProvider);

    // Set the rights we want for this file. These are the actions we 
    // might want to perform on the file. Here we ask for two rights only.
    // In a real application you should enable users to select which 
    // rights they want.
    hr = pWMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
        BYTE*) wszRights, (sizeof(wszRights) / sizeof(wszRights[0])) * 2);
    SAFE_RELEASE(pWMDRMReader);
    if (FAILED(hr))
    {
       Msg(TEXT("SetDRMProperty Failed!  hr=0x%x\n"), hr);
       return hr;
    }
    // Now proceed with license acqusition.
    if( pEventData->pData )
    {
        hr = HandleNoRightsEx(pEventData->hrStatus, 
        (WM_GET_LICENSE_DATA *)pEventData->pData);
    }
    else
    {
         hr = E_FAIL;
    }
    break;

```



## <a name="related-topics"></a><span data-ttu-id="877a3-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="877a3-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="877a3-128">**Recursos de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="877a3-128">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="877a3-129">**Lista de atributos DRM**</span><span class="sxs-lookup"><span data-stu-id="877a3-129">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="877a3-130">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="877a3-130">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="877a3-131">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="877a3-131">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="877a3-132">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="877a3-132">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[<span data-ttu-id="877a3-133">**IWMDRMWriter**</span><span class="sxs-lookup"><span data-stu-id="877a3-133">**IWMDRMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




