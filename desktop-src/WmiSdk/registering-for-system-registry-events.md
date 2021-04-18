---
description: Para receber notificações do provedor de registro do sistema, um aplicativo de gerenciamento deve ser registrado como um consumidor de evento temporário.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Registrando para eventos de registro do sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 886046f5ffef366cdba2efb86629019f2ee0b5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810855"
---
# <a name="registering-for-system-registry-events"></a>Registrando para eventos de registro do sistema

Para receber notificações do provedor de [registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) , um aplicativo de gerenciamento deve ser registrado como um consumidor de evento temporário. A maioria dos requisitos de registro para o provedor de registro do sistema é igual a qualquer outro registro de evento, exceto que você também deve executar o procedimento a seguir.

O provedor de registro fornece classes de evento para eventos no registro do sistema. Para obter mais informações sobre o registro de eventos gerais, consulte [recebendo um evento WMI](receiving-a-wmi-event.md).

O procedimento a seguir descreve como registrar-se para eventos de registro do sistema.

**Para registrar-se para eventos de registro do sistema**

1.  Chamar um método de consulta de notificação.

    Em script ou C++, use uma consulta de notificação como [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) ou [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync). Crie uma cadeia de caracteres de consulta para o parâmetro *bstrQuery* de **IWbemServices:: ExecNotificationQueryAsync** ou *strQuery* no script.

2.  Determine o tipo de evento que você deseja receber e crie a consulta.

    A tabela a seguir lista as classes de evento do registro que você pode usar.

    

    | Classe de eventos                                                      | Localização do hive        | Descrição                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent)                       | N/D<br/>       | Classe base abstrata para alterações no registro.<br/> |
    | [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | RootPath<br/>  | Monitora as alterações em uma hierarquia de chaves.<br/>         |
    | [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | KeyPath<br/>   | Monitora as alterações em uma única chave.<br/>                |
    | [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | ValueName<br/> | Monitora as alterações em um único valor.<br/>              |

    

     

    Essas classes têm uma propriedade chamada **Hive** que identifica a hierarquia de chaves a ser monitorada para alteração, como **HKEY \_ local \_ Machine**.

    As alterações nas **seções hKey \_ classes \_ raiz** e **HKEY \_ Current \_ User** não são suportadas por [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) ou classes derivadas dela, como [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).

3.  Crie a cláusula WHERE para o registro do evento.

    O provedor de registro do sistema tem regras específicas para cláusulas WHERE. Para obter mais informações, consulte [criando uma cláusula WHERE apropriada para o provedor de registro](creating-a-proper-where-clause-for-the-registry-provider.md). Para obter mais informações gerais sobre como criar uma cláusula WHERE, consulte [consultando com WQL](querying-with-wql.md).

4.  Determine se o consumidor está recebendo eventos.

    O provedor de registro do sistema não garante que todos os eventos enviados sejam entregues. Para obter mais informações, consulte [recebendo eventos do registro](receiving-registry-events.md).

O exemplo de código VBScript a seguir mostra como detectar uma alteração no registro no software da **\_ \_ máquina local hKey** \\  \\ **Microsoft** Hive ou Subtree. Esse é um script de monitoramento que, para fins de demonstração, é executado em um processo chamado Wscript.exe até que seja encerrado no **Gerenciador de tarefas**, o WMI seja interrompido ou o sistema operacional seja reinicializado. O script usa uma chamada [*semisynchronous*](gloss-s.md) para [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md). Para obter mais informações sobre chamadas semisynchronous, consulte [fazendo uma chamada semisynchronous com o VBScript](making-a-semisynchronous-call-with-vbscript.md).


```VB
Set wmiServices = GetObject("winmgmts:root/default") 
Set colTreeChanges = wmiServices.ExecNotificationQuery _
    ("SELECT * FROM RegistryTreeChangeEvent " _
    & "WHERE Hive='HKEY_LOCAL_MACHINE' " _
    & "AND RootPath='SOFTWARE\\Microsoft'")

While (True)
   Set TreeChange = colTreeChanges.NextEvent
   TreeChange.GetObjectText_()
   Wscript.Echo  "Hive = " & TreeChange.Hive & VBNewLine _
      & "RootPath = "& TreeChange.RootPath _
      & TreeChange.GetObjectText_()      
Wend
```



O exemplo de código VBScript a seguir mostra como monitorar a alteração nos valores de uma chave registrando-se para o tipo de evento do provedor de registro [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). O script chama um método assíncrono, [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Para obter mais informações sobre chamadas assíncronas e segurança, consulte [fazendo uma chamada assíncrona com o VBScript](making-an-asynchronous-call-with-vbscript.md).

O script a seguir é executado indefinidamente até que o computador seja reinicializado, o WMI é interrompido ou o script é interrompido. Para interromper o script manualmente, use o Gerenciador de tarefas para interromper o processo. Para interrompê-lo programaticamente, use o método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) na classe de processo do Win32 \_ .


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:root/default") 
Set wmiSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink", "SINK_") 
Set ObjRegistry = GetObject("winmgmts:_
    {impersonationLevel = impersonate}!\\" _
    & strComputer & "\root\default:StdRegProv")

' Create a new key
strPath = "SOFTWARE\MyKey\MySubKey\"
Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

' Start listening for change in key
objWMIServices.ExecNotificationQueryAsync wmiSink, _ 
    "SELECT * FROM RegistryKeyChangeEvent " _ 
    & "WHERE Hive='HKEY_LOCAL_MACHINE' AND " _ 
    & "KeyPath='SOFTWARE\\MyKey\\MySubKey\\'" 
WScript.Echo "Listening for Registry Change Events..." 

While(True) 
    WScript.Sleep 1000
' You can use Regedit to make a change in the key 
' HKEY_LOCAL_MACHINE\SOFTWARE\MyKey\MySubKey\ 
'    to see an event generated.
Wend 

Sub SINK_OnObjectReady(EventObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Change Event" & vbCrLf & _
      EventObject.GetObjectText_() 
End Sub
```



 

