---
description: Como configurar o localizador de proxy
ms.assetid: ddc28add-ebf5-4a68-bdf4-dc5f33ab74da
title: Como configurar o localizador de proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51dcade0909159856c4286d9c2cd5d4851d10b6d2c5e56054545bdac312e21b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061536"
---
# <a name="how-to-configure-the-proxy-locator"></a>Como configurar o localizador de proxy

O aplicativo pode alterar a configuração padrão do localizador de proxy definindo a propriedade [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) como o objeto de fábrica do localizador de proxy implementado pelo aplicativo. Quando o aplicativo chama métodos de resolvedor de origem para criar a fonte de rede, Media Foundation chama a fábrica do localizador de proxy. Esse objeto cria o localizador de proxy com configuração personalizada.

## <a name="to-change-the-default-configuration-setting-of-the-proxy-locator"></a>Para alterar a definição de configuração padrão do localizador de proxy

1.  Implemente a interface [**IMFNetProxyLocatorFactory.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory)
2.  No método [**IMFNetProxyLocatorFactory::CreateProxyLocator,**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) faça o seguinte:
    1.  Crie um armazenamento de propriedades.
    2.  Definir as definições de configuração para o localizador de proxy. Para obter informações sobre essas configurações, consulte [Configuração do localizador de proxy Configurações](proxy-locator-configuration-settings.md).
    3.  Chame a [**função MFCreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) Passe o armazenamento de propriedades e o protocolo. O protocolo é especificado no parâmetro *pszProtocol* de [**CreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator)
3.  Crie uma instância da classe de fábrica do localizador de proxy e receba um ponteiro para sua interface [**IMFNetProxyLocatorFactory.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory)
4.  Crie outro armazenamento de propriedades e de definido o valor da propriedade [**\_ PROXYLOCATORFACTORY MFNETSOURCE**](mfnetsource-proxylocatorfactory-property.md) igual ao ponteiro [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) da etapa 3.
5.  Ao criar a fonte de rede, passe o armazenamento de propriedades no parâmetro *pProps* dos métodos do resolvedor de origem, como [**IMFSourceResolver::BeginCreateObjectFromURL.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)

## <a name="example"></a>Exemplo

O exemplo de código a seguir implementa a interface [**IMFNetProxyLocatorFactory.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) O [**método IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) cria uma instância do localizador de proxy padrão e a configura para operar no modo de detecção automática.


```C++
class CProxyLocatorFactory : public IMFNetProxyLocatorFactory 
{
    LONG m_cRef;

public:

    CProxyLocatorFactory() : m_cRef(1)
    {
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CProxyLocatorFactory, IMFNetProxyLocatorFactory),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHODIMP CreateProxyLocator(
        LPCWSTR pszProtocol, 
        IMFNetProxyLocator **ppProxyLocator
        )
    {
        *ppProxyLocator = NULL;

        //Create the property store object
        IPropertyStore *pProp = NULL;

        HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pProp));

        if(SUCCEEDED(hr))
        {
            // Property key for proxy settings.
            PROPERTYKEY key;
            key.fmtid = MFNETSOURCE_PROXYSETTINGS;        
            key.pid = 0;

            // Proxy settings
            PROPVARIANT var;
            var.vt = VT_I4;
            var.lVal = MFNET_PROXYSETTING_AUTO;

            hr = pProp->SetValue(key, var);
        }

        //Create the default proxy locator.

        if(SUCCEEDED(hr))
        {
            hr = MFCreateProxyLocator(pszProtocol, pProp, ppProxyLocator);
        }

        SafeRelease(&pProp);
        return hr;
    }
};
```



O exemplo a seguir mostra como passar o ponteiro [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) para a fonte de rede.


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set a proxy locator on the network source.

HRESULT CreateMediaSourceWithProxyLocator(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    IMFNetProxyLocatorFactory *pFactory = new (std::nothrow) CProxyLocatorFactory();

    if (pFactory == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_PROXYLOCATORFACTORY;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        var.punkVal = pFactory;

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a proxy para fontes de rede](proxy-support-for-network-sources.md)
</dt> </dl>

 

 



