---
description: Desbloqueando o SDK do Windows Media Format
ms.assetid: 7ede8bda-3b26-452d-8ce9-cd2410ffd9f4
title: Desbloqueando o SDK do Windows Media Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9807794dc7e42c563f2f7d45dcb0b1b684aad1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105758824"
---
# <a name="unlocking-the-windows-media-format-sdk"></a>Desbloqueando o SDK do Windows Media Format

Para acessar a versão 7 ou 7,1 do SDK do Windows Media Format, um aplicativo deve fornecer um certificado de software, também chamado de chave, em tempo de execução. Essa chave está contida em uma biblioteca estática chamada wmstub. lib para a qual o aplicativo é vinculado no momento da compilação. Uma chave individualizada só é necessária para criar ou ler arquivos protegidos por DRM. Arquivos não DRM podem ser criados usando a biblioteca estática fornecida com o Windows Media Format SDK. Para obter detalhes sobre como obter a chave DRM, consulte o SDK do Windows Media Format. Um aplicativo do DirectShow fornece seu certificado para o gravador ASF do WM quando ele é adicionado ao grafo de filtro. O aplicativo deve ser registrado como um provedor de chaves usando as interfaces **IServiceProvider** e **IObjectWithSite** do com. Usando essa técnica, o aplicativo implementa uma classe de provedor de chave derivada de **IServiceProvider**. Essa classe implementa os três métodos COM padrão —**AddRef**, **QueryInterface** e **Release**— juntamente com um método adicional, **QueryService**, que é chamado pelo Gerenciador do grafo de filtro. **QueryService** chama o método [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) do Windows Media Format SDK e retorna ao Gerenciador do grafo de filtro um ponteiro para o certificado que foi criado. Se o certificado for válido, o Gerenciador de gráfico de filtro permitirá que o processo de criação de grafo prossiga.

> [!Note]  
> Para criar um aplicativo, inclua Wmsdkidl. h para o protótipo para [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))e vincule à biblioteca Wmstub. lib.

 

O exemplo de código a seguir ilustra as etapas básicas neste processo:


```C++
// Declare and implement a key provider class derived from IServiceProvider.

class CKeyProvider : public IServiceProvider {
public:
    // IUnknown interface
    STDMETHODIMP QueryInterface(REFIID riid, void ** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    CKeyProvider();

    // IServiceProvider
    STDMETHODIMP QueryService(REFIID siid, REFIID riid, void **ppv);
    
private:
    ULONG m_cRef;
};

CKeyProvider::CKeyProvider() : m_cRef(0)
{
}

// IUnknown methods
ULONG CKeyProvider::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

ULONG CKeyProvider::Release()
{
    ASSERT(m_cRef > 0);

    ULONG lCount = InterlockedDecrement(&m_cRef);
    if (m_cRef == 0) 
    {
        delete this;
        return (ULONG)0;
    }
    return (ULONG)lCount;
}

// We only support IUnknown and IServiceProvider.
HRESULT CKeyProvider::QueryInterface(REFIID riid, void ** ppv)
{
    if (!ppv) return E_POINTER;

    if (riid == IID_IUnknown) 
    {
        *ppv = (void *) static_cast<IUnknown *>(this);
        AddRef();
        return S_OK;
    }
    if (riid == IID_IServiceProvider) 
    {
        *ppv = (void *) static_cast<IServiceProvider *>(this);
        AddRef();
        return S_OK;
    }

    return E_NOINTERFACE;
}

STDMETHODIMP CKeyProvider::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (!ppv) return E_POINTER;

    if (siid == __uuidof(IWMReader) && riid == IID_IUnknown) 
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

////////////////////////////////////////////////////////////////////
//
// These examples illustrate the sequence of method calls
// in your application. Error checking is omitted for brevity.
//
///////////////////////////////////////////////////////////////////

// Create the filter graph manager, but don't add any filters.
IGraphBuilder *pGraph;
hr = CreateFilterGraph(&pGraph);

...

// Instantiate the key provider class, and AddRef it
// so that COM doesn't try to free our static object.

CKeyProvider prov;
prov.AddRef();  // Don't let COM try to free our static object.

// Give the graph an IObjectWithSite pointer for callbacks and QueryService.
IObjectWithSite* pObjectWithSite = NULL;

hr = pGraph->QueryInterface(IID_IObjectWithSite, (void**)&pObjectWithSite);
if (SUCCEEDED(hr))
{
    // Use the IObjectWithSite pointer to specify our key provider object.
    // The filter graph manager will use this pointer to call
    // QueryService to do the unlocking.
    // If the unlocking succeeds, then we can build our graph.

    pObjectWithSite->SetSite((IUnknown *) (IServiceProvider *) &prov);
    pObjectWithSite->Release();
}

// Now build the graph.
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
