---
description: Este tópico descreve como implementar um método assíncrono no Microsoft Media Foundation.
ms.assetid: cd94280d-7267-4d35-8333-aa4a5bd81b73
title: Escrevendo um método assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d8360d0c15fe25661b8cd0f0f5adc9768db8ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297296"
---
# <a name="writing-an-asynchronous-method"></a><span data-ttu-id="84e80-103">Escrevendo um método assíncrono</span><span class="sxs-lookup"><span data-stu-id="84e80-103">Writing an Asynchronous Method</span></span>

<span data-ttu-id="84e80-104">Este tópico descreve como implementar um método assíncrono no Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="84e80-104">This topic describes how to implement an asynchronous method in Microsoft Media Foundation.</span></span>

<span data-ttu-id="84e80-105">Os métodos assíncronos são onipresentes no pipeline de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="84e80-105">Asynchronous methods are ubiquitous in the Media Foundation pipeline.</span></span> <span data-ttu-id="84e80-106">Os métodos assíncronos facilitam a distribuição do trabalho entre vários threads.</span><span class="sxs-lookup"><span data-stu-id="84e80-106">Asynchronous methods make it easier to distribute work among several threads.</span></span> <span data-ttu-id="84e80-107">É particularmente importante executar e/s de forma assíncrona, para que a leitura de um arquivo ou rede não bloqueie o restante do pipeline.</span><span class="sxs-lookup"><span data-stu-id="84e80-107">It is particularly important to perform I/O asynchronously, so that reading from a file or network does not block the rest of the pipeline.</span></span>

<span data-ttu-id="84e80-108">Se você estiver escrevendo um coletor de mídia ou origem de mídia, é crucial tratar as operações assíncronas corretamente, pois o desempenho do componente tem um impacto em todo o pipeline.</span><span class="sxs-lookup"><span data-stu-id="84e80-108">If you are writing a media source or media sink, it is crucial to handle asynchronous operations correctly, because your component's performance has an impact on the entire pipeline.</span></span>

> [!Note]  
> <span data-ttu-id="84e80-109">As transformações de Media Foundation (MFTs) usam métodos síncronos por padrão.</span><span class="sxs-lookup"><span data-stu-id="84e80-109">Media Foundation transforms (MFTs) use synchronous methods by default.</span></span>

 

### <a name="work-queues-for-asynchronous-operations"></a><span data-ttu-id="84e80-110">Filas de trabalho para operações assíncronas</span><span class="sxs-lookup"><span data-stu-id="84e80-110">Work Queues For Asynchronous Operations</span></span>

<span data-ttu-id="84e80-111">Em Media Foundation, há uma relação de fechamento entre os [métodos de retorno de chamada assíncrono](asynchronous-callback-methods.md) e as [filas de trabalho](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="84e80-111">In Media Foundation, there is a close relationship between [Asynchronous Callback Methods](asynchronous-callback-methods.md) and [Work Queues](work-queues.md).</span></span> <span data-ttu-id="84e80-112">Uma fila de trabalho é uma abstração para mover o trabalho do thread do chamador para um thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="84e80-112">A work queue is an abstraction for moving work from the caller's thread to a worker thread.</span></span> <span data-ttu-id="84e80-113">Para executar o trabalho em uma fila de trabalho, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="84e80-113">To perform work on a work queue, do the following:</span></span>

1.  <span data-ttu-id="84e80-114">Implemente a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="84e80-114">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
2.  <span data-ttu-id="84e80-115">Chame [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para criar um objeto de *resultado* .</span><span class="sxs-lookup"><span data-stu-id="84e80-115">Call [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create a *result* object.</span></span> <span data-ttu-id="84e80-116">O objeto result expõe o [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult).</span><span class="sxs-lookup"><span data-stu-id="84e80-116">The result object exposes the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult).</span></span> <span data-ttu-id="84e80-117">O objeto de resultado contém três ponteiros:</span><span class="sxs-lookup"><span data-stu-id="84e80-117">The result object contains three pointers:</span></span>

    -   <span data-ttu-id="84e80-118">Um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) do chamador.</span><span class="sxs-lookup"><span data-stu-id="84e80-118">A pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="84e80-119">Um ponteiro opcional para um objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="84e80-119">An optional pointer to a state object.</span></span> <span data-ttu-id="84e80-120">Se especificado, o objeto de Estado deve implementar **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="84e80-120">If specified, the state object must implement **IUnknown**.</span></span>
    -   <span data-ttu-id="84e80-121">Um ponteiro opcional para um objeto particular.</span><span class="sxs-lookup"><span data-stu-id="84e80-121">An optional pointer to a private object.</span></span> <span data-ttu-id="84e80-122">Se especificado, esse objeto também deve implementar **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="84e80-122">If specified, this object also must implement **IUnknown**.</span></span>

    <span data-ttu-id="84e80-123">Os dois últimos ponteiros podem ser **nulos**.</span><span class="sxs-lookup"><span data-stu-id="84e80-123">The last two pointers can be **NULL**.</span></span> <span data-ttu-id="84e80-124">Caso contrário, use-os para manter informações sobre a operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="84e80-124">Otherwise, use them to hold information about the asynchronous operation.</span></span>

3.  <span data-ttu-id="84e80-125">Chame [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) para enfileirar para o item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="84e80-125">Call [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) to queue to the work item.</span></span>
4.  <span data-ttu-id="84e80-126">O thread de fila de trabalho chama o método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="84e80-126">The work-queue thread calls your [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span>
5.  <span data-ttu-id="84e80-127">Faça o trabalho dentro do seu método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="84e80-127">Do the work inside your [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="84e80-128">O parâmetro *pAsyncResult* desse método é o ponteiro [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) da etapa 2.</span><span class="sxs-lookup"><span data-stu-id="84e80-128">The *pAsyncResult* parameter of this method is the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) pointer from step 2.</span></span> <span data-ttu-id="84e80-129">Use este ponteiro para obter o objeto de estado e o objeto particular:</span><span class="sxs-lookup"><span data-stu-id="84e80-129">Use this pointer to get the state object and private object:</span></span>
    -   <span data-ttu-id="84e80-130">Para obter o objeto de estado, chame [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span><span class="sxs-lookup"><span data-stu-id="84e80-130">To get the state object, call [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span></span>
    -   <span data-ttu-id="84e80-131">Para obter o objeto particular, chame [**IMFAsyncResult:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).</span><span class="sxs-lookup"><span data-stu-id="84e80-131">To get the private object, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).</span></span>

<span data-ttu-id="84e80-132">Como alternativa, você pode combinar as etapas 2 e 3 chamando a função [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) .</span><span class="sxs-lookup"><span data-stu-id="84e80-132">As an alternative, you can combine steps 2 and 3 by calling the [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) function.</span></span> <span data-ttu-id="84e80-133">Internamente, essa função chama [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para criar o objeto de resultado.</span><span class="sxs-lookup"><span data-stu-id="84e80-133">Internally, this function calls [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create the result object.</span></span>

<span data-ttu-id="84e80-134">O diagrama a seguir mostra as relações entre o chamador, o objeto de resultado, o objeto de estado e o objeto particular.</span><span class="sxs-lookup"><span data-stu-id="84e80-134">The following diagram shows the relationships between the caller, the result object, the state object, and the private object.</span></span>

![diagrama mostrando um objeto de resultado assíncrono](images/workqueues01.png)

<span data-ttu-id="84e80-136">O diagrama de sequência a seguir mostra como um objeto enfileira um item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="84e80-136">The following sequence diagram shows how an object queues a work item.</span></span> <span data-ttu-id="84e80-137">Quando o thread de fila de trabalho chama [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), o objeto executa a operação assíncrona nesse thread.</span><span class="sxs-lookup"><span data-stu-id="84e80-137">When the work-queue thread calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), the object performs the asynchronous operation on that thread.</span></span>

![diagrama mostrando como um objeto enfileira um item de trabalho](images/workqueues02.png)

<span data-ttu-id="84e80-139">É importante lembrar que [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) é chamado de um thread que pertence à fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="84e80-139">It is important to remember [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) is called from a thread that is owned by the work queue.</span></span> <span data-ttu-id="84e80-140">Sua implementação de **Invoke** deve ser thread-safe.</span><span class="sxs-lookup"><span data-stu-id="84e80-140">Your implementation of **Invoke** must be thread safe.</span></span> <span data-ttu-id="84e80-141">Além disso, se você usar a fila de trabalho da plataforma (**\_ padrão de fila de retorno de chamada \_ \_ MFASYNC**), é essencial que nunca bloqueie o thread, pois isso pode bloquear todo o pipeline de Media Foundation do processamento de dados.</span><span class="sxs-lookup"><span data-stu-id="84e80-141">In addition, if you use the platform work queue (**MFASYNC\_CALLBACK\_QUEUE\_STANDARD**), it is critical that you never block the thread, because that can block the entire Media Foundation pipeline from processing data.</span></span> <span data-ttu-id="84e80-142">Se você precisar executar uma operação que irá bloquear ou levar muito tempo para ser concluída, use uma fila de trabalho particular.</span><span class="sxs-lookup"><span data-stu-id="84e80-142">If you need to perform an operation that will block or take a long time to complete, use a private work queue.</span></span> <span data-ttu-id="84e80-143">Para criar uma fila de trabalho particular, chame [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span><span class="sxs-lookup"><span data-stu-id="84e80-143">To create a private work queue, call [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span> <span data-ttu-id="84e80-144">Qualquer componente de pipeline que executa operações de e/s deve evitar o bloqueio de chamadas de e/s pelo mesmo motivo.</span><span class="sxs-lookup"><span data-stu-id="84e80-144">Any pipeline component that performs I/O operations should avoid blocking I/O calls for the same reason.</span></span> <span data-ttu-id="84e80-145">A interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) fornece uma abstração útil para e/s de arquivo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="84e80-145">The [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface provides a useful abstraction for asynchronous file I/O.</span></span>

### <a name="implementing-the-beginend-pattern"></a><span data-ttu-id="84e80-146">Implementando o Begin. ../end... Padrão</span><span class="sxs-lookup"><span data-stu-id="84e80-146">Implementing the Begin.../End... Pattern</span></span>

<span data-ttu-id="84e80-147">Conforme descrito em [chamando métodos assíncronos](calling-asynchronous-methods.md), os métodos assíncronos no Media Foundation geralmente usam o botão **Iniciar...** / **Terminar....** padrão.</span><span class="sxs-lookup"><span data-stu-id="84e80-147">As described in [Calling Asynchronous Methods](calling-asynchronous-methods.md), asynchronous methods in Media Foundation often use the **Begin...**/**End....** pattern.</span></span> <span data-ttu-id="84e80-148">Nesse padrão, uma operação assíncrona usa dois métodos com assinaturas semelhantes às seguintes:</span><span class="sxs-lookup"><span data-stu-id="84e80-148">In this pattern, an asynchronous operation uses two methods with signatures similar to the following:</span></span>

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

<span data-ttu-id="84e80-149">Para tornar o método realmente assíncrono, a implementação de **BeginX** deve executar o trabalho real em outro thread.</span><span class="sxs-lookup"><span data-stu-id="84e80-149">To make the method truly asynchronous, the implementation of **BeginX** must perform the actual work on another thread.</span></span> <span data-ttu-id="84e80-150">É aí que as filas de trabalho entram em cena.</span><span class="sxs-lookup"><span data-stu-id="84e80-150">This is where work queues come into the picture.</span></span> <span data-ttu-id="84e80-151">Nas etapas a seguir, o *chamador* é o código que chama **BeginX** e **EndX**.</span><span class="sxs-lookup"><span data-stu-id="84e80-151">In the steps that follow, the *caller* is the code that calls **BeginX** and **EndX**.</span></span> <span data-ttu-id="84e80-152">Isso pode ser um aplicativo ou o pipeline de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="84e80-152">This might be an application or the Media Foundation pipeline.</span></span> <span data-ttu-id="84e80-153">O *componente* é o código que implementa **BeginX** e **EndX**.</span><span class="sxs-lookup"><span data-stu-id="84e80-153">The *component* is the code that implements **BeginX** and **EndX**.</span></span>

1.  <span data-ttu-id="84e80-154">O chamador chama **begin...**, passando um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) do chamador.</span><span class="sxs-lookup"><span data-stu-id="84e80-154">The caller calls **Begin...**, passing in a pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
2.  <span data-ttu-id="84e80-155">O componente cria um novo objeto de resultado assíncrono.</span><span class="sxs-lookup"><span data-stu-id="84e80-155">The component creates a new asynchronous result object.</span></span> <span data-ttu-id="84e80-156">Esse objeto armazena a interface de retorno de chamada do chamador e o objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="84e80-156">This object stores the caller's callback interface and state object.</span></span> <span data-ttu-id="84e80-157">Normalmente, ele também armazena qualquer informação de estado particular que o componente precisa para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="84e80-157">Typically, it also stores any private state information that the component needs to complete the operation.</span></span> <span data-ttu-id="84e80-158">O objeto de resultado desta etapa é rotulado "resultado 1" no diagrama seguinte.</span><span class="sxs-lookup"><span data-stu-id="84e80-158">The result object from this step is labeled "Result 1" in the next diagram.</span></span>
3.  <span data-ttu-id="84e80-159">O componente cria um segundo objeto de resultado.</span><span class="sxs-lookup"><span data-stu-id="84e80-159">The component creates a second result object.</span></span> <span data-ttu-id="84e80-160">Esse objeto de resultado armazena dois ponteiros: o primeiro objeto de resultado e a interface de retorno de chamada do receptor.</span><span class="sxs-lookup"><span data-stu-id="84e80-160">This result object stores two pointers: The first result object, and the callback interface of the callee.</span></span> <span data-ttu-id="84e80-161">Esse objeto de resultado é rotulado "resultado 2" no próximo diagrama.</span><span class="sxs-lookup"><span data-stu-id="84e80-161">This result object is labeled "Result 2" in the next diagram.</span></span>
4.  <span data-ttu-id="84e80-162">O componente chama [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) para enfileirar um novo item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="84e80-162">The component calls [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) to queue a new work item.</span></span>
5.  <span data-ttu-id="84e80-163">No método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , o componente faz o trabalho assíncrono.</span><span class="sxs-lookup"><span data-stu-id="84e80-163">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, the component does the asynchronous work.</span></span>
6.  <span data-ttu-id="84e80-164">O componente chama [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) para invocar o método de retorno de chamada do chamador.</span><span class="sxs-lookup"><span data-stu-id="84e80-164">The component calls [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the caller's callback method.</span></span>
7.  <span data-ttu-id="84e80-165">O chamador chama o método **EndX** .</span><span class="sxs-lookup"><span data-stu-id="84e80-165">The caller calls the **EndX** method.</span></span>

![diagrama mostrando como um objeto implementa o padrão inicial/final](images/workqueues03.png)

## <a name="asynchronous-method-example"></a><span data-ttu-id="84e80-167">Exemplo do método assíncrono</span><span class="sxs-lookup"><span data-stu-id="84e80-167">Asynchronous Method Example</span></span>

<span data-ttu-id="84e80-168">Para ilustrar essa discussão, usaremos um exemplo de forçado.</span><span class="sxs-lookup"><span data-stu-id="84e80-168">To illustrate this discussion, we will use a contrived example.</span></span> <span data-ttu-id="84e80-169">Considere um método assíncrono para computar uma raiz quadrada:</span><span class="sxs-lookup"><span data-stu-id="84e80-169">Consider an asynchronous method for computing a square root:</span></span>


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



<span data-ttu-id="84e80-170">O parâmetro *x* de `BeginSquareRoot` é o valor cuja raiz quadrada será calculada.</span><span class="sxs-lookup"><span data-stu-id="84e80-170">The *x* parameter of `BeginSquareRoot` is the value whose square root will be calculated.</span></span> <span data-ttu-id="84e80-171">A raiz quadrada é retornada no parâmetro *PVal* de `EndSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="84e80-171">The square root is returned in the *pVal* parameter of `EndSquareRoot`.</span></span>

<span data-ttu-id="84e80-172">Aqui está a declaração de uma classe que implementa esses dois métodos:</span><span class="sxs-lookup"><span data-stu-id="84e80-172">Here is the declaration of a class that implements these two methods:</span></span>


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



<span data-ttu-id="84e80-173">A `SqrRoot` classe implementa [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) para que ela possa colocar a operação raiz quadrada em uma fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="84e80-173">The `SqrRoot` class implements [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) so that it can put the square root operation on a work queue.</span></span> <span data-ttu-id="84e80-174">O `DoCalculateSquareRoot` método é o método da classe privada que calcula a raiz quadrada.</span><span class="sxs-lookup"><span data-stu-id="84e80-174">The `DoCalculateSquareRoot` method is the private class method that calculates the square root.</span></span> <span data-ttu-id="84e80-175">Esse método será chamado a partir do thread da fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="84e80-175">This method will be called from the work queue thread.</span></span>

<span data-ttu-id="84e80-176">Primeiro, precisamos de uma maneira de armazenar o valor de *x*, para que ele possa ser recuperado quando o thread da fila de trabalho chamar `SqrRoot::Invoke` .</span><span class="sxs-lookup"><span data-stu-id="84e80-176">First, we need a way to store the value of *x*, so that it can be retrieved when the work queue thread calls `SqrRoot::Invoke`.</span></span> <span data-ttu-id="84e80-177">Aqui está uma classe simples que armazena as informações:</span><span class="sxs-lookup"><span data-stu-id="84e80-177">Here is a simple class that stores the information:</span></span>


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



<span data-ttu-id="84e80-178">Essa classe implementa **IUnknown** , de forma que possa ser armazenada em um objeto de resultado.</span><span class="sxs-lookup"><span data-stu-id="84e80-178">This class implements **IUnknown** so that it can be stored in a result object.</span></span>

<span data-ttu-id="84e80-179">O código a seguir implementa o `BeginSquareRoot` método:</span><span class="sxs-lookup"><span data-stu-id="84e80-179">The following code implements the `BeginSquareRoot` method:</span></span>


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



<span data-ttu-id="84e80-180">O código faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="84e80-180">This code does the following:</span></span>

1.  <span data-ttu-id="84e80-181">Cria uma nova instância da `AsyncOp` classe para armazenar o valor de *x*.</span><span class="sxs-lookup"><span data-stu-id="84e80-181">Creates a new instance of the `AsyncOp` class to hold the value of *x*.</span></span>
2.  <span data-ttu-id="84e80-182">Chama [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) para criar um objeto de resultado.</span><span class="sxs-lookup"><span data-stu-id="84e80-182">Calls [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create a result object.</span></span> <span data-ttu-id="84e80-183">Esse objeto contém vários ponteiros:</span><span class="sxs-lookup"><span data-stu-id="84e80-183">This object holds several pointers:</span></span>
    -   <span data-ttu-id="84e80-184">Um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) do chamador.</span><span class="sxs-lookup"><span data-stu-id="84e80-184">A pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="84e80-185">Um ponteiro para o objeto de estado do chamador (*pState*).</span><span class="sxs-lookup"><span data-stu-id="84e80-185">A pointer to the caller's state object (*pState*).</span></span>
    -   <span data-ttu-id="84e80-186">Um ponteiro para o objeto `AsyncOp`.</span><span class="sxs-lookup"><span data-stu-id="84e80-186">A pointer to the `AsyncOp` object.</span></span>
3.  <span data-ttu-id="84e80-187">Chama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) para enfileirar um novo item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="84e80-187">Calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) to queue a new work item.</span></span> <span data-ttu-id="84e80-188">Essa chamada Cria implicitamente um objeto de resultado externo, que contém os seguintes ponteiros:</span><span class="sxs-lookup"><span data-stu-id="84e80-188">This call implicitly creates an outer result object, which holds the following pointers:</span></span>
    -   <span data-ttu-id="84e80-189">Um ponteiro para a `SqrRoot` interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) do objeto.</span><span class="sxs-lookup"><span data-stu-id="84e80-189">A pointer to the `SqrRoot` object's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="84e80-190">Um ponteiro para o objeto de resultado interno da etapa 2.</span><span class="sxs-lookup"><span data-stu-id="84e80-190">A pointer to the inner result object from step 2.</span></span>

<span data-ttu-id="84e80-191">O código a seguir implementa o `SqrRoot::Invoke` método:</span><span class="sxs-lookup"><span data-stu-id="84e80-191">The following code implements the `SqrRoot::Invoke` method:</span></span>


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



<span data-ttu-id="84e80-192">Esse método obtém o objeto de resultado interno e o `AsyncOp` objeto.</span><span class="sxs-lookup"><span data-stu-id="84e80-192">This method gets the inner result object and the `AsyncOp` object.</span></span> <span data-ttu-id="84e80-193">Em seguida, ele passa o `AsyncOp` objeto para `DoCalculateSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="84e80-193">Then it passes the `AsyncOp` object to `DoCalculateSquareRoot`.</span></span> <span data-ttu-id="84e80-194">Por fim, ele chama [**IMFAsyncResult:: SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) para definir o código de status e [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) para invocar o método de retorno de chamada do chamador.</span><span class="sxs-lookup"><span data-stu-id="84e80-194">Finally, it calls [**IMFAsyncResult::SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) to set the status code and [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the caller's callback method.</span></span>

<span data-ttu-id="84e80-195">O `DoCalculateSquareRoot` método faz exatamente o que você esperaria:</span><span class="sxs-lookup"><span data-stu-id="84e80-195">The `DoCalculateSquareRoot` method does exactly what you would expect:</span></span>


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



<span data-ttu-id="84e80-196">Quando o método de retorno de chamada do chamador é invocado, é responsabilidade do chamador chamar o método **end...** — nesse caso, `EndSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="84e80-196">When the caller's callback method is invoked, it is the caller's responsibility to call the **End...** method—in this case, `EndSquareRoot`.</span></span> <span data-ttu-id="84e80-197">O `EndSquareRoot` é como o chamador recupera o resultado da operação assíncrona, que neste exemplo é a raiz quadrada computada.</span><span class="sxs-lookup"><span data-stu-id="84e80-197">The `EndSquareRoot` is how the caller retrieves the result of the asynchronous operation, which in this example is the computed square root.</span></span> <span data-ttu-id="84e80-198">Essas informações são armazenadas no objeto de resultado:</span><span class="sxs-lookup"><span data-stu-id="84e80-198">This information is stored in the result object:</span></span>


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



## <a name="operation-queues"></a><span data-ttu-id="84e80-199">Filas de operação</span><span class="sxs-lookup"><span data-stu-id="84e80-199">Operation Queues</span></span>

<span data-ttu-id="84e80-200">Até agora, foi tacitly pressupor que uma operação assíncrona poderia ser feita a qualquer momento, independentemente do estado atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="84e80-200">So far, it has been tacitly assumed that an asynchronous operation could be done at any time, regardless of the object's current state.</span></span> <span data-ttu-id="84e80-201">Por exemplo, considere o que acontece se um aplicativo chama `BeginSquareRoot` enquanto uma chamada anterior para o mesmo método ainda está pendente.</span><span class="sxs-lookup"><span data-stu-id="84e80-201">For example, consider what happens if an application calls `BeginSquareRoot` while an earlier call to the same method is still pending.</span></span> <span data-ttu-id="84e80-202">A `SqrRoot` classe pode enfileirar o novo item de trabalho antes que o item de trabalho anterior seja concluído.</span><span class="sxs-lookup"><span data-stu-id="84e80-202">The `SqrRoot` class might queue the new work item before the previous work item is done.</span></span> <span data-ttu-id="84e80-203">No entanto, as filas de trabalho não têm garantia de serializar itens de trabalho.</span><span class="sxs-lookup"><span data-stu-id="84e80-203">However, work queues are not guaranteed to serialize work items.</span></span> <span data-ttu-id="84e80-204">Lembre-se de que uma fila de trabalho pode usar mais de um thread para distribuir itens de trabalho.</span><span class="sxs-lookup"><span data-stu-id="84e80-204">Recall that a work queue can use more than one thread to dispatch work items.</span></span> <span data-ttu-id="84e80-205">Em um ambiente multi-threaded, um item de trabalho pode ser invocado antes da conclusão da tarefa anterior.</span><span class="sxs-lookup"><span data-stu-id="84e80-205">In a multithreaded environment, a work item might be invoked before the previous one has completed.</span></span> <span data-ttu-id="84e80-206">Os itens de trabalho podem até mesmo ser invocados fora de ordem, se ocorrer uma alternância de contexto logo antes do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="84e80-206">Work items can even be invoked out of order, if a context switch happens to occur just before the callback is invoked.</span></span>

<span data-ttu-id="84e80-207">Por esse motivo, é responsabilidade do objeto serializar operações em si mesmo, se necessário.</span><span class="sxs-lookup"><span data-stu-id="84e80-207">For this reason, it is the object's responsibility to serialize operations on itself, if required.</span></span> <span data-ttu-id="84e80-208">Em outras palavras, se o objeto exigir que *a operação a seja concluída* antes que a operação *B* possa ser iniciada, o objeto não deverá enfileirar um item de trabalho para *B* até que *a operação A* seja concluída.</span><span class="sxs-lookup"><span data-stu-id="84e80-208">In other words, if the object requires operation *A* to finish before operation *B* can start, the object must not queue a work item for *B* until operation *A* has completed.</span></span> <span data-ttu-id="84e80-209">Um objeto pode atender a esse requisito tendo sua própria fila de operações pendentes.</span><span class="sxs-lookup"><span data-stu-id="84e80-209">An object can meet this requirement by having its own queue of pending operations.</span></span> <span data-ttu-id="84e80-210">Quando um método assíncrono é chamado no objeto, o objeto coloca a solicitação em sua própria fila.</span><span class="sxs-lookup"><span data-stu-id="84e80-210">When an asynchronous method is called on the object, the object puts the request on its own queue.</span></span> <span data-ttu-id="84e80-211">Como cada operação assíncrona é concluída, o objeto recebe a próxima solicitação da fila.</span><span class="sxs-lookup"><span data-stu-id="84e80-211">As each asynchronous operation is completed, the object pulls the next request from the queue.</span></span> <span data-ttu-id="84e80-212">O [exemplo MPEG1Source](mpeg1source-sample.md) mostra um exemplo de como implementar essa fila.</span><span class="sxs-lookup"><span data-stu-id="84e80-212">The [MPEG1Source Sample](mpeg1source-sample.md) shows an example of how to implement such a queue.</span></span>

<span data-ttu-id="84e80-213">Um único método pode envolver várias operações assíncronas, especialmente quando chamadas de e/s são usadas.</span><span class="sxs-lookup"><span data-stu-id="84e80-213">A single method might involve several asynchronous operations, particularly when I/O calls are used.</span></span> <span data-ttu-id="84e80-214">Ao implementar métodos assíncronos, pense atentamente sobre os requisitos de serialização.</span><span class="sxs-lookup"><span data-stu-id="84e80-214">When you implement asynchronous methods, think carefully about serialization requirements.</span></span> <span data-ttu-id="84e80-215">Por exemplo, é válido para o objeto iniciar uma nova operação enquanto uma solicitação de e/s anterior ainda está pendente?</span><span class="sxs-lookup"><span data-stu-id="84e80-215">For example, is it valid for the object to start a new operation while a previous I/O request is still pending?</span></span> <span data-ttu-id="84e80-216">Se a nova operação alterar o estado interno do objeto, o que acontece quando uma solicitação de e/s anterior é concluída e retorna dados que agora podem estar obsoletos?</span><span class="sxs-lookup"><span data-stu-id="84e80-216">If the new operation changes the object's internal state, what happens when a previous I/O request completes and returns data that might now be stale?</span></span> <span data-ttu-id="84e80-217">Um bom diagrama de estado pode ajudar a identificar as transições de estado válidas.</span><span class="sxs-lookup"><span data-stu-id="84e80-217">A good state diagram can help to identify the valid state transitions.</span></span>

## <a name="cross-thread-and-cross-process-considerations"></a><span data-ttu-id="84e80-218">Considerações entre threads e processos cruzados</span><span class="sxs-lookup"><span data-stu-id="84e80-218">Cross-Thread and Cross-Process Considerations</span></span>

<span data-ttu-id="84e80-219">As filas de trabalho não usam o marshaling COM para empacotar ponteiros de interface entre limites de thread.</span><span class="sxs-lookup"><span data-stu-id="84e80-219">Work queues do not use COM marshaling to marshal interface pointers across thread boundaries.</span></span> <span data-ttu-id="84e80-220">Portanto, mesmo que um objeto seja registrado como Apartment-Threaded ou o thread do aplicativo tenha inserido um STA (single-threaded apartment), os retornos de chamada [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) serão invocados de um thread diferente.</span><span class="sxs-lookup"><span data-stu-id="84e80-220">Therefore, even if an object is registered as apartment-threaded or the application thread has entered a single-threaded apartment (STA), [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callbacks will be invoked from a different thread.</span></span> <span data-ttu-id="84e80-221">Em qualquer caso, todos os componentes de pipeline Media Foundation devem usar o modelo de Threading "both".</span><span class="sxs-lookup"><span data-stu-id="84e80-221">In any case, all Media Foundation pipeline components should use the "Both" threading model.</span></span>

<span data-ttu-id="84e80-222">Algumas interfaces no Media Foundation definem versões remotas de alguns métodos assíncronos.</span><span class="sxs-lookup"><span data-stu-id="84e80-222">Some interfaces in Media Foundation define remote versions of some asynchronous methods.</span></span> <span data-ttu-id="84e80-223">Quando um desses métodos é chamado entre limites de processo, a DLL Media Foundation proxy/stub chama a versão remota do método, que executa o marshaling personalizado dos parâmetros do método.</span><span class="sxs-lookup"><span data-stu-id="84e80-223">When one of these methods is called across process boundaries, the Media Foundation proxy/stub DLL calls the remote version of the method, which performs custom marshaling of the method parameters.</span></span> <span data-ttu-id="84e80-224">No processo remoto, o stub traduz a chamada de volta para o método local no objeto.</span><span class="sxs-lookup"><span data-stu-id="84e80-224">In the remote process, the stub translates the call back into the local method on the object.</span></span> <span data-ttu-id="84e80-225">Esse processo é transparente para o aplicativo e o objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="84e80-225">This process is transparent to both the application and the remote object.</span></span> <span data-ttu-id="84e80-226">Esses métodos de marshaling personalizados são fornecidos principalmente para objetos que são carregados no caminho de mídia protegido (PMP).</span><span class="sxs-lookup"><span data-stu-id="84e80-226">These custom marshaling methods are provided primarily for objects that are loaded in the protected media path (PMP).</span></span> <span data-ttu-id="84e80-227">Para obter mais informações sobre o PMP, consulte [proteção de caminho de mídia](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="84e80-227">For more information about the PMP, see [Protected Media Path](protected-media-path.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84e80-228">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="84e80-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84e80-229">Métodos de retorno de chamada assíncrono</span><span class="sxs-lookup"><span data-stu-id="84e80-229">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> <dt>

[<span data-ttu-id="84e80-230">Filas de trabalho</span><span class="sxs-lookup"><span data-stu-id="84e80-230">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 



