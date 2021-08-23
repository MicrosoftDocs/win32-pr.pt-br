---
description: Microsoft Media Foundation usa uma combinação de constructos COM, mas não é uma API totalmente baseada em COM.
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: Media Foundation e COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb43fa29063da453a17275fca0b5c441e89f75aab8016a1abcf1702f5433fd71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974205"
---
# <a name="media-foundation-and-com"></a>Media Foundation e COM

Microsoft Media Foundation usa uma combinação de constructos COM, mas não é uma API totalmente baseada em COM. Este tópico descreve a interação entre COM e Media Foundation. Ele também define algumas práticas recomendadas para desenvolver Media Foundation componentes de plug-in. Seguir essas práticas pode ajudá-lo a evitar alguns erros de programação comuns, mas sutis.

-   [Práticas recomendadas para aplicativos](#best-practices-for-applications)
-   [Práticas recomendadas para Media Foundation componentes](#best-practices-for-media-foundation-components)
-   [Resumo](#summary)
-   [Tópicos relacionados](#related-topics)

## <a name="best-practices-for-applications"></a>Práticas recomendadas para aplicativos

No Media Foundation, o processamento assíncrono e os retornos de chamada são tratados por [filas de trabalho.](work-queues.md) As filas de trabalho sempre têm threads MTA (multithreaded apartment), portanto, um aplicativo terá uma implementação mais simples se ele for executado em um thread MTA também. Portanto, é recomendável chamar [**CoInitializeEx com**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) o **sinalizador COINIT \_ MULTITHREADED.**

Media Foundation não faz marshal de objetos STA (single-threaded apartment) para trabalhar threads de fila. Nem garante que as invariáveis STA sejam mantidas. Portanto, um aplicativo STA deve ter cuidado para não passar objetos STA ou proxies para Media Foundation APIs. Não há suporte para objetos somente STA no Media Foundation.

Se você tiver um proxy STA para um objeto MTA ou de thread livre, o objeto poderá ser marshalado para um proxy MTA usando um retorno de chamada de fila de trabalho. A [**função CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pode retornar um ponteiro bruto ou um proxy STA, dependendo do modelo de objeto definido no Registro para esse CLSID. Se um proxy STA for retornado, você não deverá passar o ponteiro para uma API Media Foundation dados.

Por exemplo, suponha que você queira passar um ponteiro **IPropertyStore** para o método [**IMFSourceResolver::BeginCreateObjectFromURL.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) Você pode chamar **PSCreateMemoryPropertyStore** para criar o ponteiro **IPropertyStore.** Se você estiver chamando de um STA, deverá efetuar marshal do ponteiro antes de passá-lo para **BeginCreateObjectFromURL.**

O código a seguir mostra como fazer marshal de um proxy STA para uma API Media Foundation dados.


```C++
class CCreateSourceMarshalCallback
    : public IMFAsyncCallback
{
public:
    CCreateSourceMarshalCallback(
        LPCWSTR szURL, 
        IMFSourceResolver* pResolver, 
        IPropertyStore* pSourceProps, 
        IMFAsyncCallback* pCompletionCallback, 
        HRESULT& hr
        )
        : m_szURL(szURL), 
          m_pResolver(pResolver), 
          m_pCompletionCallback(pCompletionCallback),
          m_pGIT(NULL),
          m_cRef(1)
    {
        hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable, NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGIT));

        if(SUCCEEDED(hr))
        {
            hr = m_pGIT->RegisterInterfaceInGlobal(
                pSourceProps, IID_IPropertyStore, &m_dwInterfaceCookie);
        }
    }
    ~CCreateSourceMarshalCallback()
    {
        SafeRelease(&m_pResolver);
        SafeRelease(&m_pCompletionCallback);
        SafeRelease(&m_pGIT);
    }


    STDMETHOD_(ULONG, AddRef)()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHOD_(ULONG, Release)()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (0 == cRef)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHOD(QueryInterface)(REFIID riid, LPVOID* ppvObject)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCreateSourceMarshalCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppvObject);

    }

    STDMETHOD(GetParameters)(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHOD(Invoke)(IMFAsyncResult* pResult)
    {
        IPropertyStore *pSourceProps = NULL;

        HRESULT hr = m_pGIT->GetInterfaceFromGlobal(
            m_dwInterfaceCookie, 
            IID_PPV_ARGS(&pSourceProps)
            );

        if(SUCCEEDED(hr))
        {
            hr = m_pResolver->BeginCreateObjectFromURL(
                m_szURL, MF_RESOLUTION_MEDIASOURCE, pSourceProps, NULL, 
                m_pCompletionCallback, NULL);
        }

        SafeRelease(&pSourceProps);
        return hr;
    }

private:
    LPCWSTR m_szURL;
    IMFSourceResolver *m_pResolver;
    IMFAsyncCallback *m_pCompletionCallback;
    IGlobalInterfaceTable *m_pGIT;
    DWORD m_dwInterfaceCookie;
    LONG m_cRef;
};
```



Para obter mais informações sobre a tabela de interface global, consulte [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Se você estiver usando Media Foundation em processo, os objetos retornados de Media Foundation e funções serão ponteiros diretos para o objeto . Para processos cruzados Media Foundation, esses objetos podem ser proxies MTA e devem ser empacotados em um thread STA, se necessário. Da mesma forma, objetos obtidos dentro de um retorno de chamada – por exemplo, uma topologia do evento [MESessionTopologyStatus](mesessiontopologystatus.md) – são ponteiros diretos quando Media Foundation é usado em processo, mas são proxies MTA quando Media Foundation é usado entre processos.

> [!Note]  
> O cenário mais comum para usar Media Foundation entre processos é com o caminho [de mídia](protected-media-path.md) protegido (PMP). No entanto, esses comentários se aplicam a qualquer situação quando Media Foundation APIs são usadas por meio de RPC.

 

Todas as implementações de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) devem ser compatíveis com MTA. Esses objetos não precisam ser objetos COM. Mas, se eles são, eles não podem ser executados no STA. A [**função IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) será invocada em um thread de workqueue do MTA e o objeto [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) fornecido será um ponteiro de objeto direto ou um proxy MTA.

## <a name="best-practices-for-media-foundation-components"></a>Práticas recomendadas para Media Foundation componentes

Há duas categorias de Media Foundation objetos que precisam se preocupar com COM. Alguns componentes, como transformar ou manipuladores de fluxo de byte, são objetos COM completos criados pelo CLSID. Esses objetos devem seguir as regras para apartments COM, tanto em processo quanto entre Media Foundation. Outros Media Foundation componentes não são objetos COM completos, mas precisam de proxies COM para reprodução entre processos. Os objetos nessa categoria incluem fontes de mídia e objeto de ativação. Esses objetos poderão ignorar problemas de apartment se eles serão usados apenas para problemas em Media Foundation.

Embora nem todos os Media Foundation objetos sejam objetos COM, todas Media Foundation interfaces derivam [**de IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Portanto, todos os Media Foundation devem implementar **IUnknown** de acordo com as especificações COM, incluindo as regras para contagem de referência e [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Todos os objetos contados por referência também devem garantir que [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) não permita que o módulo seja descarregado enquanto os objetos ainda persistem.

Media Foundation componentes não podem ser objetos STA. Muitos Media Foundation objetos não precisam ser objetos COM. Mas, se eles são, eles não podem ser executados no STA. Todos Media Foundation componentes devem ser thread-safe. Alguns Media Foundation objetos devem ser de thread livre ou neutros em apartment também. A tabela a seguir especifica os requisitos para implementações de interface personalizadas:



| Interface                                                          | Categoria            | Apartment necessário       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | Proxy entre processos | Threaded livre ou neutro |
| [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | Objeto COM          | MTA                      |
| [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | Proxy entre processos | Threaded livre ou neutro |
| [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | Objeto COM          | Threaded livre ou neutro |
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | Proxy entre processos | Threaded livre ou neutro |
| [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | Objeto COM          | MTA                      |
| [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | Objeto COM          | Threaded livre ou neutro |
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | Objeto COM          | MTA                      |



 

Pode haver requisitos adicionais dependendo da implementação. Por exemplo, se um sink de mídia implementar outra interface que permita que o aplicativo faça chamadas de função diretas para o sink, o sink precisará ser livre ou neutro, para que ele possa lidar com chamadas diretas entre processos. Qualquer objeto pode ser de thread livre; essa tabela especifica os requisitos mínimos.

A maneira recomendada de implementar objetos de thread livre ou neutros é agregando o marshaler de thread livre. Para obter mais detalhes, consulte a documentação do MSDN [**em CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler). De acordo com o requisito de não passar objetos STA ou proxies para apIs Media Foundation, os objetos de thread livre não precisam se preocupar com o marshaling de ponteiros de entrada STA em componentes de thread livre.

Os componentes que usam a fila de trabalho de função longa (FUNÇÃO LONGA DA FILA DE RETORNO DE CHAMADA **MFASYNC \_ \_ \_ \_**) devem ter mais cuidado. Os threads na função longa criam seu próprio STA. Os componentes que usam a longa linha de trabalho de função para retornos de chamada devem evitar a criação de objetos COM nesses threads e precisam ter cuidado para efetuar marshaling de proxies para o STA conforme necessário.

## <a name="summary"></a>Resumo

Os aplicativos terão um tempo mais fácil se eles interagirem com Media Foundation de um thread MTA, mas é possível com algum cuidado usar Media Foundation de um thread STA. Media Foundation não lida com componentes STA e os aplicativos devem ter cuidado para não passar objetos STA para Media Foundation APIs. Alguns objetos têm requisitos adicionais, especialmente objetos que são executados em uma situação entre processos. Seguir essas diretrizes ajudará a evitar erros COM, deadlocks e atrasos inesperados no processamento de mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Media Foundation Platform APIs](media-foundation-platform-apis.md)
</dt> <dt>

[Arquitetura Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 
