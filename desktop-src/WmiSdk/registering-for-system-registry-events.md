---
description: Para receber notificações do provedor do Registro do Sistema, um aplicativo de gerenciamento deve se registrar como um consumidor de evento temporário.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Registrando-se para eventos do Registro do Sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c6f60b21dee729a879aaeab676da67b06ca0a822bcfd6509bc0f406f96fecec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554241"
---
# <a name="registering-for-system-registry-events"></a>Registrando-se para eventos do Registro do Sistema

Para receber notificações do provedor do [Registro do](/previous-versions/windows/desktop/regprov/system-registry-provider) Sistema, um aplicativo de gerenciamento deve se registrar como um consumidor de evento temporário. A maioria dos requisitos para se registrar no provedor do Registro do Sistema é igual a qualquer outro registro de evento, exceto que você também deve executar o procedimento a seguir.

O provedor do Registro fornece classes de evento para eventos no registro do sistema. Para obter mais informações sobre o registro de evento geral, consulte [Recebendo um evento WMI](receiving-a-wmi-event.md).

O procedimento a seguir descreve como se registrar para eventos do Registro do sistema.

**Para registrar-se para eventos de registro do sistema**

1.  Chame um método de consulta de notificação.

    No script ou no C++, use uma consulta de notificação como [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) ou [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync). Crie uma cadeia de caracteres de consulta para o parâmetro *bstrQuery* **de IWbemServices::ExecNotificationQueryAsync** ou *o strQuery* no script.

2.  Determine qual tipo de evento você deseja receber e crie a consulta.

    A tabela a seguir lista as classes de evento do Registro que você pode usar.

    

    | Classe de eventos                                                      | Localização do Hive        | Descrição                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent)                       | N/D<br/>       | Classe base abstrata para alterações no Registro.<br/> |
    | [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | RootPath<br/>  | Monitora as alterações em uma hierarquia de chaves.<br/>         |
    | [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | KeyPath<br/>   | Monitora as alterações em uma única chave.<br/>                |
    | [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | ValueName<br/> | Monitora as alterações em um único valor.<br/>              |

    

     

    Essas classes têm uma propriedade chamada **Hive** que identifica a hierarquia de chaves a ser monitorada quanto a alterações, como **HKEY \_ LOCAL \_ MACHINE.**

    Não há suporte para alterações nas classes **HKEY \_ \_ ROOT** e **HKEY \_ CURRENT \_ USER** hives por [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) ou classes derivadas dele, como [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).

3.  Crie a cláusula WHERE para o registro de evento.

    O provedor do Registro do Sistema tem regras específicas para cláusulas WHERE. Para obter mais informações, consulte [Criando uma cláusula WHERE adequada para o provedor do Registro](creating-a-proper-where-clause-for-the-registry-provider.md). Para obter informações mais gerais sobre como criar uma cláusula WHERE, consulte [Consultando com WQL](querying-with-wql.md).

4.  Determine se o consumidor está recebendo eventos.

    O provedor do Registro do Sistema não garante que todos os eventos enviados sejam entregues. Para obter mais informações, consulte [Recebendo eventos do Registro](receiving-registry-events.md).

O exemplo de código VBScript a seguir mostra como detectar uma alteração de registro na subárvore ou subárvore **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft.** Este é um script de monitoramento que, para fins de demonstração, é executado em um processo chamado Wscript.exe até que seja encerrado no **Gerenciador de Tarefas**, o WMI é interrompido ou o sistema operacional é reinicializado. O script usa uma [*chamada síncrona*](gloss-s.md) para [**SWbemServices.ExecNotificationQuery.**](swbemservices-execnotificationquery.md) Para obter mais informações sobre chamadas síncronas, consulte Fazendo uma [chamada semisíncrona com VBScript.](making-a-semisynchronous-call-with-vbscript.md)


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



O exemplo de código VBScript a seguir mostra como monitorar a alteração nos valores de uma chave registrando-se para o tipo de evento do provedor de Registro [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). O script chama um método assíncrono, [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Para obter mais informações sobre chamadas assíncronas e segurança, consulte Fazendo uma [chamada assíncrona com o VBScript.](making-an-asynchronous-call-with-vbscript.md)

O script a seguir é executado indefinidamente até que o computador seja reinicializado, o WMI seja interrompido ou o script seja interrompido. Para interromper o script manualmente, use Gerenciador de Tarefas para interromper o processo. Para interromper programaticamente, use o [**método Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) na classe Processo Win32. \_


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



 

