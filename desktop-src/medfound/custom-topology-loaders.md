---
description: Carregadores de topologia personalizados
ms.assetid: 3982b07e-3179-45c1-9f17-f2114363f53d
title: Carregadores de topologia personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a8f9e24b207d43620e7b2d09080d244b0a9e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768231"
---
# <a name="custom-topology-loaders"></a>Carregadores de topologia personalizados

Quando um aplicativo enfileira uma topologia parcial na sessão de mídia, a sessão de mídia usa um carregador de topologia para resolver a topologia. Por padrão, a sessão de mídia usa a implementação de Media Foundation padrão do carregador de topologia, mas você também pode fornecer uma implementação personalizada. Isso lhe dá mais controle sobre a topologia final. Um carregador de topologia personalizado deve implementar a interface [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .

Para definir um carregador de topologia personalizado na sessão de mídia, faça o seguinte:

1.  Crie um repositório de atributos vazio chamando [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Defina o [**atributo \_ \_ TOPOLOADER da sessão MF**](mf-session-topoloader-attribute.md) no repositório de atributos. O valor do atributo é o CLSID do carregador personalizado.
3.  Chame [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para criar a sessão de mídia para conteúdo desprotegido ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) para criar a sessão de mídia dentro do caminho de mídia protegido (PMP).

> [!Note]  
> Para usar um carregador de topologia personalizado dentro do PMP, o carregador de topologia deve ser um componente confiável. Para obter mais informações, consulte [proteção de caminho de mídia](protected-media-path.md).

 

O código a seguir mostra como definir um carregador de topologia personalizado na sessão de mídia.


```C++
HRESULT CreateSession_CustomTopoLoader(REFCLSID clsid, IMFMediaSession **ppSession)
{
    *ppSession = NULL;

    IMFMediaSession *pSession = NULL;
    IMFAttributes *pConfig = NULL;

    // Create an attribute store to configure the media session.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Set the CLSID of the custom topology loader.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(MF_SESSION_TOPOLOADER, clsid);
    }

    // Create the media session.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaSession(pConfig, &pSession);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSession = pSession;
        (*ppSession)->AddRef();
    }

    SafeRelease(&pSession);
    SafeRelease(&pConfig);

    return hr;
}
```



Não é necessário implementar todo o algoritmo de carregamento de topologia em seu carregador de topologia. Como alternativa, você pode encapsular o carregador de topologia de Media Foundation padrão. Em sua implementação do método [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) , modifique a topologia conforme necessário e passe a topologia modificada para o carregador de topologia padrão. Em seguida, o carregador de topologia padrão conclui a topologia. Você também pode modificar a topologia concluída antes de passá-la de volta para a sessão de mídia.

O código a seguir mostra o contorno geral dessa abordagem. Ele não mostra nenhum detalhe do método [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) , pois isso dependerá dos requisitos específicos do seu aplicativo.


```C++
class CTopoLoader : public IMFTopoLoader
{
public:

    static HRESULT CreateInstance(REFIID iid, void **ppv)
    {
        HRESULT hr = S_OK;

        CTopoLoader *pTopoLoader = new (std::nothrow) CTopoLoader(&hr);
        
        if (pTopoLoader == NULL)
        {
            return E_OUTOFMEMORY;
        }

        if (SUCCEEDED(hr))
        {
            hr = pTopoLoader->QueryInterface(iid, ppv);
        }

        SafeRelease(&pTopoLoader);
        return hr;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CTopoLoader, IMFTopoLoader),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        long cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMTopoLoader methods.
    STDMETHODIMP Load(
        IMFTopology *pInput, 
        IMFTopology **ppOutput, 
        IMFTopology *pCurrent
        )
    {
        HRESULT hr = S_OK;

        // TODO: Add custom topology-building code here.
        //       Modify pInput as needed.

        if (SUCCEEDED(hr))
        {
            hr = m_pTopoLoader->Load(pInput, ppOutput, pCurrent);
        }

        // TODO: Add custom topology-building code here.
        //       Modify ppOutput as needed.

        return hr;
    }

private:
    CTopoLoader(HRESULT *phr) : m_cRef(1), m_pTopoLoader(NULL)
    {
        *phr = MFCreateTopoLoader(&m_pTopoLoader);
    }

    virtual ~CTopoLoader()
    {
        SafeRelease(&m_pTopoLoader);
    }

private:
    long            m_cRef;          // Reference count.
    IMFTopoLoader   *m_pTopoLoader;  // Standard topoloader.
};
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**MFCreateTopoLoader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[Criação de topologia avançada](advanced-topology-building.md)
</dt> </dl>

 

 



