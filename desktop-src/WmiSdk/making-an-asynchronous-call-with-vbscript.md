---
description: Fazer uma chamada assíncrona para um método WMI ou um método de provedor permite que um script continue em execução enquanto os objetos retornam a um objeto SWbemSink e são tratados por métodos como SWbemSink.OnObjectReady.
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: Fazendo uma chamada assíncrona com VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee8c4737ff7513441532275e24f2cfe20f8e30fa2932e854cc566eb032c49d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555128"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a>Fazendo uma chamada assíncrona com VBScript

Fazer uma chamada assíncrona para um [](gloss-p.md) método [*WMI*](gloss-w.md) ou um método de provedor permite que um script continue em execução enquanto os objetos retornam a um objeto [**SWbemSink**](swbemsink.md) e são tratados por métodos como [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md). No entanto, chamadas assíncronas não são recomendadas porque os dados podem não ser retornados no mesmo nível de segurança que a chamada é feita.

Ao usar chamadas de sink assíncronas como [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) para obter dados retornados, você pode definir o valor do Registro a seguir.

**HKEY \_ SOFTWARE \_ DO** COMPUTADOR LOCAL \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault**

Definir esse valor do Registro garante a autenticação dos objetos de dados retornados ao sink. Se **UnsecAppAccessControlDefault** for definido como um (1), o WMI executará a verificação de acesso do retorno de dados. Verificações de acesso verificam se os dados vêm da origem correta. Para obter mais informações, consulte [Configurando a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

Métodos assíncronos com nomes que terminam em "Assíncrono" sempre retornam imediatamente após serem chamados para que um programa possa \_ continuar em execução. Por exemplo, [**SWbemServices.ExecQuery**](swbemservices-execquery.md) é síncrono e bloqueia a execução até que todos os objetos sejam retornados. O [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) é a versão assíncrona não desbloqueada. Uma maneira mais segura de fazer a chamada **paraSWbemServices.ExecQuery** não bloqueado é fazendo a chamada de forma [*semissíncrona.*](gloss-s.md) Para obter mais informações, consulte [Configurando a](setting-security-on-an-asynchronous-call.md) segurança em uma chamada assíncrona e Fazendo uma chamada [semisíncrona com o VBScript.](making-a-semisynchronous-call-with-vbscript.md)

O *parâmetro iFlags* para chamadas assíncronas sempre assume como padrão zero (0). Métodos assíncronos não fornecem uma [**coleção SWbemObjectSet**](swbemobjectset.md) para a sub-rotina do sink. Em vez disso, a sub-rotina de evento [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) em seu script ou aplicativo recebe cada objeto conforme ele é fornecido.

Quando a chamada assíncrona original é concluída, ela chama o evento [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) do sink do objeto e executa o código que você coloca lá para processar o resultado da chamada.

> [!Note]  
> Uma asp (página de Active Server) como um host de script não dá suporte a uma chamada assíncrona.

 

O procedimento a seguir descreve como fazer uma chamada assíncrona usando o VBScript.

**Para fazer uma chamada assíncrona usando VBScript**

1.  Conexão para WMI e obter um [**objeto SWbemServices.**](swbemservices.md)

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  Crie o sink de objeto usando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) ou (somente para Windows Host de Script 2.0) a marca OBJECT com um atributo de eventos definido como **TRUE.**

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    -ou-

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  Crie uma sub-rotina para cada evento que um evento assíncrono possa disparar. Esses eventos são definidos como métodos [**em SWbemObject**](swbemobject.md). Por exemplo, o WMI faz um retorno de chamada para [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) conforme cada instância retorna.

    Ao criar a sub-rotina, coloque o código na sub-rotina para manipular cada evento quando ele for recebido.

    ```VB
    Sub SINK_OnCompleted(
          iHResult, 
          objErrorObject, 
          objAsyncContext
          )
        WScript.Echo "Asynchronous operation is done."
    End Sub

    Sub SINK_OnObjectReady(objObject, objAsyncContext)
        WScript.Echo (objObject.Name)
    End Sub
    ```

    

    Examine o *parâmetro iHresult* retornado pelo [**evento OnCompleted**](swbemsink-oncompleted.md) para determinar se a chamada assíncrona foi bem-sucedida ou se ocorreu um erro. Se for bem-sucedido, o valor passado no parâmetro *iHresult* será igual a zero (0). Qualquer outro valor pode indicar um erro e você deve verificar os valores no objeto de erro retornado no *parâmetro objErrorObject.*

4.  Faça uma chamada assíncrona e passe o nome do seu sink no parâmetro *objWbemSink.*

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  Faça uma chamada que impeça que o script seja encerrado antes que todos os eventos sejam recebidos. Se o script puder ser executado com uma interface de tela, uma maneira simples de fazer isso é usar um comando WSH (Host de Script Windows), que é mostrado no exemplo a `Echo` seguir.

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    Ao executar esse script, você poderá ver a primeira instância retornar antes da mensagem Aguardando **instâncias** ou poderá vê-la depois. Essa é a natureza do processamento assíncrono. Se você fechar a **caixa de mensagem Aguardando instâncias** muito em breve, talvez não veja todas as instâncias.

6.  Se você tiver resultados de várias chamadas assíncronas diferentes retornando para o mesmo sink, armazene todos os dados de distinção necessários no parâmetro de contexto *objWbemAsyncContext.*

7.  Quando terminar com o sink, cancele sua chamada assíncrona com o [**método Cancel.**](swbemsink-cancel.md)

    ```VB
    objwbemsink.Cancel()
    ```

    

    O [**método Cancel**](swbemsink-cancel.md) instrui o WSH a cancelar todas as chamadas assíncronas associadas a um determinado objeto de sink. Portanto, talvez você queira usar os sinks separados para operações assíncronas que devem ser independentes.

8.  Libere o objeto de sink atribuindo o objeto de sink a `Nothing` .

    ```VB
    set objwbemsink= Nothing
    ```

    

O exemplo de código a seguir mostra uma consulta assíncrona para todas as instâncias do [**Processo Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) no computador local. Para uma versão síncrona do mesmo método, consulte [Chamando um método](calling-a-method.md).


```VB
' Create an object sink
set oSink = WScript.CreateObject("wbemscripting.swbemsink","sink_")
' Connect to WMI and the cimv2 namespace, and obtain
' an SWbemServices object
set oSvc = GetObject("winmgmts:root\cimv2")

bdone = false
' Query for all Win32_Process objects
osvc.ExecQueryAsync oSink, "SELECT Name FROM Win32_Process"
' Wait until all instances are returned. 
' The bdone flag prevents the script from exiting until
' the sink.OnCompleted subroutine is executed when
' all the objects are returned.
while not bdone    
    wscript.sleep 1000
wend

' The sink subroutine to handle the OnObjectReady 
' event. This is called as each object returns.
sub sink_OnObjectReady(oInst, octx)
    WScript.Echo "Got Instance: " & oInst.Name
end sub
' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned. 
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "ExecQueryAsync completed"
    bdone = true
end sub
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chamando um método](calling-a-method.md)
</dt> <dt>

[Mantendo a segurança WMI](maintaining-wmi-security.md)
</dt> </dl>

 

 
