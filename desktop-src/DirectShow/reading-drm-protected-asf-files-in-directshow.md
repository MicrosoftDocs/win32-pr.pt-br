---
description: Este tópico descreve como usar o DirectShow para reproduzir arquivos de mídia protegidos com o DRM (Windows Media Digital Rights Management).
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Lendo DRM-Protected arquivos ASF no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3a90b61982d6c7c444ddcf53948c225b6fc685
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105759431"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a><span data-ttu-id="fa583-103">Lendo DRM-Protected arquivos ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="fa583-103">Reading DRM-Protected ASF Files in DirectShow</span></span>

<span data-ttu-id="fa583-104">Este tópico descreve como usar o DirectShow para reproduzir arquivos de mídia protegidos com o DRM (Windows Media Digital Rights Management).</span><span class="sxs-lookup"><span data-stu-id="fa583-104">This topic describes how to use DirectShow to play media files that are protected with Windows Media Digital Rights Management (DRM).</span></span>

## <a name="drm-concepts"></a><span data-ttu-id="fa583-105">Conceitos de DRM</span><span class="sxs-lookup"><span data-stu-id="fa583-105">DRM Concepts</span></span>

<span data-ttu-id="fa583-106">A proteção de um arquivo de mídia com o Windows Media DRM envolve duas etapas distintas:</span><span class="sxs-lookup"><span data-stu-id="fa583-106">Protecting a media file with Windows Media DRM involves two distinct steps:</span></span>

-   <span data-ttu-id="fa583-107">O provedor de conteúdo empacota o arquivo, ou seja, criptografa o arquivo e anexa informações de licenciamento ao cabeçalho do arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="fa583-107">The content provider packages the file—that is, encrypts the file and attaches licensing information to the ASF file header.</span></span> <span data-ttu-id="fa583-108">As informações de licenciamento incluem uma URL onde o cliente pode obter a licença.</span><span class="sxs-lookup"><span data-stu-id="fa583-108">The licensing information includes a URL where the client can obtain the license.</span></span>
-   <span data-ttu-id="fa583-109">O aplicativo cliente adquire uma licença para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="fa583-109">The client application acquires a license for the content.</span></span>

<span data-ttu-id="fa583-110">O empacotamento ocorre antes de o arquivo ser distribuído.</span><span class="sxs-lookup"><span data-stu-id="fa583-110">Packaging happens before the file is distributed.</span></span> <span data-ttu-id="fa583-111">A aquisição de licença ocorre quando o usuário tenta reproduzir ou copiar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="fa583-111">License acquisition occurs when the user tries to play or copy the file.</span></span> <span data-ttu-id="fa583-112">A aquisição de licença pode ser *silenciosa* ou *não silenciosa*.</span><span class="sxs-lookup"><span data-stu-id="fa583-112">License acquisition may be either *silent* or *non-silent*.</span></span> <span data-ttu-id="fa583-113">A aquisição silenciosa não requer nenhuma interação com o usuário.</span><span class="sxs-lookup"><span data-stu-id="fa583-113">Silent acquisition does not require any interaction with the user.</span></span> <span data-ttu-id="fa583-114">A aquisição não silenciosa exige que o aplicativo abra uma janela do navegador e exiba uma página da Web para o usuário.</span><span class="sxs-lookup"><span data-stu-id="fa583-114">Non-silent acquisition requires the application to open a browser window and display a web page to the user.</span></span> <span data-ttu-id="fa583-115">Nesse ponto, o usuário pode precisar fornecer algum tipo de informação ao provedor de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="fa583-115">At that point, the user might need to provide some kind of information to the content provider.</span></span> <span data-ttu-id="fa583-116">No entanto, os dois tipos de aquisição de licença exigem que o cliente envie uma solicitação HTTP para um servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="fa583-116">However, both types of license acquisition require the client to submit an HTTP request to a license server.</span></span>

### <a name="drm-versions"></a><span data-ttu-id="fa583-117">Versões de DRM</span><span class="sxs-lookup"><span data-stu-id="fa583-117">DRM Versions</span></span>

<span data-ttu-id="fa583-118">Existem várias versões do Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="fa583-118">Several versions of Windows Media DRM exist.</span></span> <span data-ttu-id="fa583-119">Da perspectiva de um aplicativo cliente, eles podem ser agrupados em duas categorias: DRM versão 1 e DRM versão 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="fa583-119">From the perspective of a client application, they can be grouped into two categories: DRM version 1, and DRM version 7 or later.</span></span> <span data-ttu-id="fa583-120">(A segunda categoria inclui as versões 9 e 10 do DRM, bem como a versão 7.) O motivo para categorizar as versões de DRM dessa forma é que as licenças da versão 1 são tratadas de forma ligeiramente diferente da versão 7 ou licenças posteriores.</span><span class="sxs-lookup"><span data-stu-id="fa583-120">(The second category includes DRM versions 9 and 10, as well as version 7.) The reason for categorizing DRM versions this way is that version 1 licenses are handled somewhat differently than version 7 or later licenses.</span></span> <span data-ttu-id="fa583-121">Nesta documentação, o termo *licença versão 7* significa versão 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="fa583-121">In this documentation, the term *version 7 license* means version 7 or later.</span></span>

<span data-ttu-id="fa583-122">Também é importante distinguir o empacotamento DRM da licença DRM.</span><span class="sxs-lookup"><span data-stu-id="fa583-122">It is also important to distinguish the DRM packaging from the DRM license.</span></span> <span data-ttu-id="fa583-123">Se o arquivo for empacotado usando o Windows Media Rights Manager versão 7 ou posterior, o cabeçalho DRM poderá conter uma URL de licença da versão 1, além da URL de licença da versão 7.</span><span class="sxs-lookup"><span data-stu-id="fa583-123">If the file is packaged using Windows Media Rights Manager version 7 or later, the DRM header can contain a version 1 license URL in addition to the version 7 license URL.</span></span> <span data-ttu-id="fa583-124">A URL de licença da versão 1 Habilita players mais antigos que não dão suporte à versão 7 para obter uma licença para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="fa583-124">The version 1 license URL enables older players that do not support version 7 to obtain a license for the content.</span></span> <span data-ttu-id="fa583-125">No entanto, o inverso não é verdadeiro, portanto, um arquivo com o empacotamento da versão 1 não pode ter uma URL de licença da versão 7.</span><span class="sxs-lookup"><span data-stu-id="fa583-125">However, the converse is not true, so a file with version 1 packaging cannot have a version 7 license URL.</span></span>

### <a name="application-security-level"></a><span data-ttu-id="fa583-126">Nível de segurança do aplicativo</span><span class="sxs-lookup"><span data-stu-id="fa583-126">Application Security Level</span></span>

<span data-ttu-id="fa583-127">Para reproduzir arquivos protegidos por DRM, o aplicativo cliente deve ser vinculado a uma biblioteca estática que é fornecida em formato binário pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fa583-127">To play DRM-protected files, the client application must be linked to a static library that is provided in binary form by Microsoft.</span></span> <span data-ttu-id="fa583-128">Essa biblioteca, que identifica exclusivamente o aplicativo, às vezes é chamada de biblioteca de stub.</span><span class="sxs-lookup"><span data-stu-id="fa583-128">This library, which uniquely identifies the application, is sometimes called the stub library.</span></span> <span data-ttu-id="fa583-129">A biblioteca de stub tem um nível de segurança atribuído, o valor que é determinado pelo contrato de licença que você assinou quando obteve a biblioteca de stub.</span><span class="sxs-lookup"><span data-stu-id="fa583-129">The stub library has an assigned security level, the value of which is determined by the license agreement that you signed when you obtained the stub library.</span></span>

<span data-ttu-id="fa583-130">O provedor de conteúdo define um nível de segurança mínimo necessário para adquirir a licença.</span><span class="sxs-lookup"><span data-stu-id="fa583-130">The content provider sets a minimum security level needed to acquire the license.</span></span> <span data-ttu-id="fa583-131">Se o nível de segurança da sua biblioteca de stub for menor que o nível mínimo de segurança exigido pelo servidor de licença, o aplicativo não poderá obter a licença.</span><span class="sxs-lookup"><span data-stu-id="fa583-131">If the security level of your stub library is less than the minimum security level required by the license server, the application cannot obtain the license.</span></span>

### <a name="individualization"></a><span data-ttu-id="fa583-132">Individualização</span><span class="sxs-lookup"><span data-stu-id="fa583-132">Individualization</span></span>

<span data-ttu-id="fa583-133">Para aumentar a segurança, um aplicativo pode atualizar os componentes DRM no computador do cliente.</span><span class="sxs-lookup"><span data-stu-id="fa583-133">To increase security, an application may update the DRM components on the client's computer.</span></span> <span data-ttu-id="fa583-134">Essa atualização, chamada individualização, diferencia a cópia do aplicativo do usuário de todas as outras cópias do mesmo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fa583-134">This update, called individualization, differentiates the user's copy of the application from all other copies of the same application.</span></span> <span data-ttu-id="fa583-135">O cabeçalho DRM de um arquivo protegido pode especificar pode especificar um nível de individualização mínimo.</span><span class="sxs-lookup"><span data-stu-id="fa583-135">The DRM header of a protected file may specify may specify a minimum individualization level.</span></span> <span data-ttu-id="fa583-136">(Para obter mais informações, consulte a documentação de WMRMHeader. IndividualizedVersion no SDK do Windows Media Rights Manager.)</span><span class="sxs-lookup"><span data-stu-id="fa583-136">(For more information, see the documentation for WMRMHeader.IndividualizedVersion in the Windows Media Rights Manager SDK.)</span></span>

<span data-ttu-id="fa583-137">Como o serviço de individualização da Microsoft manipula informações do usuário, você deve exibir a política de privacidade da Microsoft ou fornecer um link para essa página no site da Microsoft antes do seu aplicativo individualizes: <https://go.microsoft.com/fwlink/p/?linkid=10240> .</span><span class="sxs-lookup"><span data-stu-id="fa583-137">Because the Microsoft Individualization Service handles information from the user, you must display the Microsoft privacy policy or provide a link to that page at the Microsoft website before your application individualizes: <https://go.microsoft.com/fwlink/p/?linkid=10240>.</span></span>

## <a name="provide-the-software-certificate"></a><span data-ttu-id="fa583-138">Fornecer o certificado de software</span><span class="sxs-lookup"><span data-stu-id="fa583-138">Provide the Software Certificate</span></span>

<span data-ttu-id="fa583-139">Para permitir que o aplicativo use a licença DRM, o aplicativo deve fornecer um certificado de software ou *chave* para o Gerenciador de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="fa583-139">To enable the application to use the DRM license, the application must provide a software certificate or *key* to the Filter Graph Manager.</span></span> <span data-ttu-id="fa583-140">Essa chave está contida em uma biblioteca estática que é individualizada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fa583-140">This key is contained in a static library that is individualized for the application.</span></span> <span data-ttu-id="fa583-141">Para obter informações sobre como obter a biblioteca individualizada, consulte [obtendo a biblioteca de DRM necessária](../wmformat/obtaining-the-required-drm-library.md) na documentação do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="fa583-141">For information about obtaining the individualized library, see [Obtaining the Required DRM Library](../wmformat/obtaining-the-required-drm-library.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="fa583-142">Para fornecer a chave de software, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="fa583-142">To provide the software key, perform the following steps:</span></span>

1.  <span data-ttu-id="fa583-143">Link para a biblioteca estática.</span><span class="sxs-lookup"><span data-stu-id="fa583-143">Link to the static library.</span></span>
2.  <span data-ttu-id="fa583-144">Implemente a interface **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="fa583-144">Implement the **IServiceProvider** interface.</span></span>
3.  <span data-ttu-id="fa583-145">Consulte o Gerenciador de gráfico de filtro para a interface [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) .</span><span class="sxs-lookup"><span data-stu-id="fa583-145">Query the Filter Graph Manager for the [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) interface.</span></span>
4.  <span data-ttu-id="fa583-146">Chame [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) com um ponteiro para sua implementação de **IServiceProvider**.</span><span class="sxs-lookup"><span data-stu-id="fa583-146">Call [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) with a pointer to your implementation of **IServiceProvider**.</span></span>
5.  <span data-ttu-id="fa583-147">O Gerenciador de gráfico de filtro chamará **IServiceProvider:: QueryService**, especificando **IID \_ IWMReader** para o identificador de serviço.</span><span class="sxs-lookup"><span data-stu-id="fa583-147">The Filter Graph Manager will call **IServiceProvider::QueryService**, specifying **IID\_IWMReader** for the service identifier.</span></span>
6.  <span data-ttu-id="fa583-148">Em sua implementação de **QueryService**, chame [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) para criar a chave de software.</span><span class="sxs-lookup"><span data-stu-id="fa583-148">In your implementation of **QueryService**, call [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) to create the software key.</span></span>

<span data-ttu-id="fa583-149">O código a seguir mostra como implementar o método **QueryService** :</span><span class="sxs-lookup"><span data-stu-id="fa583-149">The following code shows how to implement the **QueryService** method:</span></span>


```C++
STDMETHODIMP Player::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (ppv == NULL ) 
    { 
        return E_POINTER; 
    }

    if (siid == __uuidof(IWMReader) && riid == __uuidof(IUnknown))
    {
        IUnknown *punkCert;

        HRESULT hr = WMCreateCertificate(&punkCert);

        if (SUCCEEDED(hr))
        {
            *ppv = (void *) punkCert;
        }

        return hr;
    }
    return E_NOINTERFACE;
}
```



<span data-ttu-id="fa583-150">O código a seguir mostra como chamar [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) no Gerenciador de gráfico de filtro:</span><span class="sxs-lookup"><span data-stu-id="fa583-150">The following code shows how to call [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) on the Filter Graph Manager:</span></span>


```C++
HRESULT Player::CreateFilterGraph()
{
    CComPtr<IObjectWithSite> pSite;

    HRESULT hr = pGraph.CoCreateInstance(CLSID_FilterGraph);

    if (FAILED(hr))
    {
        goto done;
    }

    // Register the application as a site (service).
    hr = pGraph->QueryInterface(&pSite);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSite->SetSite(this);


done:
    return hr;
}
```





## <a name="building-the-playback-graph"></a><span data-ttu-id="fa583-151">Criando o grafo de reprodução</span><span class="sxs-lookup"><span data-stu-id="fa583-151">Building the Playback Graph</span></span>

<span data-ttu-id="fa583-152">Para reproduzir um arquivo ASF protegido por DRM, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="fa583-152">To play a DRM-protected ASF file, perform the following steps:</span></span>

1.  <span data-ttu-id="fa583-153">Crie o [Gerenciador de gráfico de filtro](filter-graph-manager.md) e use a interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) para se registrar em eventos de grafo.</span><span class="sxs-lookup"><span data-stu-id="fa583-153">Create the [Filter Graph Manager](filter-graph-manager.md) and use the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface to register for graph events.</span></span>
2.  <span data-ttu-id="fa583-154">Chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma nova instância do filtro de [leitor ASF do WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="fa583-154">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a new instance of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>
3.  <span data-ttu-id="fa583-155">Chame [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para adicionar o filtro ao grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="fa583-155">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the filter graph.</span></span>
4.  <span data-ttu-id="fa583-156">Consulte o filtro para a interface [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .</span><span class="sxs-lookup"><span data-stu-id="fa583-156">Query the filter for the [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interface.</span></span>
5.  <span data-ttu-id="fa583-157">Chame [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) com a URL do arquivo.</span><span class="sxs-lookup"><span data-stu-id="fa583-157">Call [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) with the URL of the file.</span></span>
6.  <span data-ttu-id="fa583-158">Manipule eventos de [**\_ \_ evento do EC WMT**](ec-wmt-event.md) .</span><span class="sxs-lookup"><span data-stu-id="fa583-158">Handle [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span>
7.  <span data-ttu-id="fa583-159">No primeiro evento [**de \_ \_ evento do EC WMT**](ec-wmt-event.md) , consulte o filtro de [leitor ASF do WM](wm-asf-reader-filter.md) para a interface **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="fa583-159">On the first [**EC\_WMT\_EVENT**](ec-wmt-event.md) event, query the [WM ASF Reader](wm-asf-reader-filter.md) filter for the **IServiceProvider** interface.</span></span>
8.  <span data-ttu-id="fa583-160">Chame **IServiceProvider:: QueryService** para obter um ponteiro para a interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .</span><span class="sxs-lookup"><span data-stu-id="fa583-160">Call **IServiceProvider::QueryService** to get a pointer to the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface.</span></span>
9.  <span data-ttu-id="fa583-161">Chame [**IGraphBuilder:: render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para renderizar os Pins de saída do filtro de [leitor ASF do WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="fa583-161">Call [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) to render the output pins of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>

> [!Note]  
> <span data-ttu-id="fa583-162">Ao abrir um arquivo protegido por DRM, não chame [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) para criar o grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="fa583-162">When opening a DRM-protected file, do not call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) to create the filter graph.</span></span> <span data-ttu-id="fa583-163">O filtro de leitor ASF do WM não pode se conectar a nenhum outro filtro até que a licença DRM seja adquirida.</span><span class="sxs-lookup"><span data-stu-id="fa583-163">The WM ASF Reader filter cannot connect to any other filters until the DRM license is acquired.</span></span> <span data-ttu-id="fa583-164">Esta etapa requer que o aplicativo use a interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) , que deve ser obtida do filtro, conforme descrito nas etapas 7 a 8.</span><span class="sxs-lookup"><span data-stu-id="fa583-164">This step requires the application to use the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface, which must be obtained from the filter, as described in steps 7–8.</span></span> <span data-ttu-id="fa583-165">Portanto, você deve criar o filtro e adicioná-lo ao grafo</span><span class="sxs-lookup"><span data-stu-id="fa583-165">Therefore, you must create the filter and add it to the graph</span></span>

 

> [!Note]  
> <span data-ttu-id="fa583-166">É importante registrar-se para eventos de grafo (etapa 1) antes de adicionar o filtro de [leitor ASF do WM](wm-asf-reader-filter.md) ao grafo (etapa 3), pois o aplicativo deve lidar com os eventos de [**evento do EC \_ WMT \_**](ec-wmt-event.md) .</span><span class="sxs-lookup"><span data-stu-id="fa583-166">It is important to register for graph events (step 1) before adding the [WM ASF Reader](wm-asf-reader-filter.md) filter to the graph (step 3), because the application must handle the [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span> <span data-ttu-id="fa583-167">Os eventos são enviados quando o [**carregamento**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) é chamado (etapa 5).</span><span class="sxs-lookup"><span data-stu-id="fa583-167">The events are sent when [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) is called (step 5).</span></span>

 

<span data-ttu-id="fa583-168">O código a seguir mostra como criar o grafo:</span><span class="sxs-lookup"><span data-stu-id="fa583-168">The following code shows how to build the graph:</span></span>


```C++
HRESULT Player::LoadMediaFile(PCWSTR pwszFile)
{


    BOOL bIsWindowsMediaFile = IsWindowsMediaFile(pwszFile);

    HRESULT hr = S_OK;

    // If this is the first time opening the file, create the
    // filter graph and add the WM ASF Reader filter.

    if (m_DRM.State() == DRM_INITIAL)
    {
        hr = CreateFilterGraph();
        if (FAILED(hr))
        {
            goto done;
        }

        // Use special handling for Windows Media files.
        if (bIsWindowsMediaFile)
        {
            // Add the ASF Reader filter to the graph.
            hr = m_pReader.CoCreateInstance(CLSID_WMAsfReader);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pGraph->AddFilter(m_pReader, NULL);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = m_pReader->QueryInterface(&m_pFileSource);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    }

    if (bIsWindowsMediaFile)
    {
            hr = m_pFileSource->Load(pwszFile, NULL);
```

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa583-169">C++</span><span class="sxs-lookup"><span data-stu-id="fa583-169">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            if (FAILED(hr))
            {
                goto done;
            }
            hr = RenderOutputPins(pGraph, m_pReader);
    }
    else
    {
        // Not a Windows Media file, so just render the standard way.
        hr = pGraph->RenderFile(pwszFile, NULL);
    }

done:
    return hr;
}</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="fa583-170">No código anterior, a `RenderOutputPins` função enumera os Pins de saída no filtro de [leitor ASF do WM](wm-asf-reader-filter.md) e chama [**IGraphBuilder:: render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para cada PIN.</span><span class="sxs-lookup"><span data-stu-id="fa583-170">In the previous code, the `RenderOutputPins` function enumerates the output pins on the [WM ASF Reader](wm-asf-reader-filter.md) filter and calls [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) for each pin.</span></span>


```C++
HRESULT RenderOutputPins(IGraphBuilder *pGraph, IBaseFilter *pFilter)
{
    CComPtr<IEnumPins>  pEnumPin = NULL;
    CComPtr<IPin>       pConnectedPin;
    CComPtr<IPin>       pPin;

    // Enumerate all pins on the filter
    HRESULT hr = pFilter->EnumPins(&pEnumPin);
    if (FAILED(hr))
    {
        goto done;
    }

    // Step through every pin, looking for the output pins.
    while (S_OK == (hr = pEnumPin->Next(1, &pPin, NULL)))
    {
        // Skip connected pins.
        hr = pPin->ConnectedTo(&pConnectedPin);
        if (hr == VFW_E_NOT_CONNECTED)
        {
            PIN_DIRECTION PinDirection;
            hr = pPin->QueryDirection(&PinDirection);

            if ((S_OK == hr) && (PinDirection == PINDIR_OUTPUT))
            {
                hr = pGraph->Render(pPin);
            }
        }

        pConnectedPin.Release();
        pPin.Release();

        // If there was an error, stop enumerating.
        if (FAILED(hr))
        {
            break;
        }
    }

done:
    return hr;
}
```



<span data-ttu-id="fa583-171">O código a seguir mostra como obter um ponteiro para a interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) do [leitor ASF do WM](wm-asf-reader-filter.md):</span><span class="sxs-lookup"><span data-stu-id="fa583-171">The following code shows how to get a pointer to the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface from the [WM ASF Reader](wm-asf-reader-filter.md):</span></span>


```C++
HRESULT DrmManager::Initialize(IBaseFilter *pFilter)
{


    CComPtr<IServiceProvider> pService;
    CComPtr<IWMDRMReader> pDrmReader;

    HRESULT hr = pFilter->QueryInterface(&pService);
    if (SUCCEEDED(hr))
    {
        hr = pService->QueryService(
            __uuidof(IWMDRMReader), IID_PPV_ARGS(&m_pDrmReader));
    }
    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="fa583-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa583-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa583-173">Lendo arquivos ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="fa583-173">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
