---
description: Scripts WMI podem condensar muitas das etapas necessárias em um programa C++.
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: Conectando-se ao WMI com VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b4e71f4225a55e24432562d4c35754080b9746386489b7dbf7061cb65c9771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131608"
---
# <a name="connecting-to-wmi-with-vbscript"></a>Conectando-se ao WMI com VBScript

Scripts WMI podem condensar muitas das etapas necessárias em um programa C++. Eles podem se conectar ao WMI, não apenas por meio de um [**objeto SWbemLocator,**](swbemlocator.md) mas também por meio do moniker "winmgmts:". Um moniker é um nome curto que localiza um namespace, classe ou instância no WMI. O nome "winmgmts:" é o moniker WMI que informa ao Host de Script do Windows para usar os objetos WMI, conecta-se ao namespace padrão e obtém um [**objeto SWbemServices.**](swbemservices.md) Outras informações de conexão, como um nível de representação ou uma classe ou instância específica, aparecem na cadeia de caracteres após o nome do moniker. Você pode usar monikers em chamadas que criam ou geram objetos WMI. Para obter mais informações, consulte [Constructing a Moniker String](constructing-a-moniker-string.md).

O procedimento a seguir descreve como se conectar ao WMI usando **SWbemLocator**.

**Para se conectar ao WMI usando SWbemLocator**

1.  Recupere um objeto de localizador com uma chamada para [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  Faça logon no namespace usando uma chamada para o [**método ConnectServer.**](swbemlocator-connectserver.md)

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    Se você não especificar um computador na chamada para [**ConnectServer,**](swbemlocator-connectserver.md)o WMI se conectará ao computador local. Se você não especificar um namespace, o WMI se conectará ao namespace especificado na chave do Registro.

    **HKEY \_ Namespace \_ padrão** de script \\  \\  \\ **WBEM** \\ **do** \\  Microsoft MACHINE SOFTWARE LOCAL

    O namespace padrão é \\ root \\ cimv2. Para obter mais informações sobre namespaces, consulte [Criando hierarquias no WMI](creating-hierarchies-within-wmi.md).

3.  De definir o nível de representação com uma chamada para o [**método SWbemServices.Security. \_**](swbemservices-security-.md)

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    Para obter mais informações, consulte Definindo o nível de segurança [do processo padrão usando o VBScript.](setting-the-default-process-security-level-using-vbscript.md)

4.  Implemente a finalidade do script.

    O WMI expõe uma variedade de objetos de script que usam para acessar e manipular dados em sua rede. Para obter mais informações, consulte [Manipulando informações de classe e instância](manipulating-class-and-instance-information.md) e API de script para [WMI](scripting-api-for-wmi.md).

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    objService.Security_.ImpersonationLevel = 3
    Set Jobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
    i=0
    For each Job in Jobs
        i = i+1   
        WScript.Echo Job.JobId & "  " & Job.Command & VBNewLine
    Next
    If i = 0 Then
        WScript.Echo "No Jobs Scheduled with the AT command were found"
    End If
    ```

    

O procedimento a seguir descreve como se conectar ao WMI e recuperar um objeto usando um moniker.

**Para se conectar ao WMI e recuperar um objeto usando um moniker**

1.  Chame [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) com um moniker no parâmetro de entrada.

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    O moiniker contém vários elementos que você pode usar para se conectar ao WMI:

    -   O "winmgmts:" informa ao WSH para usar [objetos da API de Script.](scripting-api-objects.md) Neste exemplo específico, o WSH sabe que ele deve retornar um SWbemObject que descreve o primeiro Win32 \_ scheduledJob no sistema. Outros objetos possíveis a serem retornadas seriam um objeto SWbemCollection ou [**SWbemServices,**](swbemservices.md) dependendo do que o moniker descreveu.

    -   Opcionalmente, você pode definir os níveis de segurança para a conexão. No entanto, não é possível definir informações de nome e senha em um moniker. Para obter mais informações, consulte [Proteger clientes de script.](securing-scripting-clients.md)

    -   Opcionalmente, você pode definir o caminho para o objeto WMI. Isso inclui o computador local ou remoto, o namespace, bem como o nome da classe. Para obter mais informações sobre como usar o [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) do VBScript em scripts WMI, consulte Criando uma instância e recuperando [uma instância WMI](retrieving-an-instance.md). [](creating-an-instance.md)

2.  Em vez de recuperar um único item ou coleção, você também pode optar por recuperar o objeto [**SWbemServices**](swbemservices.md) (conforme descrito no exemplo anterior). Posteriormente, você pode chamar consultas adicionais no objeto retornado.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    No exemplo anterior, representar ou impersonationLevel=3 é o nível de segurança do processo padrão. No exemplo a seguir, não é necessário especificar esse nível de segurança do processo, a menos que você precise alterar a segurança do processo para **delegar**. Para obter mais informações, consulte Definindo o nível de segurança [do processo padrão usando o VBScript.](setting-the-default-process-security-level-using-vbscript.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
