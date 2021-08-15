---
description: Uma consulta assíncrona, embora seja um pouco mais complexa de escrever, é o tipo preferencial de consulta quando o desempenho do sistema ou da rede é afetado pela consulta de um grande grupo de dados.
ms.assetid: b382610a-dac9-4d31-b756-aa84d16f0234
ms.tgt_platform: multiple
title: Invocando uma consulta assíncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ae188e3826562b1de68357db34dca6cea60a40e4be07c16946b13ed3eb3007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993066"
---
# <a name="invoking-an-asynchronous-query"></a>Invocando uma consulta assíncrona

Uma consulta assíncrona, embora seja um pouco mais complexa de escrever, é o tipo preferencial de consulta quando o desempenho do sistema ou da rede é afetado pela consulta de um grande grupo de dados. No script, criar um objeto [**SWbemSink**](swbemsink.md) e sub-rotinas para manipular os eventos que o coletor pode receber são as únicas tarefas adicionais além da consulta básica.

> [!Note]  
> Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

As seguintes consultas de script abreviadas para todos os arquivos de dados no computador local. Essa consulta pode levar um tempo excessivo se tiver sido executada para todos os computadores em uma rede. Um objeto [**SWbemSink**](swbemsink.md) é configurado e o único evento que é manipulado é o evento OnCompleted.


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



Para obter informações detalhadas sobre como construir chamadas de método assíncronos no script, consulte [chamando um método](calling-a-method.md).

Em aplicativos C++, uma consulta assíncrona gera um processo separado para receber dados de consulta. Uma consulta assíncrona é mais complexa do que uma consulta síncrona, pois você deve codificar um aplicativo multi-threaded. No entanto, uma consulta assíncrona não monopoliza o thread principal do seu aplicativo.

O procedimento a seguir descreve como executar uma consulta assíncrona em C++.

**Para executar uma consulta assíncrona em C++**

1.  Implemente um objeto **IWbemSink** .

    Um objeto **IWbemSink** recebe informações sobre uma operação assíncrona.

2.  Descreva sua consulta em uma chamada para [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).

    O WMI move imediatamente o processo que consulta o CIM para outro thread e libera o thread que executou a consulta para outra tarefa.

3.  Aguarde até que o WMI chame o método [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .

    Quando terminar, as chamadas WMI [**indicam**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) que o aplicativo foi concluído para a conclusão da consulta. O WMI também retorna os resultados da consulta para o coletor como um ponteiro para um ponteiro de interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) . Assim como com uma consulta síncrona, use o ponteiro para acessar os objetos que compõem o resultado da consulta.

O exemplo de código a seguir não compila sem erro porque a classe QuerySink não foi definida. Para obter a definição da classe QuerySink, consulte [**IWbemObjectSink**](iwbemobjectsink.md). O exemplo de código também requer a referência a seguir e as \# instruções include.


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



O exemplo de código a seguir mostra como fazer uma chamada assíncrona para emitir uma consulta.


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



Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

 



