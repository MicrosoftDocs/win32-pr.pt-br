---
description: Os aplicativos WMI escritos em C++ podem fazer chamadas assíncronas usando muitos dos métodos da interface COM de IWbemServices.
ms.assetid: 5179969f-bc7d-4408-84ef-7b003950a59f
ms.tgt_platform: multiple
title: Fazendo uma chamada assíncrona com C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f093aef4b1a1b4dbede53333e77d737f8efd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791425"
---
# <a name="making-an-asynchronous-call-with-c"></a><span data-ttu-id="767e2-103">Fazendo uma chamada assíncrona com C++</span><span class="sxs-lookup"><span data-stu-id="767e2-103">Making an Asynchronous Call with C++</span></span>

<span data-ttu-id="767e2-104">Os aplicativos WMI escritos em C++ podem fazer chamadas assíncronas usando muitos dos métodos da interface com de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="767e2-104">WMI applications written in C++ can make asynchronous calls by using many of the methods of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) COM interface.</span></span> <span data-ttu-id="767e2-105">No entanto, o procedimento recomendado para chamar um [*método WMI*](gloss-w.md) ou um [*método de provedor*](gloss-p.md) é usar chamadas semisynchronous porque chamadas semisynchronous são mais seguras do que chamadas assíncronas.</span><span class="sxs-lookup"><span data-stu-id="767e2-105">However, the recommended procedure for calling a [*WMI method*](gloss-w.md) or a [*provider method*](gloss-p.md) is by using semisynchronous calls because semisynchronous calls are more secure than asynchronous calls.</span></span> <span data-ttu-id="767e2-106">Para obter mais informações, consulte [fazendo uma chamada Semisynchronous com C++](making-a-semisynchronous-call-with-c--.md) e [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="767e2-106">For more information, see [Making a Semisynchronous Call with C++](making-a-semisynchronous-call-with-c--.md) and [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="767e2-107">O procedimento a seguir descreve como fazer uma chamada assíncrona usando o coletor em seu processo.</span><span class="sxs-lookup"><span data-stu-id="767e2-107">The following procedure describes how to make an asynchronous call by using the sink in your process.</span></span>

<span data-ttu-id="767e2-108">**Para fazer uma chamada assíncrona usando C++**</span><span class="sxs-lookup"><span data-stu-id="767e2-108">**To make an asynchronous call using C++**</span></span>

1.  <span data-ttu-id="767e2-109">Implemente a interface [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="767e2-109">Implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="767e2-110">Todos os aplicativos que fazem chamadas assíncronas devem implementar [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="767e2-110">All applications that make asynchronous calls must implement [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="767e2-111">Os consumidores de eventos temporários também implementam **IWbemObjectSink** para receber notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="767e2-111">Temporary event consumers also implement **IWbemObjectSink** to receive notification of events.</span></span>

2.  <span data-ttu-id="767e2-112">Faça logon no namespace WMI de destino.</span><span class="sxs-lookup"><span data-stu-id="767e2-112">Log on to the target WMI namespace.</span></span>

    <span data-ttu-id="767e2-113">Os aplicativos sempre precisam chamar a função COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) durante a fase de inicialização.</span><span class="sxs-lookup"><span data-stu-id="767e2-113">Applications always have to call the COM function [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) during the initialization phase.</span></span> <span data-ttu-id="767e2-114">Se eles não fizerem isso antes de fazer uma chamada assíncrona, o WMI liberará o coletor de aplicativos sem concluir a chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="767e2-114">If they do not do so before making an asynchronous call, WMI releases the application sink without completing the asynchronous call.</span></span> <span data-ttu-id="767e2-115">Para obter mais informações, consulte [Inicializando com para um aplicativo WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="767e2-115">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

3.  <span data-ttu-id="767e2-116">Defina a segurança para o coletor.</span><span class="sxs-lookup"><span data-stu-id="767e2-116">Set the security for your sink.</span></span>

    <span data-ttu-id="767e2-117">As chamadas assíncronas criam uma variedade de problemas de segurança com os quais você pode ter que lidar, por exemplo, permitindo o acesso de WMI ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="767e2-117">Asynchronous calls create a variety of security issues that you may have to deal with, for example, allowing WMI access to your application.</span></span> <span data-ttu-id="767e2-118">Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="767e2-118">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

4.  <span data-ttu-id="767e2-119">Faça a chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="767e2-119">Make the asynchronous call.</span></span>

    <span data-ttu-id="767e2-120">O método retorna imediatamente com o código de falha de **\_ \_ \_ erro WBEM S** .</span><span class="sxs-lookup"><span data-stu-id="767e2-120">The method returns immediately with the **WBEM\_S\_NO\_ERROR** success code.</span></span> <span data-ttu-id="767e2-121">O aplicativo pode continuar com outras tarefas enquanto aguarda a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="767e2-121">The application can proceed with other tasks while waiting for the operation to complete.</span></span> <span data-ttu-id="767e2-122">Os relatórios WMI de volta para o aplicativo chamando métodos na implementação [**IWbemObjectSink**](iwbemobjectsink.md) do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="767e2-122">WMI reports back to the application by calling methods in the [**IWbemObjectSink**](iwbemobjectsink.md) implementation of your application.</span></span>

5.  <span data-ttu-id="767e2-123">Se necessário, verifique sua implementação periodicamente para obter atualizações.</span><span class="sxs-lookup"><span data-stu-id="767e2-123">If necessary, check your implementation periodically for updates.</span></span>

    <span data-ttu-id="767e2-124">Os aplicativos podem receber a notificação do status intermediário definindo o parâmetro *lFlags* na chamada assíncrona para o **\_ sinalizador WBEM \_ Enviar \_ status**.</span><span class="sxs-lookup"><span data-stu-id="767e2-124">Applications can receive notification of intermediate status by setting the *lFlags* parameter in the asynchronous call to **WBEM\_FLAG\_SEND\_STATUS**.</span></span> <span data-ttu-id="767e2-125">O WMI relata o status de sua chamada definindo o parâmetro *lFlags* de [**IWbemObjectSink**](iwbemobjectsink.md) para **o \_ \_ progresso do status do WBEM**.</span><span class="sxs-lookup"><span data-stu-id="767e2-125">WMI reports the status of your call by setting the *lFlags* parameter of [**IWbemObjectSink**](iwbemobjectsink.md) to **WBEM\_STATUS\_PROGRESS**.</span></span>

6.  <span data-ttu-id="767e2-126">Se necessário, você pode cancelar a chamada antes de o WMI concluir o processamento chamando o método [**IWbemServices:: CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .</span><span class="sxs-lookup"><span data-stu-id="767e2-126">If necessary, you can cancel the call before WMI finishes processing by calling the [**IWbemServices::CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method.</span></span>

    <span data-ttu-id="767e2-127">O método [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) cancela o processamento assíncrono, liberando imediatamente o ponteiro para a interface [**IWbemObjectSink**](iwbemobjectsink.md) e garante que o ponteiro seja liberado antes que **CancelAsyncCall** seja retornado.</span><span class="sxs-lookup"><span data-stu-id="767e2-127">The [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method cancels asynchronous processing by immediately releasing the pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface and guarantees that the pointer is released before **CancelAsyncCall** returns.</span></span>

    <span data-ttu-id="767e2-128">Se você estiver usando um objeto wrapper implementando a interface **IUnsecured** para hospedar o [**IWbemObjectSink**](iwbemobjectsink.md), poderá encontrar algumas complicações adicionais.</span><span class="sxs-lookup"><span data-stu-id="767e2-128">If you are using a wrapper object implementing the **IUnsecured** interface to host [**IWbemObjectSink**](iwbemobjectsink.md), you may find some additional complications.</span></span> <span data-ttu-id="767e2-129">Como o aplicativo deve passar o mesmo ponteiro para [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) que foi passado na chamada assíncrona original, o aplicativo deve manter o objeto wrapper até ficar claro que o cancelamento não é necessário.</span><span class="sxs-lookup"><span data-stu-id="767e2-129">Because the application must pass the same pointer to [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) that was passed in the original asynchronous call, the application must hold on to the wrapper object until it becomes clear that cancellation is not required.</span></span> <span data-ttu-id="767e2-130">Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="767e2-130">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

7.  <span data-ttu-id="767e2-131">Quando terminar, limpe os ponteiros e desligue o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="767e2-131">When finished, clean up pointers and shut down the application.</span></span>

    <span data-ttu-id="767e2-132">O WMI fornece a chamada de status final por meio do método [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) .</span><span class="sxs-lookup"><span data-stu-id="767e2-132">WMI provides the final status call through the [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) method.</span></span>

    > [!Note]  
    > <span data-ttu-id="767e2-133">Depois de enviar a atualização de status final, o WMI libera o coletor de objeto chamando o método **Release** para a classe que implementa a interface [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="767e2-133">After sending the final status update, WMI releases the object sink by calling the **Release** method for the class that implements the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span> <span data-ttu-id="767e2-134">No exemplo anterior, trata-se do método **QuerySink:: Release** .</span><span class="sxs-lookup"><span data-stu-id="767e2-134">In the previous example, this is the **QuerySink::Release** method.</span></span> <span data-ttu-id="767e2-135">Se você quiser ter controle sobre o tempo de vida do objeto do coletor, poderá implementar o coletor com uma contagem de referência inicial de um (1).</span><span class="sxs-lookup"><span data-stu-id="767e2-135">If you want to have control over the lifetime of the sink object, you can implement the sink with an initial reference count of one (1).</span></span>

     

    <span data-ttu-id="767e2-136">Se um aplicativo cliente passar a mesma interface de coletor em duas chamadas assíncronas sobrepostas diferentes, o WMI não garantirá a ordem do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="767e2-136">If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback.</span></span> <span data-ttu-id="767e2-137">Um aplicativo cliente que faz chamadas assíncronas sobrepostas deve passar objetos de coletor diferentes ou serializar as chamadas.</span><span class="sxs-lookup"><span data-stu-id="767e2-137">A client application making overlapping asynchronous calls should either pass different sink objects or serialize the calls.</span></span>

<span data-ttu-id="767e2-138">O exemplo a seguir requer a referência a seguir e as \# instruções include.</span><span class="sxs-lookup"><span data-stu-id="767e2-138">The following example requires the following reference and \#include statements.</span></span>


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



<span data-ttu-id="767e2-139">O exemplo a seguir descreve como fazer uma consulta assíncrona usando o método [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) , mas não cria configurações de segurança nem libera o objeto [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="767e2-139">The following example describes how to make an asynchronous query using the [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, but does not create security settings or release the [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span> <span data-ttu-id="767e2-140">Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="767e2-140">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>


```C++
// Set input parameters to ExecQueryAsync.
BSTR QueryLang = SysAllocString(L"WQL");
BSTR Query = SysAllocString(L"SELECT * FROM MyClass");

// Create IWbemObjectSink object and set pointer.
QuerySink *pSink = new QuerySink;

IWbemServices* pSvc = 0;

// Call ExecQueryAsync.
HRESULT hRes = pSvc->ExecQueryAsync(QueryLang, 
                                    Query, 
                                    0, 
                                    NULL, 
                                    pSink);

// Check for errors.
if (hRes)
{
    printf("ExecQueryAsync failed with = 0x%X\n", hRes);
    SysFreeString(QueryLang);
    SysFreeString(Query);
    delete pSink;    
    return ERROR;
}
```



> [!Note]  
> <span data-ttu-id="767e2-141">O código acima não compila sem erro porque a classe **QuerySink** não foi definida.</span><span class="sxs-lookup"><span data-stu-id="767e2-141">The code above does not compile without error because the **QuerySink** class has not been defined.</span></span> <span data-ttu-id="767e2-142">Para obter mais informações sobre **QuerySink**, consulte [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="767e2-142">For more information about **QuerySink**, see [**IWbemObjectSink**](iwbemobjectsink.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="767e2-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="767e2-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="767e2-144">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="767e2-144">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
