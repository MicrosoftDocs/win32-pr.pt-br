---
description: este tópico descreve como dar suporte a DXVA (DirectX Video Acceleration) 2,0 em um filtro de decodificador DirectShow.
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: Suporte a DXVA 2,0 no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58631a407e42c0561ebee0ad2b3187e248fc2d25dc0bdf4e98ed0219d8dae916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238079"
---
# <a name="supporting-dxva-20-in-directshow"></a>Suporte a DXVA 2,0 no DirectShow

este tópico descreve como dar suporte a DXVA (DirectX Video Acceleration) 2,0 em um filtro de decodificador DirectShow. Especificamente, ele descreve a comunicação entre o decodificador e o processador de vídeo. Este tópico não descreve como implementar a decodificação de DXVA.

-   [Pré-requisitos](#prerequisites)
-   [Notas de migração](#migration-notes)
-   [Encontrando uma configuração de decodificador](#finding-a-decoder-configuration)
-   [Notificando o renderizador de vídeo](#notifying-the-video-renderer)
-   [Alocando buffers descompactados](#allocating-uncompressed-buffers)
-   [Decodificação](#decoding)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

este tópico pressupõe que você esteja familiarizado com a gravação de filtros de DirectShow. para obter mais informações, consulte o tópico [Writing DirectShow filters](../directshow/writing-directshow-filters.md) na documentação do SDK do DirectShow. Os exemplos de código neste tópico pressupõem que o filtro de decodificador seja derivado da classe [**CTransformFilter**](../directshow/ctransformfilter.md) , com a seguinte definição de classe:


```C++
class CDecoder : public CTransformFilter
{
public:
    static CUnknown* WINAPI CreateInstance(IUnknown *pUnk, HRESULT *pHr);

    HRESULT CompleteConnect(PIN_DIRECTION direction, IPin *pPin);

    HRESULT InitAllocator(IMemAllocator **ppAlloc);
    HRESULT DecideBufferSize(IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp);

    // TODO: The implementations of these methods depend on the specific decoder.
    HRESULT CheckInputType(const CMediaType *mtIn);
    HRESULT CheckTransform(const CMediaType *mtIn, const CMediaType *mtOut);
    HRESULT CTransformFilter::GetMediaType(int,CMediaType *);

private:
    CDecoder(HRESULT *pHr);
    ~CDecoder();

    CBasePin * GetPin(int n);

    HRESULT ConfigureDXVA2(IPin *pPin);
    HRESULT SetEVRForDXVA2(IPin *pPin);

    HRESULT FindDecoderConfiguration(
        /* [in] */  IDirectXVideoDecoderService *pDecoderService,
        /* [in] */  const GUID& guidDecoder, 
        /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
        /* [out] */ BOOL *pbFoundDXVA2Configuration
        );

private:
    IDirectXVideoDecoderService *m_pDecoderService;

    DXVA2_ConfigPictureDecode m_DecoderConfig;
    GUID                      m_DecoderGuid;
    HANDLE                    m_hDevice;

    FOURCC                    m_fccOutputFormat;
};
```



No restante deste tópico, o termo *decodificador* refere-se ao filtro do decodificador, que recebe vídeo compactado e gera vídeo descompactado. O termo *dispositivo decodificador* refere-se a um acelerador de vídeo de hardware implementado pelo driver de gráficos.

Aqui estão as etapas básicas que um filtro de decodificador deve executar para dar suporte a DXVA 2,0:

1.  Negocie um tipo de mídia.
2.  Localize uma configuração de decodificador DXVA.
3.  Notifique o renderizador de vídeo que o decodificador está usando a decodificação de DXVA.
4.  Forneça um alocador personalizado que aloque superfícies do Direct3D.

Essas etapas são descritas mais detalhadamente no restante deste tópico.

## <a name="migration-notes"></a>Notas de migração

Se estiver migrando do DXVA 1,0, você deve estar ciente de algumas diferenças significativas entre as duas versões:

-   O DXVA 2,0 não usa as interfaces [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) e [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) , porque o decodificador pode acessar as APIs de DXVA 2,0 diretamente por meio da interface [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .
-   Durante a negociação do tipo de mídia, o decodificador não usa um GUID de aceleração de vídeo como o subtipo. Em vez disso, o subtipo é apenas o formato de vídeo descompactado (como NV12), assim como com a decodificação de software.
-   O procedimento para configurar o acelerador foi alterado. No DXVA 1,0, o decodificador chama **Execute** com uma estrutura de **\_ ConfigPictureDecode de DXVA** para configurar o accerlator. No DXVA 2,0, o decodificador usa a interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) , conforme descrito na próxima seção.
-   O decodificador aloca os buffers descompactados. O renderizador de vídeo não os aloca.
-   Em vez de chamar [**IAMVideoAccelerator::D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) para exibir o quadro decodificado, o decodificador entrega o quadro ao renderizador chamando [**IMemInputPin:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), assim como com a decodificação de software.
-   O decodificador não é mais responsável por verificar quando os buffers de dados são seguros para atualizações. Portanto, o DXVA 2,0 não tem nenhum método equivalente a [**IAMVideoAccelerator:: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).
-   A mesclagem de subimagem é feita pelo processador de vídeo, usando as APIs do processador de vídeo DXVA 2.0. Os decodificadores que fornecem subfiguras (por exemplo, decodificadores de DVD) devem enviar dados de subimagem em um pino de saída separado.

Para operações de decodificação, o DXVA 2,0 usa as mesmas estruturas de dados que a DXVA 1,0.

O filtro EVR (processador de vídeo avançado) dá suporte a DXVA 2,0. Os filtros de processador de mixagem de vídeo (VMR-7 e VMR-9) dão suporte apenas a DXVA 1,0.

## <a name="finding-a-decoder-configuration"></a>Encontrando uma configuração de decodificador

Depois que o decodificador negociar o tipo de mídia de saída, ele deverá encontrar uma configuração compatível para o dispositivo de decodificador DXVA. Você pode executar essa etapa dentro do método [**CBaseOutputPin:: CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) do pino de saída. Essa etapa garante que o driver de gráficos dê suporte aos recursos necessários para o decodificador, antes que o decodificador confirme o uso de DXVA.

Para localizar uma configuração para o dispositivo decodificador, faça o seguinte:

1.  Consulte o PIN de entrada do renderizador para a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
2.  Chame [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter um ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . O GUID do serviço é \_ o \_ serviço de aceleração de vídeo Mr \_ .
3.  Chame [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) para obter um identificador para o dispositivo Direct3D do renderizador.
4.  Chame [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) e passe o identificador do dispositivo. Esse método retorna um ponteiro para a interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .
5.  Chame [**IDirectXVideoDecoderService:: GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids). Esse método retorna uma matriz de GUIDs de dispositivo do decodificador.
6.  Faça um loop através da matriz de GUIDs do decodificador para localizar os que o filtro de decodificador suporta. Por exemplo, para um decodificador MPEG-2, você procurará **DXVA2 \_ ModeMPEG2 \_ MOCOMP**, **DXVA2 \_ ModeMPEG2 \_ IDCT** ou **DXVA2 \_ ModeMPEG2 \_** VLD.

7.  Quando você encontrar um GUID de dispositivo de decodificador candidato, passe o GUID para o método [**IDirectXVideoDecoderService:: GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) . Esse método retorna uma matriz de formatos de destino de renderização, especificados como valores de **D3DFORMAT** .
8.  Faça um loop pelos formatos de destino de renderização e procure um que corresponda ao formato de saída. Normalmente, um dispositivo decodificador dá suporte a um único formato de destino de renderização. O filtro do decodificador deve se conectar ao renderizador usando esse subtipo. Na primeira chamada para [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), o decodificador pode destermos o formato de destino de renderização e, em seguida, retornar esse formato como um tipo de saída preferencial.

9.  Chame [**IDirectXVideoDecoderService:: GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Passe o mesmo GUID do dispositivo decodificador, junto com uma estrutura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) que descreve o formato proposto. O método retorna uma matriz de estruturas [**DXVA2 \_ ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) . Cada estrutura descreve uma configuração possível para o dispositivo decodificador.

10. Supondo que as etapas anteriores sejam bem-sucedidas, armazene o identificador do dispositivo Direct3D, o GUID do dispositivo do decodificador e a estrutura de configuração. O filtro usará essas informações para criar o dispositivo decodificador.

O código a seguir mostra como localizar uma configuração de decodificador.


```C++
HRESULT CDecoder::ConfigureDXVA2(IPin *pPin)
{
    UINT    cDecoderGuids = 0;
    BOOL    bFoundDXVA2Configuration = FALSE;
    GUID    guidDecoder = GUID_NULL;

    DXVA2_ConfigPictureDecode config;
    ZeroMemory(&config, sizeof(config));

    // Variables that follow must be cleaned up at the end.

    IMFGetService               *pGetService = NULL;
    IDirect3DDeviceManager9     *pDeviceManager = NULL;
    IDirectXVideoDecoderService *pDecoderService = NULL;

    GUID   *pDecoderGuids = NULL; // size = cDecoderGuids
    HANDLE hDevice = INVALID_HANDLE_VALUE;

    // Query the pin for IMFGetService.
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pGetService));

    // Get the Direct3D device manager.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(

            MR_VIDEO_ACCELERATION_SERVICE,
            IID_PPV_ARGS(&pDeviceManager)
            );
    }

    // Open a new device handle.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    } 

    // Get the video decoder service.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->GetVideoService(
            hDevice, IID_PPV_ARGS(&pDecoderService));
    }

    // Get the decoder GUIDs.
    if (SUCCEEDED(hr))
    {
        hr = pDecoderService->GetDecoderDeviceGuids(
            &cDecoderGuids, &pDecoderGuids);
    }

    if (SUCCEEDED(hr))
    {
        // Look for the decoder GUIDs we want.
        for (UINT iGuid = 0; iGuid < cDecoderGuids; iGuid++)
        {
            // Do we support this mode?
            if (!IsSupportedDecoderMode(pDecoderGuids[iGuid]))
            {
                continue;
            }

            // Find a configuration that we support. 
            hr = FindDecoderConfiguration(pDecoderService, pDecoderGuids[iGuid],
                &config, &bFoundDXVA2Configuration);
            if (FAILED(hr))
            {
                break;
            }

            if (bFoundDXVA2Configuration)
            {
                // Found a good configuration. Save the GUID and exit the loop.
                guidDecoder = pDecoderGuids[iGuid];
                break;
            }
        }
    }

    if (!bFoundDXVA2Configuration)
    {
        hr = E_FAIL; // Unable to find a configuration.
    }

    if (SUCCEEDED(hr))
    {
        // Store the things we will need later.

        SafeRelease(&m_pDecoderService);
        m_pDecoderService = pDecoderService;
        m_pDecoderService->AddRef();

        m_DecoderConfig = config;
        m_DecoderGuid = guidDecoder;
        m_hDevice = hDevice;
    }

    if (FAILED(hr))
    {
        if (hDevice != INVALID_HANDLE_VALUE)
        {
            pDeviceManager->CloseDeviceHandle(hDevice);
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pDeviceManager);
    SafeRelease(&pDecoderService);
    return hr;
}
HRESULT CDecoder::FindDecoderConfiguration(
    /* [in] */  IDirectXVideoDecoderService *pDecoderService,
    /* [in] */  const GUID& guidDecoder, 
    /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
    /* [out] */ BOOL *pbFoundDXVA2Configuration
    )
{
    HRESULT hr = S_OK;
    UINT cFormats = 0;
    UINT cConfigurations = 0;

    D3DFORMAT                   *pFormats = NULL;     // size = cFormats
    DXVA2_ConfigPictureDecode   *pConfig = NULL;      // size = cConfigurations

    // Find the valid render target formats for this decoder GUID.
    hr = pDecoderService->GetDecoderRenderTargets(
        guidDecoder,
        &cFormats,
        &pFormats
        );

    if (SUCCEEDED(hr))
    {
        // Look for a format that matches our output format.
        for (UINT iFormat = 0; iFormat < cFormats;  iFormat++)
        {
            if (pFormats[iFormat] != (D3DFORMAT)m_fccOutputFormat)
            {
                continue;
            }

            // Fill in the video description. Set the width, height, format, 
            // and frame rate.
            DXVA2_VideoDesc videoDesc = {0};

            FillInVideoDescription(&videoDesc); // Private helper function.
            videoDesc.Format = pFormats[iFormat];

            // Get the available configurations.
            hr = pDecoderService->GetDecoderConfigurations(
                guidDecoder,
                &videoDesc,
                NULL, // Reserved.
                &cConfigurations,
                &pConfig
                );

            if (FAILED(hr))
            {
                break;
            }

            // Find a supported configuration.
            for (UINT iConfig = 0; iConfig < cConfigurations; iConfig++)
            {
                if (IsSupportedDecoderConfig(pConfig[iConfig]))
                {
                    // This configuration is good.
                    *pbFoundDXVA2Configuration = TRUE;
                    *pSelectedConfig = pConfig[iConfig];
                    break;
                }
            }

            CoTaskMemFree(pConfig);
            break;

        } // End of formats loop.
    }

    CoTaskMemFree(pFormats);

    // Note: It is possible to return S_OK without finding a configuration.
    return hr;
}
```



Como esse exemplo é genérico, parte da lógica foi colocada em funções auxiliares que precisariam ser implementadas pelo decodificador. O código a seguir mostra as declarações para essas funções:


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a>Notificando o renderizador de vídeo

Se o decodificador encontrar uma configuração de decodificador, a próxima etapa será notificar o renderizador de vídeo de que o decodificador usará aceleração de hardware. Você pode executar essa etapa dentro do método [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) . Esta etapa deve ocorrer antes da seleção do alocador, pois afeta como o alocador é selecionado.

1.  Consulte o PIN de entrada do renderizador para a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
2.  Chame [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter um ponteiro para a interface [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) . O GUID do serviço é o **\_ \_ \_ serviço de aceleração de vídeo Mr**.
3.  Chame [**IDirectXVideoMemoryConfiguration:: GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) em um loop, incrementando a variável *dwTypeIndex* de zero. Pare quando o método retornar o valor **DXVA2 \_ surfacetype \_ DecoderRenderTarget** no parâmetro *pdwType* . Essa etapa garante que o processador de vídeo dê suporte à decodificação acelerada por hardware. Esta etapa sempre terá sucesso para o filtro EVR.
4.  Se a etapa anterior tiver sido bem-sucedida, chame [**IDirectXVideoMemoryConfiguration:: Setsurfacetype**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) com o valor DXVA2 \_ surfacetype \_ DecoderRenderTarget. Chamar **Setsurfacetype** com esse valor coloca o processador de vídeo no modo DXVA. Quando o processador de vídeo está nesse modo, o decodificador deve fornecer seu próprio alocador.

O código a seguir mostra como notificar o renderizador de vídeo.


```C++
HRESULT CDecoder::SetEVRForDXVA2(IPin *pPin)
{
    HRESULT hr = S_OK;

    IMFGetService                       *pGetService = NULL;
    IDirectXVideoMemoryConfiguration    *pVideoConfig = NULL;

    // Query the pin for IMFGetService.
    hr = pPin->QueryInterface(__uuidof(IMFGetService), (void**)&pGetService);

    // Get the IDirectXVideoMemoryConfiguration interface.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(
            MR_VIDEO_ACCELERATION_SERVICE, IID_PPV_ARGS(&pVideoConfig));
    }

    // Notify the EVR. 
    if (SUCCEEDED(hr))
    {
        DXVA2_SurfaceType surfaceType;

        for (DWORD iTypeIndex = 0; ; iTypeIndex++)
        {
            hr = pVideoConfig->GetAvailableSurfaceTypeByIndex(iTypeIndex, &surfaceType);
            
            if (FAILED(hr))
            {
                break;
            }

            if (surfaceType == DXVA2_SurfaceType_DecoderRenderTarget)
            {
                hr = pVideoConfig->SetSurfaceType(DXVA2_SurfaceType_DecoderRenderTarget);
                break;
            }
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pVideoConfig);

    return hr;
}
```



Se o decodificador encontrar uma configuração válida e notificar com êxito o processador de vídeo, o decodificador poderá usar o DXVA para decodificação. O decodificador deve implementar um alocador personalizado para seu pino de saída, conforme descrito na próxima seção.

## <a name="allocating-uncompressed-buffers"></a>Alocando buffers descompactados

No DXVA 2,0, o decodificador é responsável por alocar superfícies do Direct3D para usar como buffers de vídeo não compactados. Portanto, o decodificador deve implementar um alocador personalizado que criará as superfícies. Os exemplos de mídia fornecidos por esse alocador manterão ponteiros para as superfícies do Direct3D. O EVR recupera um ponteiro para a superfície chamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) no exemplo de mídia. O identificador de serviço é o **\_ \_ serviço de buffer do Mr**.

Para fornecer o alocador personalizado, execute as seguintes etapas:

1.  Defina uma classe para os exemplos de mídia. Essa classe pode derivar da classe [**CMediaSample**](../directshow/cmediasample.md) . Dentro dessa classe, faça o seguinte:
    -   Armazene um ponteiro para a superfície do Direct3D.
    -   Implemente a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) . No método [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , se o GUID do serviço for **o \_ \_ serviço de buffer do Mr**, consulte a superfície do Direct3D para obter a interface solicitada. Caso contrário, o **GetService** pode retornar o **\_ serviço MF E \_ sem suporte \_**.
    -   Substitua o método [**CMediaSample:: Getapontarr**](../directshow/cmediasample-getpointer.md) para retornar E \_ NOTIMPL.
2.  Defina uma classe para o alocador. O alocador pode derivar da classe [**CBaseAllocator**](../directshow/cbaseallocator.md) . Dentro dessa classe, faça o seguinte.
    -   Substitua o método [**CBaseAllocator:: Alloc**](../directshow/cbaseallocator-alloc.md) . Dentro desse método, chame [**IDirectXVideoAccelerationService:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) para criar as superfícies. (A interface [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) herda esse método de [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)
    -   Substitua o método [**CBaseAllocator:: Free**](../directshow/cbaseallocator-free.md) para liberar as superfícies.
3.  No PIN de saída do filtro, substitua o método [**CBaseOutputPin:: InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) . Dentro desse método, crie uma instância do seu alocador personalizado.
4.  No filtro, implemente o método [**CTransformFilter::D ecidebuffersize**](../directshow/ctransformfilter-decidebuffersize.md) . O parâmetro *pProperties* indica o número de superfícies que o EVR exige. Adicione a esse valor o número de superfícies exigidas pelo decodificador e chame [**IMemAllocator:: SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) no alocador.

O código a seguir mostra como implementar a classe de exemplo de mídia:


```C++
class CDecoderSample : public CMediaSample, public IMFGetService
{
    friend class CDecoderAllocator;

public:

    CDecoderSample(CDecoderAllocator *pAlloc, HRESULT *phr)
        : CMediaSample(NAME("DecoderSample"), (CBaseAllocator*)pAlloc, phr, NULL, 0),
          m_pSurface(NULL),
          m_dwSurfaceId(0)
    { 
    }

    // Note: CMediaSample does not derive from CUnknown, so we cannot use the
    //       DECLARE_IUNKNOWN macro that is used by most of the filter classes.

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        CheckPointer(ppv, E_POINTER);

        if (riid == IID_IMFGetService)
        {
            *ppv = static_cast<IMFGetService*>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            return CMediaSample::QueryInterface(riid, ppv);
        }
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return CMediaSample::AddRef();
    }

    STDMETHODIMP_(ULONG) Release()
    {
        // Return a temporary variable for thread safety.
        ULONG cRef = CMediaSample::Release();
        return cRef;
    }

    // IMFGetService::GetService
    STDMETHODIMP GetService(REFGUID guidService, REFIID riid, LPVOID *ppv)
    {
        if (guidService != MR_BUFFER_SERVICE)
        {
            return MF_E_UNSUPPORTED_SERVICE;
        }
        else if (m_pSurface == NULL)
        {
            return E_NOINTERFACE;
        }
        else
        {
            return m_pSurface->QueryInterface(riid, ppv);
        }
    }

    // Override GetPointer because this class does not manage a system memory buffer.
    // The EVR uses the MR_BUFFER_SERVICE service to get the Direct3D surface.
    STDMETHODIMP GetPointer(BYTE ** ppBuffer)
    {
        return E_NOTIMPL;
    }

private:

    // Sets the pointer to the Direct3D surface. 
    void SetSurface(DWORD surfaceId, IDirect3DSurface9 *pSurf)
    {
        SafeRelease(&m_pSurface);

        m_pSurface = pSurf;
        if (m_pSurface)
        {
            m_pSurface->AddRef();
        }

        m_dwSurfaceId = surfaceId;
    }

    IDirect3DSurface9   *m_pSurface;
    DWORD               m_dwSurfaceId;
};
```



O código a seguir mostra como implementar o método [**Alloc**](../directshow/cbaseallocator-alloc.md) no alocador.


```C++
HRESULT CDecoderAllocator::Alloc()
{
    CAutoLock lock(this);

    HRESULT hr = S_OK;

    if (m_pDXVA2Service == NULL)
    {
        return E_UNEXPECTED;
    }

    hr = CBaseAllocator::Alloc();

    // If the requirements have not changed, do not reallocate.
    if (hr == S_FALSE)
    {
        return S_OK;
    }

    if (SUCCEEDED(hr))
    {
        // Free the old resources.
        Free();

        // Allocate a new array of pointers.
        m_ppRTSurfaceArray = new (std::nothrow) IDirect3DSurface9*[m_lCount];
        if (m_ppRTSurfaceArray == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            ZeroMemory(m_ppRTSurfaceArray, sizeof(IDirect3DSurface9*) * m_lCount);
        }
    }

    // Allocate the surfaces.
    if (SUCCEEDED(hr))
    {
        hr = m_pDXVA2Service->CreateSurface(
            m_dwWidth,
            m_dwHeight,
            m_lCount - 1,
            (D3DFORMAT)m_dwFormat,
            D3DPOOL_DEFAULT,
            0,
            DXVA2_VideoDecoderRenderTarget,
            m_ppRTSurfaceArray,
            NULL
            );
    }

    if (SUCCEEDED(hr))
    {
        for (m_lAllocated = 0; m_lAllocated < m_lCount; m_lAllocated++)
        {
            CDecoderSample *pSample = new (std::nothrow) CDecoderSample(this, &hr);

            if (pSample == NULL)
            {
                hr = E_OUTOFMEMORY;
                break;
            }
            if (FAILED(hr))
            {
                break;
            }
            // Assign the Direct3D surface pointer and the index.
            pSample->SetSurface(m_lAllocated, m_ppRTSurfaceArray[m_lAllocated]);

            // Add to the sample list.
            m_lFree.Add(pSample);
        }
    }

    if (SUCCEEDED(hr))
    {
        m_bChanged = FALSE;
    }
    return hr;
}
```



Este é o código para o método [**gratuito**](../directshow/cbaseallocator-free.md) :


```C++
void CDecoderAllocator::Free()
{
    CMediaSample *pSample = NULL;

    do
    {
        pSample = m_lFree.RemoveHead();
        if (pSample)
        {
            delete pSample;
        }
    } while (pSample);

    if (m_ppRTSurfaceArray)
    {
        for (long i = 0; i < m_lAllocated; i++)
        {
            SafeRelease(&m_ppRTSurfaceArray[i]);
        }

        delete [] m_ppRTSurfaceArray;
    }
    m_lAllocated = 0;
}
```



para obter mais informações sobre como implementar os alocadores personalizados, consulte o tópico [fornecendo um alocador personalizado](../directshow/providing-a-custom-allocator.md) na documentação do SDK do DirectShow.

## <a name="decoding"></a>Decodificação

Para criar o dispositivo decodificador, chame [**IDirectXVideoDecoderService:: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). O método retorna um ponteiro para a interface [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) do dispositivo decodificador.

Em cada quadro, chame [**IDirect3DDeviceManager9:: TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) para testar o identificador do dispositivo. Se o dispositivo tiver sido alterado, o método retornará DXVA2 \_ E \_ novo dispositivo de \_ vídeo \_ . Se isso ocorrer, faça o seguinte:

1.  Feche o identificador do dispositivo chamando [**IDirect3DDeviceManager9:: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Libere os ponteiros [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) e [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .
3.  Abra um novo identificador de dispositivo.
4.  Negocie uma nova configuração de decodificador, conforme descrito na seção [encontrando uma configuração de decodificador](#finding-a-decoder-configuration).
5.  Crie um novo dispositivo de decodificador.

Supondo que o identificador do dispositivo seja válido, o processo de decodificação funciona da seguinte maneira:

1.  Chame [**IDirectXVideoDecoder:: BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).
2.  Faça o seguinte uma ou mais vezes:
    1.  Chame [**IDirectXVideoDecoder:: GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) para obter um buffer de decodificador de DXVA.
    2.  Preencha o buffer.
    3.  Chame [**IDirectXVideoDecoder:: ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).
3.  Chame [**IDirectXVideoDecoder:: execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) para executar as operações de decodificação no quadro.

O DXVA 2,0 usa as mesmas estruturas de dados que a DXVA 1,0 para operações de decodificação. Para o conjunto original de perfis de DXVA (para H. 261, H. 263 e MPEG-2), essas estruturas de dados são descritas na [especificação DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

Em cada par de [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe) / chamadas de [**execução**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) BeginFrame, você pode chamar [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) várias vezes, mas apenas uma vez para cada tipo de buffer de DXVA. Se você chamá-lo duas vezes com o mesmo tipo de buffer, os dados serão substituídos.

Depois de chamar [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), chame [**IMemInputPin:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) para entregar o quadro ao processador de vídeo, assim como com a decodificação de software. O método **Receive** é assíncrono; Depois de retornar, o decodificador pode continuar decodificando o próximo quadro. O driver de vídeo impede que qualquer comando de decodificação substitua o buffer enquanto o buffer está em uso. O decodificador não deve reutilizar uma superfície para decodificar outro quadro até que o renderizador tenha liberado o exemplo. Quando o renderizador libera o exemplo, o alocador coloca o exemplo de volta em seu pool de exemplos disponíveis. Para obter o próximo exemplo disponível, chame [**CBaseOutputPin:: GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), que por sua vez chama [**IMemAllocator:: GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer). para obter mais informações, consulte o tópico [visão geral de dados Flow em DirectShow](../directshow/overview-of-data-flow-in-directshow.md) na documentação do DirectShow.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aceleração de vídeo do DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
