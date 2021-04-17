---
description: O WMI fornece métodos na API COM e na API de script para obter informações ou manipular objetos em um sistema empresarial.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Chamando um método WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c327bbf0c4c90ad05d1c5026e3308e5fd8447aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770615"
---
# <a name="calling-a-wmi-method"></a>Chamando um método WMI

O WMI fornece métodos na [API com](com-api-for-wmi.md) e na [API de script](scripting-api-for-wmi.md) para obter informações ou manipular objetos em um sistema empresarial. Por exemplo, o método de script WMI [**SWbemServices.Execonsultas cQuery**](swbemservices-execquery.md) para dados. Os provedores também têm métodos definidos nas classes que registram. Os exemplos são os métodos do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) [**chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) e [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) fornecidos pelo [provedor do Win32](/windows/desktop/CIMWin32Prov/win32-provider).

As seções a seguir são discutidas neste tópico:

-   [Métodos WMI em comparação com métodos de provedor](#wmi-methods-compared-to-provider-methods)
-   [Modos de chamada de método no WMI](#method-calling-modes-in-wmi)
    -   [Modo síncrono](#synchronous-mode)
    -   [Modo assíncrono](#asynchronous-mode)
    -   [Modo de Semisynchronous](#semisynchronous-mode)
-   [Tópicos relacionados](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a>Métodos WMI em comparação com métodos de provedor

Usando as chamadas de [*método WMI*](gloss-w.md) combinadas com chamadas de [*método de provedor*](gloss-p.md) , você pode recuperar e manipular informações sobre sua empresa. Para obter mais informações, consulte [chamando um método WMI](calling-a-wmi-method.md) e [chamando um método de provedor](calling-a-provider-method.md).

Os métodos do objeto de script WMI [**SWbemObject**](swbemobject.md) têm um status especial, pois podem ser aplicados a qualquer classe de dados WMI. Para obter mais informações, consulte [scripts com SWbemObject](scripting-with-swbemobject.md).

O exemplo de código a seguir chama o WMI e os métodos de provedor.

Os seguintes métodos WMI e de provedor estão localizados na [API de script para o WMI](scripting-api-for-wmi.md):

-   **objWMIService.ExecQuery** chama o método de script WMI [ **SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   **objService. StopService ()** chama o método de provedor [ **Win32 \_ Service. StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)

Você pode pesquisar o código que pode aparecer em "Return" na seção de códigos de retorno do [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```


```PowerShell

$colServices= Get-WmiObject -Class Win32_Service -Filter 'Name = &quot;Alerter&quot;'
foreach ($objService in $colServices)
{
    $objService.StopService()
}
```





## <a name="method-calling-modes-in-wmi"></a>Modos de Method-Calling no WMI

O modo de chamada semisynchronous geralmente fornece o melhor equilíbrio entre segurança e desempenho.

Para obter mais informações sobre cada um dos modos possíveis, consulte o seguinte:

-   [Síncrono](#synchronous-mode)
-   [Assíncronos](#asynchronous-mode)
-   [Semisynchronous](#semisynchronous-mode)

### <a name="synchronous-mode"></a>Modo síncrono

O modo síncrono ocorre quando o programa ou os scripts pausa até que a chamada de método retorne um objeto de coleção [**SWbemObjectSet**](swbemobjectset.md) . O WMI cria essa coleção na memória antes de retornar o objeto de coleção para o programa ou script de chamada.

O modo síncrono pode ter um efeito adverso de desempenho de programa ou script no computador que executa o programa ou o script. Por exemplo, a recuperação síncrona de milhares de eventos do log de eventos pode levar muito tempo e usar muita memória porque o WMI cria um objeto de cada evento e coloca esses objetos em uma coleção antes de passar a coleção para o método.

Você só deve chamar métodos que não retornam conjuntos de dados grandes no modo síncrono. Os seguintes métodos [**SWbemServices**](swbemservices.md) podem ser chamados com segurança no modo síncrono:

-   [**SWbemServices. Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices. Get**](swbemservices-get.md)

Qualquer método [**SWbemServices**](swbemservices.md) sem a palavra, "Async" no nome pode ser chamado no modo síncrono, definindo o valor **WbemFlagReturnWhenComplete** no parâmetro *iFlags* .

### <a name="asynchronous-mode"></a>Modo assíncrono

O modo assíncrono ocorre quando o programa ou script continua a ser executado depois de chamar o método. O WMI retorna todos os objetos do método para um objeto [**SWbemSink**](swbemsink.md) , pois cada objeto é criado. O programa ou script de chamada deve ter um objeto **SWbemSink** e um manipulador de eventos [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) para processar os objetos retornados. Para obter mais informações sobre como criar um manipulador de eventos para o modo assíncrono, consulte [recebendo um evento WMI](receiving-a-wmi-event.md).

Embora esse modo não tenha o desempenho e a penalidade de recursos do modo síncrono, o modo assíncrono pode criar sérios riscos de segurança porque os resultados armazenados no objeto [**SWbemSink**](swbemsink.md) podem não vir do script ou programa de chamada. O WMI reduz o nível de autenticação no objeto **SWbemSink** até que o método tenha sucesso. Para obter mais informações sobre como mitigar esses riscos de segurança, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

Os métodos anexados à palavra Async são métodos para o modo assíncrono. Os métodos a seguir são chamadas assíncronas:

-   [**SWbemServices. AssociatorsOfAsync**](swbemservices-associatorsofasync.md)
-   [**SWbemServices. DeleteAsync**](swbemservices-deleteasync.md)
-   [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
-   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)
-   [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)
-   [**SWbemServices. InstancesOfAsync**](swbemservices-instancesofasync.md)
-   [**SWbemServices. ReferencesToAsync**](swbemservices-referencesto.md)
-   [**SWbemServices. SubclassesOfAsync**](swbemservices-subclassesofasync.md)

Para obter mais informações sobre o modo assíncrono, consulte:

-   [Fazendo uma chamada assíncrona com C++](making-an-asynchronous-call-with-c--.md)
-   [Fazendo uma chamada assíncrona com o VBScript](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a>Modo de Semisynchronous

O modo Semisynchronous é semelhante ao modo assíncrono no qual o programa ou script continua a ser executado depois de chamar o método. No modo semisynchronous, o WMI recupera os objetos em segundo plano à medida que seu script ou programa continua a ser executado. O WMI retorna cada objeto retornado ao método de chamada logo após a criação do objeto.

Como o WMI gerencia o objeto, o modo semisynchronous é mais seguro do que o modo assíncrono. No entanto, se você usar o modo semisynchronous com mais de 1.000 instâncias, a recuperação da instância poderá monopolizar os recursos disponíveis, o que pode prejudicar o desempenho do programa ou do script e do computador usando o programa ou script. Cada objeto ocupará os recursos necessários até que a memória seja liberada.

Para contornar essa condição, você pode chamar o método com o parâmetro *iFlags* definido com os sinalizadores **wbemFlagForwardOnly** e **WBEMFLAGRETURNIMMEDIATELY** para instruir o WMI a retornar um [**SWbemObjectSet**](swbemobjectset.md)somente de encaminhamento. Um **SWbemObjectSet** somente de encaminhamento elimina o problema de desempenho causado por um grande conjunto de dados liberando a memória depois que o objeto é enumerado.

Qualquer método [**SWbemServices**](swbemservices.md) que não pode ser chamado no modo síncrono ou assíncrono é chamado no modo semisynchronous.

Os métodos a seguir são chamados no modo semisynchronous:

-   [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices. Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices. Get**](swbemservices-get.md)
-   [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)
-   [**SWbemServices. References**](swbemservices-referencesto.md)
-   [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)
-   [**SWbemServices. put**](swbemservicesex-put.md)

Para obter mais informações sobre o modo semisynchronous, consulte [fazendo uma chamada semisynchronous com C++](making-a-semisynchronous-call-with-c--.md) e [fazendo uma chamada de Semisynchronous com o VBScript](making-a-semisynchronous-call-with-vbscript.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Melhorando o desempenho da enumeração](improving-enumeration-performance.md)
</dt> <dt>

[Criando scripts com SWbemObject](scripting-with-swbemobject.md)
</dt> <dt>

[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 
