---
description: Microsoft Media Foundation usa uma combinação de construções COM, mas não é uma API totalmente baseada em COM.
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: Media Foundation e COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb7d05bac6a3f4deef2c004c6980ef1351c3823
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105769646"
---
# <a name="media-foundation-and-com"></a>Media Foundation e COM

Microsoft Media Foundation usa uma combinação de construções COM, mas não é uma API totalmente baseada em COM. Este tópico descreve a interação entre COM e Media Foundation. Ele também define algumas práticas recomendadas para o desenvolvimento de Media Foundation componentes de plug-in. Seguir essas práticas pode ajudá-lo a evitar alguns erros de programação comuns, mas sutis.

-   [Práticas recomendadas para aplicativos](#best-practices-for-applications)
-   [Práticas recomendadas para componentes de Media Foundation](#best-practices-for-media-foundation-components)
-   [Resumo](#summary)
-   [Tópicos relacionados](#related-topics)

## <a name="best-practices-for-applications"></a>Práticas recomendadas para aplicativos

No Media Foundation, o processamento assíncrono e os retornos de chamada são tratados por [filas de trabalho](work-queues.md). As filas de trabalho sempre têm threads de MTA (multithreaded apartment), de modo que um aplicativo terá uma implementação mais simples se for executado em um thread MTA também. Portanto, é recomendável chamar [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) com o sinalizador de **\_ vários threads de coinit** .

Media Foundation não empacota objetos STA (single-threaded apartment) para threads de fila de trabalho. Nem garante que as invariáveis de STA sejam mantidas. Portanto, um aplicativo STA deve ter cuidado para não passar objetos STA ou proxies para Media Foundation APIs. Os objetos que são somente STA não têm suporte no Media Foundation.

Se você tiver um proxy STA para um MTA ou um objeto de thread livre, o objeto poderá ser empacotado para um proxy MTA usando um retorno de chamada de fila de trabalho. A função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pode retornar um ponteiro bruto ou um proxy STA, dependendo do modelo de objeto definido no registro para esse CLSID. Se um proxy STA for retornado, você não deverá passar o ponteiro para uma API Media Foundation.

Por exemplo, suponha que você queira passar um ponteiro **IPropertyStore** para o método [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) . Você pode chamar **PSCreateMemoryPropertyStore** para criar o ponteiro **IPropertyStore** . Se você estiver chamando de um STA, deverá realizar marshaling do ponteiro antes de passá-lo para **BeginCreateObjectFromURL**.

O código a seguir mostra como realizar marshaling de um proxy STA para uma API Media Foundation.


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

Se você estiver usando Media Foundation em processo, os objetos retornados de Media Foundation métodos e funções serão ponteiros diretos para o objeto. Para Media Foundation de processo cruzado, esses objetos podem ser proxies MTA e devem ser empacotados em um thread STA, se necessário. Da mesma forma, os objetos obtidos dentro de um retorno de chamada — por exemplo, uma topologia do evento [MESessionTopologyStatus](mesessiontopologystatus.md) — são ponteiros diretos quando Media Foundation é usado em processo, mas são proxies MTA quando Media Foundation é usado em processo cruzado.

> [!Note]  
> O cenário mais comum para usar Media Foundation processo cruzado é com o [caminho de mídia protegido](protected-media-path.md) (PMP). No entanto, esses comentários se aplicam a qualquer situação quando Media Foundation APIs são usadas por meio de RPC.

 

Todas as implementações de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) devem ser compatíveis com o MTA. Esses objetos não precisam ser objetos COM. Mas, se estiverem, eles não poderão ser executados no STA. A função [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) será invocada em um thread de fila de pesquisa MTA e o objeto [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) fornecido será um ponteiro de objeto direto ou um proxy MTA.

## <a name="best-practices-for-media-foundation-components"></a>Práticas recomendadas para componentes de Media Foundation

Há duas categorias de objetos Media Foundation que precisam se preocupar COM o COM. Alguns componentes, como transformações ou manipuladores de fluxo de bytes, são objetos COM completos criados pelo CLSID. Esses objetos devem seguir as regras para Apartments COM, para Media Foundation em processo e em processo cruzado. Outros componentes de Media Foundation não são objetos COM completos, mas precisam de proxies COM para reprodução entre processos. Os objetos nessa categoria incluem fontes de mídia e objeto de ativação. Esses objetos poderão ignorar problemas de apartamento se eles forem usados apenas para Media Foundation em processo.

Embora nem todos os objetos de Media Foundation sejam objetos COM, todas as interfaces de Media Foundation derivam de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Portanto, todos os objetos de Media Foundation devem implementar **IUnknown** de acordo com as especificações com, incluindo as regras para contagem de referência e [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Todos os objetos de referência contados também devem garantir que o [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) não permitirá que o módulo seja descarregado enquanto os objetos ainda persistirem.

Os componentes de Media Foundation não podem ser objetos STA. Muitos objetos de Media Foundation não precisam ser objetos COM. Mas, se estiverem, eles não poderão ser executados no STA. Todos os componentes de Media Foundation devem ser thread-safe. Alguns objetos de Media Foundation devem ser de thread livre ou de apartamento neutro também. A tabela a seguir especifica os requisitos para implementações de interface personalizada:



| Interface                                                          | Category            | Apartamento necessário       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | Proxy de processo cruzado | Livre de threads ou neutros |
| [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | Objeto COM          | MTA                      |
| [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | Proxy de processo cruzado | Livre de threads ou neutros |
| [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | Objeto COM          | Livre de threads ou neutros |
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | Proxy de processo cruzado | Livre de threads ou neutros |
| [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | Objeto COM          | MTA                      |
| [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | Objeto COM          | Livre de threads ou neutros |
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | Objeto COM          | MTA                      |



 

Pode haver requisitos adicionais, dependendo da implementação. Por exemplo, se um coletor de mídia implementar outra interface que permita que o aplicativo faça chamadas de função diretas para o coletor, o coletor precisaria ser de thread livre ou neutro, para que pudesse lidar com chamadas diretas de processos cruzados. Qualquer objeto pode ser de segmento livre; Esta tabela especifica os requisitos mínimos.

A maneira recomendada para implementar objetos livres de threads ou neutros é agregar o marshaler de thread livre. Para obter mais detalhes, consulte a documentação do MSDN em [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler). De acordo com o requisito de não passar objetos STA ou proxies para Media Foundation APIs, os objetos de thread livre não precisam se preocupar com o marshaling de ponteiros de entrada STA em componentes de thread livre.

Os componentes que usam a fila de trabalho de função longa (**\_ \_ \_ \_ função longa da fila de retorno de chamada MFASYNC**) devem exercer mais cuidado. Os threads na fila de funções de longa duração criam seu próprio STA. Os componentes que usam a fila de funções de longa duração para retornos de chamada devem evitar a criação de objetos COM nesses threads e precisam ter cuidado para realizar marshaling de proxies para o STA, conforme necessário.

## <a name="summary"></a>Resumo

Os aplicativos terão um tempo mais fácil se interagirem com Media Foundation de um thread MTA, mas é possível ter cuidado ao usar Media Foundation de um thread STA. Media Foundation não trata componentes STA, e os aplicativos devem ter cuidado para não passar objetos STA para Media Foundation APIs. Alguns objetos têm requisitos adicionais, especialmente objetos executados em uma situação de processo cruzado. Seguir essas diretrizes ajudará a evitar erros COM, deadlocks e atrasos inesperados no processamento de mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs da plataforma Media Foundation](media-foundation-platform-apis.md)
</dt> <dt>

[Arquitetura Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 
