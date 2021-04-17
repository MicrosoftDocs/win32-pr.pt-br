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
# <a name="making-an-asynchronous-call-with-c"></a>Fazendo uma chamada assíncrona com C++

Os aplicativos WMI escritos em C++ podem fazer chamadas assíncronas usando muitos dos métodos da interface com de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . No entanto, o procedimento recomendado para chamar um [*método WMI*](gloss-w.md) ou um [*método de provedor*](gloss-p.md) é usar chamadas semisynchronous porque chamadas semisynchronous são mais seguras do que chamadas assíncronas. Para obter mais informações, consulte [fazendo uma chamada Semisynchronous com C++](making-a-semisynchronous-call-with-c--.md) e [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

O procedimento a seguir descreve como fazer uma chamada assíncrona usando o coletor em seu processo.

**Para fazer uma chamada assíncrona usando C++**

1.  Implemente a interface [**IWbemObjectSink**](iwbemobjectsink.md) .

    Todos os aplicativos que fazem chamadas assíncronas devem implementar [**IWbemObjectSink**](iwbemobjectsink.md). Os consumidores de eventos temporários também implementam **IWbemObjectSink** para receber notificações de eventos.

2.  Faça logon no namespace WMI de destino.

    Os aplicativos sempre precisam chamar a função COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) durante a fase de inicialização. Se eles não fizerem isso antes de fazer uma chamada assíncrona, o WMI liberará o coletor de aplicativos sem concluir a chamada assíncrona. Para obter mais informações, consulte [Inicializando com para um aplicativo WMI](initializing-com-for-a-wmi-application.md).

3.  Defina a segurança para o coletor.

    As chamadas assíncronas criam uma variedade de problemas de segurança com os quais você pode ter que lidar, por exemplo, permitindo o acesso de WMI ao seu aplicativo. Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

4.  Faça a chamada assíncrona.

    O método retorna imediatamente com o código de falha de **\_ \_ \_ erro WBEM S** . O aplicativo pode continuar com outras tarefas enquanto aguarda a conclusão da operação. Os relatórios WMI de volta para o aplicativo chamando métodos na implementação [**IWbemObjectSink**](iwbemobjectsink.md) do seu aplicativo.

5.  Se necessário, verifique sua implementação periodicamente para obter atualizações.

    Os aplicativos podem receber a notificação do status intermediário definindo o parâmetro *lFlags* na chamada assíncrona para o **\_ sinalizador WBEM \_ Enviar \_ status**. O WMI relata o status de sua chamada definindo o parâmetro *lFlags* de [**IWbemObjectSink**](iwbemobjectsink.md) para **o \_ \_ progresso do status do WBEM**.

6.  Se necessário, você pode cancelar a chamada antes de o WMI concluir o processamento chamando o método [**IWbemServices:: CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .

    O método [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) cancela o processamento assíncrono, liberando imediatamente o ponteiro para a interface [**IWbemObjectSink**](iwbemobjectsink.md) e garante que o ponteiro seja liberado antes que **CancelAsyncCall** seja retornado.

    Se você estiver usando um objeto wrapper implementando a interface **IUnsecured** para hospedar o [**IWbemObjectSink**](iwbemobjectsink.md), poderá encontrar algumas complicações adicionais. Como o aplicativo deve passar o mesmo ponteiro para [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) que foi passado na chamada assíncrona original, o aplicativo deve manter o objeto wrapper até ficar claro que o cancelamento não é necessário. Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

7.  Quando terminar, limpe os ponteiros e desligue o aplicativo.

    O WMI fornece a chamada de status final por meio do método [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) .

    > [!Note]  
    > Depois de enviar a atualização de status final, o WMI libera o coletor de objeto chamando o método **Release** para a classe que implementa a interface [**IWbemObjectSink**](iwbemobjectsink.md) . No exemplo anterior, trata-se do método **QuerySink:: Release** . Se você quiser ter controle sobre o tempo de vida do objeto do coletor, poderá implementar o coletor com uma contagem de referência inicial de um (1).

     

    Se um aplicativo cliente passar a mesma interface de coletor em duas chamadas assíncronas sobrepostas diferentes, o WMI não garantirá a ordem do retorno de chamada. Um aplicativo cliente que faz chamadas assíncronas sobrepostas deve passar objetos de coletor diferentes ou serializar as chamadas.

O exemplo a seguir requer a referência a seguir e as \# instruções include.


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



O exemplo a seguir descreve como fazer uma consulta assíncrona usando o método [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) , mas não cria configurações de segurança nem libera o objeto [**IWbemObjectSink**](iwbemobjectsink.md) . Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).


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
> O código acima não compila sem erro porque a classe **QuerySink** não foi definida. Para obter mais informações sobre **QuerySink**, consulte [**IWbemObjectSink**](iwbemobjectsink.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chamando um método](calling-a-method.md)
</dt> </dl>

 

 
