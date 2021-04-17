---
description: A classe CAMThread é uma classe abstrata para gerenciar threads de trabalho.
ms.assetid: c217d879-0203-4566-96ad-7463b05bc990
title: Classe CAMThread (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c2bde058267ae4c530f33a96778792d5fe247b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757048"
---
# <a name="camthread-class"></a><span data-ttu-id="d12d1-103">Classe CAMThread</span><span class="sxs-lookup"><span data-stu-id="d12d1-103">CAMThread class</span></span>

<span data-ttu-id="d12d1-104">A `CAMThread` classe é uma classe abstrata para gerenciar threads de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d12d1-104">The `CAMThread` class is an abstract class for managing worker threads.</span></span>



| <span data-ttu-id="d12d1-105">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="d12d1-105">Protected Member Variables</span></span>                                 | <span data-ttu-id="d12d1-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d12d1-106">Description</span></span>                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="d12d1-107">**\_hThread m**</span><span class="sxs-lookup"><span data-stu-id="d12d1-107">**m\_hThread**</span></span>](camthread-m-hthread.md)                  | <span data-ttu-id="d12d1-108">Identificador para o thread.</span><span class="sxs-lookup"><span data-stu-id="d12d1-108">Handle to the thread.</span></span>                                                        |
| <span data-ttu-id="d12d1-109">Variáveis de membro público</span><span class="sxs-lookup"><span data-stu-id="d12d1-109">Public Member Variables</span></span>                                    | <span data-ttu-id="d12d1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d12d1-110">Description</span></span>                                                                  |
| [<span data-ttu-id="d12d1-111">**\_AccessLock m**</span><span class="sxs-lookup"><span data-stu-id="d12d1-111">**m\_AccessLock**</span></span>](camthread-m-accesslock.md)            | <span data-ttu-id="d12d1-112">Seção crítica que impede que o thread seja acessado por outros threads.</span><span class="sxs-lookup"><span data-stu-id="d12d1-112">Critical section that locks the thread from being accessed by other threads.</span></span> |
| [<span data-ttu-id="d12d1-113">**\_WorkerLock m**</span><span class="sxs-lookup"><span data-stu-id="d12d1-113">**m\_WorkerLock**</span></span>](camthread-m-workerlock.md)            | <span data-ttu-id="d12d1-114">Seção crítica que bloqueia os dados compartilhados entre threads.</span><span class="sxs-lookup"><span data-stu-id="d12d1-114">Critical section that locks data shared among threads.</span></span>                       |
| <span data-ttu-id="d12d1-115">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="d12d1-115">Public Methods</span></span>                                             | <span data-ttu-id="d12d1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d12d1-116">Description</span></span>                                                                  |
| [<span data-ttu-id="d12d1-117">**CAMThread**</span><span class="sxs-lookup"><span data-stu-id="d12d1-117">**CAMThread**</span></span>](camthread-camthread.md)                   | <span data-ttu-id="d12d1-118">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="d12d1-118">Constructor method.</span></span>                                                          |
| [<span data-ttu-id="d12d1-119">**~ CAMThread**</span><span class="sxs-lookup"><span data-stu-id="d12d1-119">**~ CAMThread**</span></span>](camthread--camthread.md)                | <span data-ttu-id="d12d1-120">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="d12d1-120">Destructor method.</span></span> <span data-ttu-id="d12d1-121">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="d12d1-121">Virtual.</span></span>                                                  |
| [<span data-ttu-id="d12d1-122">**InitialThreadProc**</span><span class="sxs-lookup"><span data-stu-id="d12d1-122">**InitialThreadProc**</span></span>](camthread-initialthreadproc.md)   | <span data-ttu-id="d12d1-123">Chama o método ThreadProc quando o thread é criado.</span><span class="sxs-lookup"><span data-stu-id="d12d1-123">Calls the ThreadProc method when the thread is created.</span></span>                      |
| [<span data-ttu-id="d12d1-124">**Criar**</span><span class="sxs-lookup"><span data-stu-id="d12d1-124">**Create**</span></span>](camthread-create.md)                         | <span data-ttu-id="d12d1-125">Cria o thread.</span><span class="sxs-lookup"><span data-stu-id="d12d1-125">Creates the thread.</span></span>                                                          |
| [<span data-ttu-id="d12d1-126">**CallWorker**</span><span class="sxs-lookup"><span data-stu-id="d12d1-126">**CallWorker**</span></span>](camthread-callworker.md)                 | <span data-ttu-id="d12d1-127">Sinaliza o thread com uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="d12d1-127">Signals the thread with a request.</span></span>                                           |
| [<span data-ttu-id="d12d1-128">**Fechar**</span><span class="sxs-lookup"><span data-stu-id="d12d1-128">**Close**</span></span>](camthread-close.md)                           | <span data-ttu-id="d12d1-129">Aguarda até que o thread saia e, em seguida, libera seus recursos.</span><span class="sxs-lookup"><span data-stu-id="d12d1-129">Waits for the thread to exit, then releases its resources.</span></span>                   |
| [<span data-ttu-id="d12d1-130">**ThreadExists**</span><span class="sxs-lookup"><span data-stu-id="d12d1-130">**ThreadExists**</span></span>](camthread-threadexists.md)             | <span data-ttu-id="d12d1-131">Consulta se o thread existe.</span><span class="sxs-lookup"><span data-stu-id="d12d1-131">Queries whether the thread exists.</span></span>                                           |
| [<span data-ttu-id="d12d1-132">**GetRequest**</span><span class="sxs-lookup"><span data-stu-id="d12d1-132">**GetRequest**</span></span>](camthread-getrequest.md)                 | <span data-ttu-id="d12d1-133">Aguarda a próxima solicitação.</span><span class="sxs-lookup"><span data-stu-id="d12d1-133">Waits for the next request.</span></span>                                                  |
| [<span data-ttu-id="d12d1-134">**CheckRequest**</span><span class="sxs-lookup"><span data-stu-id="d12d1-134">**CheckRequest**</span></span>](camthread-checkrequest.md)             | <span data-ttu-id="d12d1-135">Verifica se há uma solicitação, sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="d12d1-135">Checks if there is a request, without blocking.</span></span>                              |
| [<span data-ttu-id="d12d1-136">**Responder**</span><span class="sxs-lookup"><span data-stu-id="d12d1-136">**Reply**</span></span>](camthread-reply.md)                           | <span data-ttu-id="d12d1-137">Responde a uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="d12d1-137">Replies to a request.</span></span>                                                        |
| [<span data-ttu-id="d12d1-138">**GetRequestHandle**</span><span class="sxs-lookup"><span data-stu-id="d12d1-138">**GetRequestHandle**</span></span>](camthread-getrequesthandle.md)     | <span data-ttu-id="d12d1-139">Recupera um identificador para o evento sinalizado pelo método CallWorker.</span><span class="sxs-lookup"><span data-stu-id="d12d1-139">Retrieves a handle to the event signaled by the CallWorker method.</span></span>           |
| [<span data-ttu-id="d12d1-140">**GetRequestParam**</span><span class="sxs-lookup"><span data-stu-id="d12d1-140">**GetRequestParam**</span></span>](camthread-getrequestparam.md)       | <span data-ttu-id="d12d1-141">Recupera a solicitação mais recente.</span><span class="sxs-lookup"><span data-stu-id="d12d1-141">Retrieves the latest request.</span></span>                                                |
| [<span data-ttu-id="d12d1-142">**CoInitializeHelper**</span><span class="sxs-lookup"><span data-stu-id="d12d1-142">**CoInitializeHelper**</span></span>](camthread-coinitializehelper.md) | <span data-ttu-id="d12d1-143">Chama CoInitializeEx no início do thread.</span><span class="sxs-lookup"><span data-stu-id="d12d1-143">Calls CoInitializeEx at the start of the thread.</span></span>                             |
| <span data-ttu-id="d12d1-144">Métodos virtuais puros</span><span class="sxs-lookup"><span data-stu-id="d12d1-144">Pure Virtual Methods</span></span>                                       | <span data-ttu-id="d12d1-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="d12d1-145">Description</span></span>                                                                  |
| [<span data-ttu-id="d12d1-146">**ThreadProc**</span><span class="sxs-lookup"><span data-stu-id="d12d1-146">**ThreadProc**</span></span>](camthread-threadproc.md)                 | <span data-ttu-id="d12d1-147">Procedimento de thread.</span><span class="sxs-lookup"><span data-stu-id="d12d1-147">Thread procedure.</span></span>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="d12d1-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="d12d1-148">Remarks</span></span>

<span data-ttu-id="d12d1-149">Essa classe fornece métodos para criar um thread de trabalho, passar solicitações para o thread e aguardar a saída do thread.</span><span class="sxs-lookup"><span data-stu-id="d12d1-149">This class provides methods for creating a worker thread, passing requests to the thread, and waiting for the thread to exit.</span></span> <span data-ttu-id="d12d1-150">Para usar essa classe, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d12d1-150">To use this class, do the following:</span></span>

-   <span data-ttu-id="d12d1-151">Derive uma classe de `CAMThread` e substitua o método virtual puro [**CAMThread:: ThreadProc**](camthread-threadproc.md).</span><span class="sxs-lookup"><span data-stu-id="d12d1-151">Derive a class from `CAMThread` and override the pure virtual method [**CAMThread::ThreadProc**](camthread-threadproc.md).</span></span> <span data-ttu-id="d12d1-152">Esse método é o procedimento de thread que é chamado no início do thread.</span><span class="sxs-lookup"><span data-stu-id="d12d1-152">This method is the thread procedure that gets called at the start of the thread.</span></span>
-   <span data-ttu-id="d12d1-153">Em seu aplicativo, crie uma instância da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="d12d1-153">In your application, create an instance of your derived class.</span></span> <span data-ttu-id="d12d1-154">A criação do objeto não cria o thread.</span><span class="sxs-lookup"><span data-stu-id="d12d1-154">Creating the object does not create the thread.</span></span> <span data-ttu-id="d12d1-155">Para criar o thread, chame o método [**CAMThread:: Create**](camthread-create.md) .</span><span class="sxs-lookup"><span data-stu-id="d12d1-155">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>
-   <span data-ttu-id="d12d1-156">Para enviar solicitações para o thread, chame o método [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="d12d1-156">To send requests to the thread, call the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span> <span data-ttu-id="d12d1-157">Esse método usa um parâmetro DWORD, cujo significado é definido por sua classe.</span><span class="sxs-lookup"><span data-stu-id="d12d1-157">This method takes a DWORD parameter, whose meaning is defined by your class.</span></span> <span data-ttu-id="d12d1-158">O método é bloqueado até que o thread responda (veja abaixo).</span><span class="sxs-lookup"><span data-stu-id="d12d1-158">The method blocks until the thread responds (see below).</span></span>
-   <span data-ttu-id="d12d1-159">Em seu procedimento de thread, responda a solicitações chamando [**CAMThread:: GetRequest**](camthread-getrequest.md) ou [**CAMThread:: CheckRequest**](camthread-checkrequest.md).</span><span class="sxs-lookup"><span data-stu-id="d12d1-159">In your thread procedure, respond to requests by calling either [**CAMThread::GetRequest**](camthread-getrequest.md) or [**CAMThread::CheckRequest**](camthread-checkrequest.md).</span></span> <span data-ttu-id="d12d1-160">O método GetRequest é bloqueado até que outro thread chame CallWorker.</span><span class="sxs-lookup"><span data-stu-id="d12d1-160">The GetRequest method blocks until another thread calls CallWorker.</span></span> <span data-ttu-id="d12d1-161">O método CheckRequest é sem bloqueio, o que permite que o thread Verifique se há novas solicitações enquanto trabalha de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="d12d1-161">The CheckRequest method is non-blocking, which enables the thread to check for new requests while working asynchronously.</span></span>
-   <span data-ttu-id="d12d1-162">Quando o thread recebe uma solicitação, chame [**CAMThread:: Reply**](camthread-reply.md) para desbloquear o thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="d12d1-162">When the thread receives a request, call [**CAMThread::Reply**](camthread-reply.md) to unblock the calling thread.</span></span> <span data-ttu-id="d12d1-163">O método Reply usa um parâmetro DWORD, que é passado para o thread de chamada como o valor de retorno para CallWorker.</span><span class="sxs-lookup"><span data-stu-id="d12d1-163">The Reply method takes a DWORD parameter, which is passed to the calling thread as the return value for CallWorker.</span></span>

<span data-ttu-id="d12d1-164">Quando terminar com o thread, chame o método [**CAMThread:: Close**](camthread-close.md) .</span><span class="sxs-lookup"><span data-stu-id="d12d1-164">When you are done with the thread, call the [**CAMThread::Close**](camthread-close.md) method.</span></span> <span data-ttu-id="d12d1-165">Esse método aguarda a saída do thread e fecha o identificador de thread.</span><span class="sxs-lookup"><span data-stu-id="d12d1-165">This method waits for the thread to exit, and then closes the thread handle.</span></span> <span data-ttu-id="d12d1-166">Sua mensagem ThreadProc deve ser garantida para sair, seja por conta própria ou em resposta a uma solicitação CallWorker.</span><span class="sxs-lookup"><span data-stu-id="d12d1-166">Your ThreadProc message must be guaranteed to exit, either on its own or in response to a CallWorker request.</span></span> <span data-ttu-id="d12d1-167">O método destruidor também chama Close.</span><span class="sxs-lookup"><span data-stu-id="d12d1-167">The destructor method also calls Close.</span></span>

<span data-ttu-id="d12d1-168">O exemplo a seguir ilustra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="d12d1-168">The following example illustrates these steps:</span></span>


```C++
class MyThread : public CAMThread
{
protected:
    DWORD ThreadProc(void);
};

DWORD MyThread::ThreadProc()
{
    BOOL bShutDown = FALSE;
    while (!bShutDown)
    {
        DWORD req = GetRequest();
        printf("Request: %d\n", req);
        bShutDown = (req == 0);
        Reply(bShutDown ? S_FALSE : S_OK);
    }
    printf("Quitting Thread\n");
    return 1;
}

void main()
{
    MyThread thread;
    DWORD reply;
    
    thread.Create();
    reply = thread.CallWorker(3);
    reply = thread.CallWorker(0); // Thread exits.
}
```



<span data-ttu-id="d12d1-169">Em sua classe derivada, você também pode definir funções de membro que validam os parâmetros para CallWorker.</span><span class="sxs-lookup"><span data-stu-id="d12d1-169">In your derived class, you can also define member functions that validate the parameters to CallWorker.</span></span> <span data-ttu-id="d12d1-170">O exemplo a seguir mostra uma maneira típica de fazer isso:</span><span class="sxs-lookup"><span data-stu-id="d12d1-170">The following example shows a typical way to do this:</span></span>


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



<span data-ttu-id="d12d1-171">A `CAMThread` classe fornece duas seções críticas como variáveis de membro público.</span><span class="sxs-lookup"><span data-stu-id="d12d1-171">The `CAMThread` class provides two critical sections as public member variables.</span></span> <span data-ttu-id="d12d1-172">Use `CAMThread::m_AccessLock` para bloquear o acesso do thread por outros threads.</span><span class="sxs-lookup"><span data-stu-id="d12d1-172">Use `CAMThread::m_AccessLock` to lock the thread from being accessed by other threads.</span></span> <span data-ttu-id="d12d1-173">(Por exemplo, os métodos Create e CallWorker mantêm esse bloqueio para serializar operações no thread.) Use [**CAMThread:: m \_ WorkerLock**](camthread-m-workerlock.md) para bloquear dados compartilhados entre threads.</span><span class="sxs-lookup"><span data-stu-id="d12d1-173">(For example, the Create and CallWorker methods hold this lock, to serialize operations on the thread.) Use [**CAMThread::m\_WorkerLock**](camthread-m-workerlock.md) to lock data that is shared among threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="d12d1-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d12d1-174">Requirements</span></span>



| <span data-ttu-id="d12d1-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="d12d1-175">Requirement</span></span> | <span data-ttu-id="d12d1-176">Valor</span><span class="sxs-lookup"><span data-stu-id="d12d1-176">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d12d1-177">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d12d1-177">Header</span></span><br/>  | <dl> <span data-ttu-id="d12d1-178"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d12d1-178"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d12d1-179">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d12d1-179">Library</span></span><br/> | <dl> <span data-ttu-id="d12d1-180"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d12d1-180"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




