---
description: Uma consulta assíncrona, embora seja um pouco mais complexa de escrever, é o tipo preferencial de consulta quando o desempenho do sistema ou da rede é afetado pela consulta de um grande grupo de dados.
ms.assetid: b382610a-dac9-4d31-b756-aa84d16f0234
ms.tgt_platform: multiple
title: Invocando uma consulta assíncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a0e297c6a1955d0006d888fc95f5e827f5cb75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837253"
---
# <a name="invoking-an-asynchronous-query"></a><span data-ttu-id="a0192-103">Invocando uma consulta assíncrona</span><span class="sxs-lookup"><span data-stu-id="a0192-103">Invoking an Asynchronous Query</span></span>

<span data-ttu-id="a0192-104">Uma consulta assíncrona, embora seja um pouco mais complexa de escrever, é o tipo preferencial de consulta quando o desempenho do sistema ou da rede é afetado pela consulta de um grande grupo de dados.</span><span class="sxs-lookup"><span data-stu-id="a0192-104">An asynchronous query, while somewhat more complex to write, is the preferred type of query when system or network performance will be affected by querying a large group of data.</span></span> <span data-ttu-id="a0192-105">No script, criar um objeto [**SWbemSink**](swbemsink.md) e sub-rotinas para manipular os eventos que o coletor pode receber são as únicas tarefas adicionais além da consulta básica.</span><span class="sxs-lookup"><span data-stu-id="a0192-105">In script, creating an [**SWbemSink**](swbemsink.md) object and subroutines to handle the events that the sink could receive are the only additional tasks beyond the basic query.</span></span>

> [!Note]  
> <span data-ttu-id="a0192-106">Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a0192-106">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="a0192-107">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="a0192-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="a0192-108">As seguintes consultas de script abreviadas para todos os arquivos de dados no computador local.</span><span class="sxs-lookup"><span data-stu-id="a0192-108">The following abbreviated script queries for all of the data files on the local machine.</span></span> <span data-ttu-id="a0192-109">Essa consulta pode levar um tempo excessivo se tiver sido executada para todos os computadores em uma rede.</span><span class="sxs-lookup"><span data-stu-id="a0192-109">This query could take an excessive amount of time if it were executed for all of the machines on a network.</span></span> <span data-ttu-id="a0192-110">Um objeto [**SWbemSink**](swbemsink.md) é configurado e o único evento que é manipulado é o evento OnCompleted.</span><span class="sxs-lookup"><span data-stu-id="a0192-110">An [**SWbemSink**](swbemsink.md) object is set up and the only event that is handled is the OnCompleted event.</span></span>


```VB
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
    WScript.Echo "Asynchronous operation is done."
End Sub

Set service = GetObject("winmgmts:")
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
service.ExecQueryAsync sink, "SELECT * FROM Win32_DataFile"
WScript.Echo "Waiting for instances."
sink.Cancel()
set sink= Nothing
```



<span data-ttu-id="a0192-111">Para obter informações detalhadas sobre como construir chamadas de método assíncronos no script, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="a0192-111">For detailed information about constructing asynchronous method calls in script, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="a0192-112">Em aplicativos C++, uma consulta assíncrona gera um processo separado para receber dados de consulta.</span><span class="sxs-lookup"><span data-stu-id="a0192-112">In C++ applications, an asynchronous query spawns a separate process to receive query data.</span></span> <span data-ttu-id="a0192-113">Uma consulta assíncrona é mais complexa do que uma consulta síncrona, pois você deve codificar um aplicativo multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="a0192-113">An asynchronous query is more complex than a synchronous query, as you must code a multithreaded application.</span></span> <span data-ttu-id="a0192-114">No entanto, uma consulta assíncrona não monopoliza o thread principal do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a0192-114">However, an asynchronous query does not monopolize the main thread of your application.</span></span>

<span data-ttu-id="a0192-115">O procedimento a seguir descreve como executar uma consulta assíncrona em C++.</span><span class="sxs-lookup"><span data-stu-id="a0192-115">The following procedure describes how to perform an asynchronous query in C++.</span></span>

<span data-ttu-id="a0192-116">**Para executar uma consulta assíncrona em C++**</span><span class="sxs-lookup"><span data-stu-id="a0192-116">**To perform an asynchronous query in C++**</span></span>

1.  <span data-ttu-id="a0192-117">Implemente um objeto **IWbemSink** .</span><span class="sxs-lookup"><span data-stu-id="a0192-117">Implement an **IWbemSink** object.</span></span>

    <span data-ttu-id="a0192-118">Um objeto **IWbemSink** recebe informações sobre uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a0192-118">An **IWbemSink** object receives information about an asynchronous operation.</span></span>

2.  <span data-ttu-id="a0192-119">Descreva sua consulta em uma chamada para [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).</span><span class="sxs-lookup"><span data-stu-id="a0192-119">Describe your query in a call to [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).</span></span>

    <span data-ttu-id="a0192-120">O WMI move imediatamente o processo que consulta o CIM para outro thread e libera o thread que executou a consulta para outra tarefa.</span><span class="sxs-lookup"><span data-stu-id="a0192-120">WMI immediately moves the process that queries the CIM to another thread and frees up the thread that executed the query for another task.</span></span>

3.  <span data-ttu-id="a0192-121">Aguarde até que o WMI chame o método [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .</span><span class="sxs-lookup"><span data-stu-id="a0192-121">Wait for WMI to call the [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) method.</span></span>

    <span data-ttu-id="a0192-122">Quando terminar, as chamadas WMI [**indicam**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) que o aplicativo foi concluído para a conclusão da consulta.</span><span class="sxs-lookup"><span data-stu-id="a0192-122">When finished, WMI calls [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) to signal your application that the query is complete.</span></span> <span data-ttu-id="a0192-123">O WMI também retorna os resultados da consulta para o coletor como um ponteiro para um ponteiro de interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="a0192-123">WMI also returns results of the query to the sink as a pointer to an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface pointer.</span></span> <span data-ttu-id="a0192-124">Assim como com uma consulta síncrona, use o ponteiro para acessar os objetos que compõem o resultado da consulta.</span><span class="sxs-lookup"><span data-stu-id="a0192-124">As with a synchronous query, use the pointer to access the objects that make up the result of your query.</span></span>

<span data-ttu-id="a0192-125">O exemplo de código a seguir não compila sem erro porque a classe QuerySink não foi definida.</span><span class="sxs-lookup"><span data-stu-id="a0192-125">The following code example does not compile without an error because the class QuerySink has not been defined.</span></span> <span data-ttu-id="a0192-126">Para obter a definição da classe QuerySink, consulte [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="a0192-126">For the definition of the QuerySink class, see [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="a0192-127">O exemplo de código também requer a referência a seguir e as \# instruções include.</span><span class="sxs-lookup"><span data-stu-id="a0192-127">The code example also requires the following reference and \#include statements.</span></span>


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



<span data-ttu-id="a0192-128">O exemplo de código a seguir mostra como fazer uma chamada assíncrona para emitir uma consulta.</span><span class="sxs-lookup"><span data-stu-id="a0192-128">The following code example shows how to make an asynchronous call to issue a query.</span></span>


```C++
void ExecQuery(IWbemServices *pSvc)
{
    // Create a new sink object.
    QuerySink *pSink = new QuerySink;

    // Initialize the query and query language.
    BSTR strQuery = SysAllocString(L"SELECT * FROM ClassName");
    BSTR strQueryLang = SysAllocString(L"WQL");
    
    // Issue the query.
    HRESULT hRes = pSvc->ExecQueryAsync(strQueryLang, strQuery, 0,
        NULL, pSink);

    // Clean up.
    SysFreeString(strQuery);
    SysFreeString(strQueryLang);
    
    if (hRes)
    {
        printf("ExecQueryAsync failed with = 0x%X\n", hRes);
        return;
    }
    
    printf("Completed.\n");
}
```



<span data-ttu-id="a0192-129">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="a0192-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 



