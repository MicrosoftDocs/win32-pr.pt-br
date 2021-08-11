---
description: Este tópico descreve como implementar um método assíncrono no Microsoft Media Foundation.
ms.assetid: cd94280d-7267-4d35-8333-aa4a5bd81b73
title: Escrevendo um método assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2efc9b38212f729dc840dde1ad1976a1b523103312710a0f316369637f3b66d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236997"
---
# <a name="writing-an-asynchronous-method"></a>Escrevendo um método assíncrono

Este tópico descreve como implementar um método assíncrono no Microsoft Media Foundation.

Os métodos assíncronos são onipresentes no pipeline de Media Foundation. Os métodos assíncronos facilitam a distribuição do trabalho entre vários threads. É particularmente importante executar e/s de forma assíncrona, para que a leitura de um arquivo ou rede não bloqueie o restante do pipeline.

Se você estiver escrevendo um coletor de mídia ou origem de mídia, é crucial tratar as operações assíncronas corretamente, pois o desempenho do componente tem um impacto em todo o pipeline.

> [!Note]  
> As transformações de Media Foundation (MFTs) usam métodos síncronos por padrão.

 

### <a name="work-queues-for-asynchronous-operations"></a>Filas de trabalho para operações assíncronas

Em Media Foundation, há uma relação de fechamento entre os [métodos de retorno de chamada assíncrono](asynchronous-callback-methods.md) e as [filas de trabalho](work-queues.md). Uma fila de trabalho é uma abstração para mover o trabalho do thread do chamador para um thread de trabalho. Para executar o trabalho em uma fila de trabalho, faça o seguinte:

1.  Implemente a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
2.  Chame [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para criar um objeto de *resultado* . O objeto result expõe o [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult). O objeto de resultado contém três ponteiros:

    -   Um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) do chamador.
    -   Um ponteiro opcional para um objeto de estado. Se especificado, o objeto de Estado deve implementar **IUnknown**.
    -   Um ponteiro opcional para um objeto particular. Se especificado, esse objeto também deve implementar **IUnknown**.

    Os dois últimos ponteiros podem ser **nulos**. Caso contrário, use-os para manter informações sobre a operação assíncrona.

3.  Chame [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) para enfileirar para o item de trabalho.
4.  O thread de fila de trabalho chama o método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .
5.  Faça o trabalho dentro do seu método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) . O parâmetro *pAsyncResult* desse método é o ponteiro [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) da etapa 2. Use este ponteiro para obter o objeto de estado e o objeto particular:
    -   Para obter o objeto de estado, chame [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).
    -   Para obter o objeto particular, chame [**IMFAsyncResult:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).

Como alternativa, você pode combinar as etapas 2 e 3 chamando a função [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) . Internamente, essa função chama [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para criar o objeto de resultado.

O diagrama a seguir mostra as relações entre o chamador, o objeto de resultado, o objeto de estado e o objeto particular.

![diagrama mostrando um objeto de resultado assíncrono](images/workqueues01.png)

O diagrama de sequência a seguir mostra como um objeto enfileira um item de trabalho. Quando o thread de fila de trabalho chama [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), o objeto executa a operação assíncrona nesse thread.

![diagrama mostrando como um objeto enfileira um item de trabalho](images/workqueues02.png)

É importante lembrar que [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) é chamado de um thread que pertence à fila de trabalho. Sua implementação de **Invoke** deve ser thread-safe. Além disso, se você usar a fila de trabalho da plataforma (**\_ padrão de fila de retorno de chamada \_ \_ MFASYNC**), é essencial que nunca bloqueie o thread, pois isso pode bloquear todo o pipeline de Media Foundation do processamento de dados. Se você precisar executar uma operação que irá bloquear ou levar muito tempo para ser concluída, use uma fila de trabalho particular. Para criar uma fila de trabalho particular, chame [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue). Qualquer componente de pipeline que executa operações de e/s deve evitar o bloqueio de chamadas de e/s pelo mesmo motivo. A interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) fornece uma abstração útil para e/s de arquivo assíncrono.

### <a name="implementing-the-beginend-pattern"></a>Implementando o Begin. ../end... Padrão

Conforme descrito em [chamando métodos assíncronos](calling-asynchronous-methods.md), os métodos assíncronos no Media Foundation geralmente usam o botão **Iniciar...** / **Terminar....** padrão. Nesse padrão, uma operação assíncrona usa dois métodos com assinaturas semelhantes às seguintes:

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

Para tornar o método realmente assíncrono, a implementação de **BeginX** deve executar o trabalho real em outro thread. É aí que as filas de trabalho entram em cena. Nas etapas a seguir, o *chamador* é o código que chama **BeginX** e **EndX**. Isso pode ser um aplicativo ou o pipeline de Media Foundation. O *componente* é o código que implementa **BeginX** e **EndX**.

1.  O chamador chama **begin...**, passando um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) do chamador.
2.  O componente cria um novo objeto de resultado assíncrono. Esse objeto armazena a interface de retorno de chamada do chamador e o objeto de estado. Normalmente, ele também armazena qualquer informação de estado particular que o componente precisa para concluir a operação. O objeto de resultado desta etapa é rotulado "resultado 1" no diagrama seguinte.
3.  O componente cria um segundo objeto de resultado. Esse objeto de resultado armazena dois ponteiros: o primeiro objeto de resultado e a interface de retorno de chamada do receptor. Esse objeto de resultado é rotulado "resultado 2" no próximo diagrama.
4.  O componente chama [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) para enfileirar um novo item de trabalho.
5.  No método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , o componente faz o trabalho assíncrono.
6.  O componente chama [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) para invocar o método de retorno de chamada do chamador.
7.  O chamador chama o método **EndX** .

![diagrama mostrando como um objeto implementa o padrão inicial/final](images/workqueues03.png)

## <a name="asynchronous-method-example"></a>Exemplo do método assíncrono

Para ilustrar essa discussão, usaremos um exemplo de forçado. Considere um método assíncrono para computar uma raiz quadrada:


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



O parâmetro *x* de `BeginSquareRoot` é o valor cuja raiz quadrada será calculada. A raiz quadrada é retornada no parâmetro *PVal* de `EndSquareRoot` .

Aqui está a declaração de uma classe que implementa esses dois métodos:


```C++
class SqrRoot : public IMFAsyncCallback
{
    LONG    m_cRef;
    double  m_sqrt;

    HRESULT DoCalculateSquareRoot(AsyncOp *pOp);

public:

    SqrRoot() : m_cRef(1)
    {

    }

    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(SqrRoot, IMFAsyncCallback),
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

    // IMFAsyncCallback methods.

    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;  
    }
    // Invoke is where the work is performed.
    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



A `SqrRoot` classe implementa [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) para que ela possa colocar a operação raiz quadrada em uma fila de trabalho. O `DoCalculateSquareRoot` método é o método da classe privada que calcula a raiz quadrada. Esse método será chamado a partir do thread da fila de trabalho.

Primeiro, precisamos de uma maneira de armazenar o valor de *x*, para que ele possa ser recuperado quando o thread da fila de trabalho chamar `SqrRoot::Invoke` . Aqui está uma classe simples que armazena as informações:


```C++
class AsyncOp : public IUnknown
{
    LONG    m_cRef;

public:

    double  m_value;

    AsyncOp(double val) : m_cRef(1), m_value(val) { }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(AsyncOp, IUnknown),
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
};
```



Essa classe implementa **IUnknown** , de forma que possa ser armazenada em um objeto de resultado.

O código a seguir implementa o `BeginSquareRoot` método:


```C++
HRESULT SqrRoot::BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState)
{
    AsyncOp *pOp = new (std::nothrow) AsyncOp(x);
    if (pOp == NULL)
    {
        return E_OUTOFMEMORY;
    }

    IMFAsyncResult *pResult = NULL;

    // Create the inner result object. This object contains pointers to:
    // 
    //   1. The caller's callback interface and state object. 
    //   2. The AsyncOp object, which contains the operation data.
    //

    HRESULT hr = MFCreateAsyncResult(pOp, pCB, pState, &pResult);

    if (SUCCEEDED(hr))
    {
        // Queue a work item. The work item contains pointers to:
        // 
        // 1. The callback interface of the SqrRoot object.
        // 2. The inner result object.

        hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_STANDARD, this, pResult);

        pResult->Release();
    }

    return hr;
}
```



O código faz o seguinte:

1.  Cria uma nova instância da `AsyncOp` classe para armazenar o valor de *x*.
2.  Chama [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para criar um objeto de resultado. Esse objeto contém vários ponteiros:
    -   Um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) do chamador.
    -   Um ponteiro para o objeto de estado do chamador (*pState*).
    -   Um ponteiro para o objeto `AsyncOp`.
3.  Chama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) para enfileirar um novo item de trabalho. Essa chamada Cria implicitamente um objeto de resultado externo, que contém os seguintes ponteiros:
    -   Um ponteiro para a `SqrRoot` interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) do objeto.
    -   Um ponteiro para o objeto de resultado interno da etapa 2.

O código a seguir implementa o `SqrRoot::Invoke` método:


```C++
// Invoke is called by the work queue. This is where the object performs the
// asynchronous operation.

STDMETHODIMP SqrRoot::Invoke(IMFAsyncResult* pResult)
{
    HRESULT hr = S_OK;

    IUnknown *pState = NULL;
    IUnknown *pUnk = NULL;
    IMFAsyncResult *pCallerResult = NULL;

    AsyncOp *pOp = NULL; 

    // Get the asynchronous result object for the application callback. 

    hr = pResult->GetState(&pState);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pState->QueryInterface(IID_PPV_ARGS(&pCallerResult));
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the object that holds the state information for the asynchronous method.
    hr = pCallerResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    pOp = static_cast<AsyncOp*>(pUnk);

    // Do the work.

    hr = DoCalculateSquareRoot(pOp);

done:
    // Signal the application.
    if (pCallerResult)
    {
        pCallerResult->SetStatus(hr);
        MFInvokeCallback(pCallerResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pUnk);
    SafeRelease(&pCallerResult);
    return S_OK;
}
```



Esse método obtém o objeto de resultado interno e o `AsyncOp` objeto. Em seguida, ele passa o `AsyncOp` objeto para `DoCalculateSquareRoot` . Por fim, ele chama [**IMFAsyncResult:: SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) para definir o código de status e [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) para invocar o método de retorno de chamada do chamador.

O `DoCalculateSquareRoot` método faz exatamente o que você esperaria:


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



Quando o método de retorno de chamada do chamador é invocado, é responsabilidade do chamador chamar o método **end...** — nesse caso, `EndSquareRoot` . O `EndSquareRoot` é como o chamador recupera o resultado da operação assíncrona, que neste exemplo é a raiz quadrada computada. Essas informações são armazenadas no objeto de resultado:


```C++
HRESULT SqrRoot::EndSquareRoot(IMFAsyncResult *pResult, double *pVal)
{
    *pVal = 0;

    IUnknown *pUnk = NULL;

    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    AsyncOp *pOp = static_cast<AsyncOp*>(pUnk);

    // Get the result.
    *pVal = pOp->m_value;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="operation-queues"></a>Filas de operação

Até agora, foi tacitly pressupor que uma operação assíncrona poderia ser feita a qualquer momento, independentemente do estado atual do objeto. Por exemplo, considere o que acontece se um aplicativo chama `BeginSquareRoot` enquanto uma chamada anterior para o mesmo método ainda está pendente. A `SqrRoot` classe pode enfileirar o novo item de trabalho antes que o item de trabalho anterior seja concluído. No entanto, as filas de trabalho não têm garantia de serializar itens de trabalho. Lembre-se de que uma fila de trabalho pode usar mais de um thread para distribuir itens de trabalho. Em um ambiente multi-threaded, um item de trabalho pode ser invocado antes da conclusão da tarefa anterior. Os itens de trabalho podem até mesmo ser invocados fora de ordem, se ocorrer uma alternância de contexto logo antes do retorno de chamada.

Por esse motivo, é responsabilidade do objeto serializar operações em si mesmo, se necessário. Em outras palavras, se o objeto exigir que *a operação a seja concluída* antes que a operação *B* possa ser iniciada, o objeto não deverá enfileirar um item de trabalho para *B* até que *a operação A* seja concluída. Um objeto pode atender a esse requisito tendo sua própria fila de operações pendentes. Quando um método assíncrono é chamado no objeto, o objeto coloca a solicitação em sua própria fila. Como cada operação assíncrona é concluída, o objeto recebe a próxima solicitação da fila. O [exemplo MPEG1Source](mpeg1source-sample.md) mostra um exemplo de como implementar essa fila.

Um único método pode envolver várias operações assíncronas, especialmente quando chamadas de e/s são usadas. Ao implementar métodos assíncronos, pense atentamente sobre os requisitos de serialização. Por exemplo, é válido para o objeto iniciar uma nova operação enquanto uma solicitação de e/s anterior ainda está pendente? Se a nova operação alterar o estado interno do objeto, o que acontece quando uma solicitação de e/s anterior é concluída e retorna dados que agora podem estar obsoletos? Um bom diagrama de estado pode ajudar a identificar as transições de estado válidas.

## <a name="cross-thread-and-cross-process-considerations"></a>Considerações entre threads e processos cruzados

As filas de trabalho não usam o marshaling COM para empacotar ponteiros de interface entre limites de thread. Portanto, mesmo que um objeto seja registrado como Apartment-Threaded ou o thread do aplicativo tenha inserido um STA (single-threaded apartment), os retornos de chamada [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) serão invocados de um thread diferente. Em qualquer caso, todos os componentes de pipeline Media Foundation devem usar o modelo de Threading "both".

Algumas interfaces no Media Foundation definem versões remotas de alguns métodos assíncronos. Quando um desses métodos é chamado entre limites de processo, a DLL Media Foundation proxy/stub chama a versão remota do método, que executa o marshaling personalizado dos parâmetros do método. No processo remoto, o stub traduz a chamada de volta para o método local no objeto. Esse processo é transparente para o aplicativo e o objeto remoto. Esses métodos de marshaling personalizados são fornecidos principalmente para objetos que são carregados no caminho de mídia protegido (PMP). Para obter mais informações sobre o PMP, consulte [proteção de caminho de mídia](protected-media-path.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Métodos de retorno de chamada assíncrono](asynchronous-callback-methods.md)
</dt> <dt>

[Filas de trabalho](work-queues.md)
</dt> </dl>

 

 



