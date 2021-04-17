---
description: A notificação de eventos assíncronos é uma técnica que permite que um aplicativo monitore constantemente os eventos sem monopolizar os recursos do sistema.
ms.assetid: 69ec8ead-9073-4689-bc66-5134728ab147
ms.tgt_platform: multiple
title: Recebendo notificações de eventos assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d883908475c796a6bcf31895f2928345541c940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748889"
---
# <a name="receiving-asynchronous-event-notifications"></a>Recebendo notificações de eventos assíncronos

A notificação de eventos assíncronos é uma técnica que permite que um aplicativo monitore constantemente os eventos sem monopolizar os recursos do sistema. As notificações de eventos assíncronos têm as mesmas limitações de segurança que outras chamadas assíncronas têm. Em vez disso, você pode fazer chamadas semisynchronous. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

A fila de eventos assíncronos roteados para um cliente tem o potencial de crescer excepcionalmente grande. Portanto, o WMI implementa uma política de todo o sistema para evitar ficar sem memória. O WMI torna os eventos lentos ou começa a descartar eventos da fila quando a fila cresce além de um determinado tamanho.

O WMI usa as propriedades [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) e [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) da classe [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) para definir limites para evitar memória insuficiente. O valor mínimo indica quando o WMI deve iniciar a lentidão na notificação de eventos e o valor máximo indica quando iniciar a descartar eventos. Os valores padrão para os limites baixo e alto são 1 milhão (10 MB) e 2 milhões (20 MB). Além disso, você pode definir a propriedade [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) para descrever a quantidade de tempo que o WMI deve aguardar antes de remover eventos. O valor padrão para **MaxWaitOnEvents** é 2000 ou 2 segundos.

## <a name="receiving-asynchronous-event-notifications-in-vbscript"></a>Recebendo notificações de eventos assíncronos no VBScript

As chamadas de script para receber notificações de eventos são essencialmente as mesmas que todas as chamadas assíncronas com os mesmos problemas de segurança. Para obter mais informações, consulte [fazendo uma chamada assíncrona com o VBScript](making-an-asynchronous-call-with-vbscript.md).

**Para receber notificações de eventos assíncronas no VBScript**

1.  Crie um objeto de coletor chamando [WScript. CreateObject](/previous-versions//xzysf6hc(v=vs.85)) e especificando o ProgID de "WbemScripting" e o tipo de objeto de [**SWbemSink**](swbemsink.md). O objeto Sink recebe as notificações.
2.  Escreva uma sub-rotina para cada evento que você deseja manipular. A tabela a seguir lista os eventos [**SWbemSink**](swbemsink.md) .

    

    | Evento                                            | Significado                                                                                                                         |
    |--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
    | [**OnObjectReady**](swbemsink-onobjectready.md) | Relata os retornos de um objeto para o coletor. O uso dessa chamada retorna um objeto cada vez até que a operação seja concluída.     |
    | [**OnCompleted**](swbemsink-oncompleted.md)     | Relata quando uma chamada assíncrona é concluída. Esse evento nunca ocorrerá se a operação estiver indefinida.                          |
    | [**OnObjectPut**](swbemsink-onobjectput.md)     | Relata a conclusão de uma operação Put assíncrona. Esse evento retorna o caminho do objeto da instância ou da classe salva. |
    | [**OnProgress**](swbemsink-onprogress.md)       | Relata o status de uma chamada assíncrona que está em andamento. Nem todos os provedores dão suporte a relatórios de progresso provisório.             |
    | [**Cancelar**](swbemsink-cancel.md)               | Cancela todas as operações assíncronas pendentes associadas a este coletor de objeto.                                        |

    

     

O exemplo de código VBScript a seguir notifica a exclusão de processos com um intervalo de sondagem de 10 segundos. Nesse script, o coletor de sub-rotina \_ OnObjectReady manipula a ocorrência do evento. No exemplo, o objeto Sink é denominado "Sink", no entanto, você pode nomear esse objeto conforme escolher.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, _
    "SELECT * FROM __InstanceDeletionEvent" _
    & " WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'"


WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "__InstanceDeletionEvent event has occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="receiving-asynchronous-event-notifications-in-c"></a>Recebendo notificações de eventos assíncronos em C++

Para executar uma notificação assíncrona, você cria um thread separado exclusivamente para monitorar e receber eventos de Instrumentação de Gerenciamento do Windows (WMI). Quando esse thread recebe uma mensagem, o thread notifica seu aplicativo principal.

Ao dedicar um thread separado, você permite que seu processo principal execute outras atividades enquanto aguarda a chegada de um evento. A entrega assíncrona de notificações melhora o desempenho, mas pode fornecer menos segurança do que o desejado. Em C++, você tem a opção de usar a interface [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) ou executar verificações de acesso em descritores de segurança. Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

**Para configurar notificações de eventos assíncronos**

1.  Antes de inicializar qualquer notificação assíncrona, verifique se os parâmetros de prevenção de memória insuficiente estão definidos corretamente no [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).

2.  Determine que tipo de eventos você deseja receber.

    O WMI dá suporte a eventos intrínsecos e extrínsecos. Um evento intrínseco é um evento predefinido pelo WMI, enquanto um evento extrínsecos é um evento definido por um provedor de terceiros. Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).

O procedimento a seguir descreve como receber notificações de eventos assíncronos em C++.

**Para receber notificações de eventos assíncronos em C++**

1.  Configure seu aplicativo com chamadas para as funções [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

    Chamar [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) inicializa com, enquanto [**COINITIALIZESECURITY**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) concede ao WMI a permissão para chamar o processo do consumidor. A função **CoInitializeEx** também concede a capacidade de programar um aplicativo multithread, que é necessário para a notificação assíncrona. Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).

    O código neste tópico requer as seguintes referências e \# inclui instruções para compilar corretamente.

    ```C++
    #define _WIN32_DCOM
    #include <iostream>
    using namespace std;
    #include <wbemidl.h>
    ```

    

    O exemplo de código a seguir descreve como configurar o consumidor de evento temporário com chamadas para [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    ```C++
    void main(int argc, char **argv)
    {
        HRESULT hr = 0;
        hr = CoInitializeEx (0, COINIT_MULTITHREADED);
        hr = CoInitializeSecurity (NULL, 
           -1, 
           NULL, 
           NULL,   
           RPC_C_AUTHN_LEVEL_NONE, 
           RPC_C_IMP_LEVEL_IMPERSONATE, 
           NULL,
           EOAC_NONE,
           NULL); 

        if (FAILED(hr))
        {
           CoUninitialize();
           cout << "Failed to initialize security. Error code = 0x"
               << hex << hr << endl;
           return;
        }

    // ...
    }
    ```

    

2.  Crie um objeto de coletor por meio da interface [**IWbemObjectSink**](iwbemobjectsink.md) .

    O WMI usa [**IWbemObjectSink**](iwbemobjectsink.md) para enviar notificações de eventos e relatar o status em uma operação assíncrona ou notificação de eventos.

3.  Registre seu consumidor de evento com uma chamada para o método [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .

    Certifique-se de que o parâmetro *pResponseHandler* aponta para o objeto de coletor criado na etapa anterior.

    A finalidade do registro é receber apenas as notificações necessárias. O recebimento de notificações supérfluas desperdiça o tempo de processamento e de entrega; e não usa a capacidade de filtragem do WMI para o potencial máximo.

    No entanto, um consumidor temporário pode receber mais de um tipo de evento. Nesse caso, um consumidor temporário deve fazer chamadas separadas para [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) para cada tipo de evento. Por exemplo, um consumidor pode exigir notificação quando novos processos são criados (um evento de criação de instância ou [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) e para alterações em determinadas chaves do registro (um evento de registro, como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)). Portanto, o consumidor faz uma chamada para [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) para registrar eventos de criação de instância e outra chamada para **ExecNotificationQueryAsync** para registrar eventos de registro.

    Se você optar por criar um consumidor de eventos que se registra para vários eventos, evite registrar várias classes com o mesmo coletor. Em vez disso, use um coletor separado para cada classe de evento registrado. Ter um coletor dedicado simplifica o processamento e ajuda na manutenção, permitindo que você cancele um registro sem afetar os outros.

4.  Execute as atividades necessárias em seu consumidor de eventos.

    Essa etapa deve conter a maior parte do seu código e incluir atividades como exibir eventos em uma interface do usuário.

5.  Quando terminar, cancele o registro do consumidor de evento temporário com uma chamada para o evento [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .

    Independentemente de a chamada para [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) ter êxito ou falhar, não exclua o objeto de coletor até que a contagem de referência de objeto chegue a zero. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

 
