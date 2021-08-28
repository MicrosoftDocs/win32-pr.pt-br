---
description: Este tópico descreve como usar o DirectShow para reproduzir arquivos de mídia protegidos com o DRM (Windows Media Digital Rights Management).
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Lendo DRM-Protected arquivos ASF no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178dc0dbaa9a8b8e2e849164106816afc6990c89
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786962"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a>Lendo DRM-Protected arquivos ASF no DirectShow

Este tópico descreve como usar o DirectShow para reproduzir arquivos de mídia protegidos com o DRM (Windows Media Digital Rights Management).

## <a name="drm-concepts"></a>Conceitos de DRM

Proteger um arquivo de mídia com Windows DRM de Mídia envolve duas etapas distintas:

-   O provedor de conteúdo pacotes o arquivo , ou seja, criptografa o arquivo e anexa informações de licenciamento ao título do arquivo ASF. As informações de licenciamento incluem uma URL em que o cliente pode obter a licença.
-   O aplicativo cliente adquire uma licença para o conteúdo.

O empacotamento ocorre antes que o arquivo seja distribuído. A aquisição de licença ocorre quando o usuário tenta reproduzir ou copiar o arquivo. A aquisição de licença *pode ser silenciosa* ou não *silenciosa.* A aquisição silenciosa não exige nenhuma interação com o usuário. A aquisição não silenciosa exige que o aplicativo abra uma janela do navegador e exibir uma página da Web para o usuário. Nesse ponto, o usuário pode precisar fornecer algum tipo de informação para o provedor de conteúdo. No entanto, os dois tipos de aquisição de licença exigem que o cliente envie uma solicitação HTTP para um servidor de licença.

### <a name="drm-versions"></a>Versões do DRM

Existem várias versões Windows DRM de Mídia. Da perspectiva de um aplicativo cliente, eles podem ser agrupados em duas categorias: DRM versão 1 e DRM versão 7 ou posterior. (A segunda categoria inclui as versões 9 e 10 do DRM, bem como a versão 7.) O motivo para categorizar versões de DRM dessa maneira é que as licenças da versão 1 são tratadas de forma um pouco diferente das licenças da versão 7 ou posteriores. Nesta documentação, o termo *licença versão 7 significa* versão 7 ou posterior.

Também é importante distinguir o empacotamento DRM da licença drm. Se o arquivo for empacotado usando o Windows Media Rights Manager versão 7 ou posterior, o header drm poderá conter uma URL de licença da versão 1, além da URL de licença da versão 7. A URL de licença da versão 1 permite que players mais antigos que não têm suporte para a versão 7 obtenham uma licença para o conteúdo. No entanto, o inverso não é verdadeiro, portanto, um arquivo com empacotamento da versão 1 não pode ter uma URL de licença da versão 7.

### <a name="application-security-level"></a>Nível de segurança do aplicativo

Para reproduzir arquivos protegidos por DRM, o aplicativo cliente deve estar vinculado a uma biblioteca estática fornecida em formato binário pela Microsoft. Essa biblioteca, que identifica exclusivamente o aplicativo, às vezes é chamada de biblioteca de stub. A biblioteca de stub tem um nível de segurança atribuído, que é determinado pelo contrato de licença assinado quando você obteve a biblioteca de stub.

O provedor de conteúdo define um nível de segurança mínimo necessário para adquirir a licença. Se o nível de segurança da biblioteca de stub for menor que o nível de segurança mínimo exigido pelo servidor de licença, o aplicativo não poderá obter a licença.

### <a name="individualization"></a>Individualização

Para aumentar a segurança, um aplicativo pode atualizar os componentes drm no computador do cliente. Essa atualização, chamada individualização, diferencia a cópia do aplicativo do usuário de todas as outras cópias do mesmo aplicativo. O header DRM de um arquivo protegido pode especificar pode especificar um nível mínimo de individualização. (Para obter mais informações, consulte a documentação do WMRMHeader.IndividualizedVersion no SDK Windows Media Rights Manager.)

Como o Serviço de Individualização da Microsoft lida com informações do usuário, você deve exibir a política de privacidade da Microsoft ou fornecer um link para essa página no site da Microsoft antes que seu aplicativo seja individualizado: <https://go.microsoft.com/fwlink/p/?linkid=10240> .

## <a name="provide-the-software-certificate"></a>Fornecer o certificado de software

Para permitir que o aplicativo use a licença drm, o aplicativo deve fornecer um certificado de software ou *uma* chave para o Gerenciador Graph Filtro. Essa chave está contida em uma biblioteca estática individualizada para o aplicativo. Para obter informações sobre como obter a biblioteca individualizada, consulte Obtendo a biblioteca [DRM](../wmformat/obtaining-the-required-drm-library.md) necessária na documentação do SDK Windows Formato de Mídia.

Para fornecer a chave de software, execute as seguintes etapas:

1.  Link para a biblioteca estática.
2.  Implemente a interface **IServiceProvider.**
3.  Consulte a interface Filter Graph Manager para a interface [**IObjectWithSite.**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
4.  Chame [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) com um ponteiro para sua implementação **de IServiceProvider.**
5.  O Gerenciador Graph Filtro chamará **IServiceProvider::QueryService**, especificando **IID \_ IWMReader** para o identificador de serviço.
6.  Em sua implementação de **QueryService,** chame [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) para criar a chave de software.

O código a seguir mostra como implementar o **método QueryService:**


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



O código a seguir mostra como chamar [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) no Gerenciador de Graph Filtro:


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





## <a name="building-the-playback-graph"></a>Criando o controle de reprodução Graph

Para executar um arquivo ASF protegido por DRM, execute as seguintes etapas:

1.  Crie o [Gerenciador Graph Filtro e](filter-graph-manager.md) use a interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) para registrar eventos de grafo.
2.  Chame [**CoCreateInstance para**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) criar uma nova instância do filtro [Leitor do WM ASF.](wm-asf-reader-filter.md)
3.  Chame [**IFilterGraph::AddFilter para**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) adicionar o filtro ao grafo de filtro.
4.  Consulte o filtro para a interface [**IFileSourceFilter.**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)
5.  Chame [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) com a URL do arquivo.
6.  Manipular [**eventos \_ EC WMT \_ EVENT.**](ec-wmt-event.md)
7.  No primeiro evento [**\_ EC WMT \_ EVENT,**](ec-wmt-event.md) consulte o filtro [Leitor do WM ASF](wm-asf-reader-filter.md) para a interface **IServiceProvider.**
8.  Chame **IServiceProvider::QueryService** para obter um ponteiro para a interface [**IWMDRMReader.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
9.  Chame [**IGraphBuilder::Render para**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) renderizar os pinos de saída do filtro [Leitor do WM ASF.](wm-asf-reader-filter.md)

> [!Note]  
> Ao abrir um arquivo protegido por DRM, não chame [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) para criar o grafo de filtro. O filtro Leitor do WM ASF não pode se conectar a nenhum outro filtro até que a licença drm seja adquirida. Esta etapa exige que o aplicativo use a interface [**IWMDRMReader,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) que deve ser obtida do filtro, conforme descrito nas etapas 7 a 8. Portanto, você deve criar o filtro e adicioná-lo ao grafo

 

> [!Note]  
> É importante registrar-se para eventos de grafo (etapa 1) antes de adicionar o filtro [leitor do WM ASF](wm-asf-reader-filter.md) ao grafo (etapa 3), porque o aplicativo deve manipular os eventos [**EC \_ WMT \_ EVENT.**](ec-wmt-event.md) Os eventos são enviados quando [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) é chamado (etapa 5).

 

O código a seguir mostra como criar o grafo:


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




| C++ | 
|-----|
| <pre><code>            if (FAILED(hr))            {                goto done;            }            hr = RenderOutputPins(pGraph, m_pReader);    }    else    {        // Not a Windows Media file, so just render the standard way.        hr = pGraph-&gt;RenderFile(pwszFile, NULL);    }done:    return hr;}</code></pre> | 




No código anterior, a função enumera os pinos de saída no filtro leitor do WM ASF e chama `RenderOutputPins` [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para cada pino. [](wm-asf-reader-filter.md)


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



O código a seguir mostra como obter um ponteiro para a interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) do [Leitor do WM ASF:](wm-asf-reader-filter.md)


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





## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
