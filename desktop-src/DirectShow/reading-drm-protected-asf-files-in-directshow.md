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
# <a name="reading-drm-protected-asf-files-in-directshow"></a>Lendo DRM-Protected arquivos ASF no DirectShow

Este tópico descreve como usar o DirectShow para reproduzir arquivos de mídia protegidos com o DRM (Windows Media Digital Rights Management).

## <a name="drm-concepts"></a>Conceitos de DRM

A proteção de um arquivo de mídia com o Windows Media DRM envolve duas etapas distintas:

-   O provedor de conteúdo empacota o arquivo, ou seja, criptografa o arquivo e anexa informações de licenciamento ao cabeçalho do arquivo ASF. As informações de licenciamento incluem uma URL onde o cliente pode obter a licença.
-   O aplicativo cliente adquire uma licença para o conteúdo.

O empacotamento ocorre antes de o arquivo ser distribuído. A aquisição de licença ocorre quando o usuário tenta reproduzir ou copiar o arquivo. A aquisição de licença pode ser *silenciosa* ou *não silenciosa*. A aquisição silenciosa não requer nenhuma interação com o usuário. A aquisição não silenciosa exige que o aplicativo abra uma janela do navegador e exiba uma página da Web para o usuário. Nesse ponto, o usuário pode precisar fornecer algum tipo de informação ao provedor de conteúdo. No entanto, os dois tipos de aquisição de licença exigem que o cliente envie uma solicitação HTTP para um servidor de licença.

### <a name="drm-versions"></a>Versões de DRM

Existem várias versões do Windows Media DRM. Da perspectiva de um aplicativo cliente, eles podem ser agrupados em duas categorias: DRM versão 1 e DRM versão 7 ou posterior. (A segunda categoria inclui as versões 9 e 10 do DRM, bem como a versão 7.) O motivo para categorizar as versões de DRM dessa forma é que as licenças da versão 1 são tratadas de forma ligeiramente diferente da versão 7 ou licenças posteriores. Nesta documentação, o termo *licença versão 7* significa versão 7 ou posterior.

Também é importante distinguir o empacotamento DRM da licença DRM. Se o arquivo for empacotado usando o Windows Media Rights Manager versão 7 ou posterior, o cabeçalho DRM poderá conter uma URL de licença da versão 1, além da URL de licença da versão 7. A URL de licença da versão 1 Habilita players mais antigos que não dão suporte à versão 7 para obter uma licença para o conteúdo. No entanto, o inverso não é verdadeiro, portanto, um arquivo com o empacotamento da versão 1 não pode ter uma URL de licença da versão 7.

### <a name="application-security-level"></a>Nível de segurança do aplicativo

Para reproduzir arquivos protegidos por DRM, o aplicativo cliente deve ser vinculado a uma biblioteca estática que é fornecida em formato binário pela Microsoft. Essa biblioteca, que identifica exclusivamente o aplicativo, às vezes é chamada de biblioteca de stub. A biblioteca de stub tem um nível de segurança atribuído, o valor que é determinado pelo contrato de licença que você assinou quando obteve a biblioteca de stub.

O provedor de conteúdo define um nível de segurança mínimo necessário para adquirir a licença. Se o nível de segurança da sua biblioteca de stub for menor que o nível mínimo de segurança exigido pelo servidor de licença, o aplicativo não poderá obter a licença.

### <a name="individualization"></a>Individualização

Para aumentar a segurança, um aplicativo pode atualizar os componentes DRM no computador do cliente. Essa atualização, chamada individualização, diferencia a cópia do aplicativo do usuário de todas as outras cópias do mesmo aplicativo. O cabeçalho DRM de um arquivo protegido pode especificar pode especificar um nível de individualização mínimo. (Para obter mais informações, consulte a documentação de WMRMHeader. IndividualizedVersion no SDK do Windows Media Rights Manager.)

Como o serviço de individualização da Microsoft manipula informações do usuário, você deve exibir a política de privacidade da Microsoft ou fornecer um link para essa página no site da Microsoft antes do seu aplicativo individualizes: <https://go.microsoft.com/fwlink/p/?linkid=10240> .

## <a name="provide-the-software-certificate"></a>Fornecer o certificado de software

Para permitir que o aplicativo use a licença DRM, o aplicativo deve fornecer um certificado de software ou *chave* para o Gerenciador de gráfico de filtro. Essa chave está contida em uma biblioteca estática que é individualizada para o aplicativo. Para obter informações sobre como obter a biblioteca individualizada, consulte [obtendo a biblioteca de DRM necessária](../wmformat/obtaining-the-required-drm-library.md) na documentação do SDK do Windows Media Format.

Para fornecer a chave de software, execute as seguintes etapas:

1.  Link para a biblioteca estática.
2.  Implemente a interface **IServiceProvider** .
3.  Consulte o Gerenciador de gráfico de filtro para a interface [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) .
4.  Chame [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) com um ponteiro para sua implementação de **IServiceProvider**.
5.  O Gerenciador de gráfico de filtro chamará **IServiceProvider:: QueryService**, especificando **IID \_ IWMReader** para o identificador de serviço.
6.  Em sua implementação de **QueryService**, chame [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) para criar a chave de software.

O código a seguir mostra como implementar o método **QueryService** :


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



O código a seguir mostra como chamar [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) no Gerenciador de gráfico de filtro:


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





## <a name="building-the-playback-graph"></a>Criando o grafo de reprodução

Para reproduzir um arquivo ASF protegido por DRM, execute as seguintes etapas:

1.  Crie o [Gerenciador de gráfico de filtro](filter-graph-manager.md) e use a interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) para se registrar em eventos de grafo.
2.  Chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma nova instância do filtro de [leitor ASF do WM](wm-asf-reader-filter.md) .
3.  Chame [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para adicionar o filtro ao grafo de filtro.
4.  Consulte o filtro para a interface [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .
5.  Chame [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) com a URL do arquivo.
6.  Manipule eventos de [**\_ \_ evento do EC WMT**](ec-wmt-event.md) .
7.  No primeiro evento [**de \_ \_ evento do EC WMT**](ec-wmt-event.md) , consulte o filtro de [leitor ASF do WM](wm-asf-reader-filter.md) para a interface **IServiceProvider** .
8.  Chame **IServiceProvider:: QueryService** para obter um ponteiro para a interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .
9.  Chame [**IGraphBuilder:: render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para renderizar os Pins de saída do filtro de [leitor ASF do WM](wm-asf-reader-filter.md) .

> [!Note]  
> Ao abrir um arquivo protegido por DRM, não chame [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) para criar o grafo de filtro. O filtro de leitor ASF do WM não pode se conectar a nenhum outro filtro até que a licença DRM seja adquirida. Esta etapa requer que o aplicativo use a interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) , que deve ser obtida do filtro, conforme descrito nas etapas 7 a 8. Portanto, você deve criar o filtro e adicioná-lo ao grafo

 

> [!Note]  
> É importante registrar-se para eventos de grafo (etapa 1) antes de adicionar o filtro de [leitor ASF do WM](wm-asf-reader-filter.md) ao grafo (etapa 3), pois o aplicativo deve lidar com os eventos de [**evento do EC \_ WMT \_**](ec-wmt-event.md) . Os eventos são enviados quando o [**carregamento**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) é chamado (etapa 5).

 

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

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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



No código anterior, a `RenderOutputPins` função enumera os Pins de saída no filtro de [leitor ASF do WM](wm-asf-reader-filter.md) e chama [**IGraphBuilder:: render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para cada PIN.


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



O código a seguir mostra como obter um ponteiro para a interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) do [leitor ASF do WM](wm-asf-reader-filter.md):


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

 

 
