---
description: Você pode criar uma conexão remota com o WMI com o VBScript criando um objeto de conexão. Esse objeto contém o nome do computador, o namespace WMI ao qual você deseja se conectar, bem como quaisquer credenciais relevantes e níveis de autenticação.
ms.assetid: b2ad262b-148d-47cc-8be7-6df99245aa7f
ms.tgt_platform: multiple
title: Conectando-se ao WMI remotamente com o VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ccdd4466273cdc3b49399abf30915a975418433183d821482a8fa92920d52d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819684"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a>Conectando-se ao WMI remotamente com o VBScript

Você pode criar uma conexão remota com o WMI com o VBScript criando um objeto de conexão. Esse objeto contém o nome do computador, o namespace WMI ao qual você deseja se conectar, bem como quaisquer credenciais relevantes e níveis de autenticação.

**Para se conectar a um sistema remoto usando o VBScript**

1.  Especifique as informações de conexão, como o nome do computador remoto, as credenciais e o nível de autenticação para a conexão.

    Se você estiver se conectando a um computador remoto usando as mesmas credenciais (domínio e nome de usuário) com as quais você fez logon, poderá especificar as informações de conexão em um [moniker](constructing-a-moniker-string.md) [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), conforme descrito no exemplo de código a seguir.

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    Em termos gerais, você deve especificar o namespace do WMI para se conectar ao no computador remoto. Isso ocorre porque é possível que o namespace padrão não seja o mesmo em computadores diferentes. Especificar o namespace garante que você se conecte ao mesmo namespace em todos os computadores.

    Para obter mais informações sobre as constantes do VBScript e cadeias de caracteres de script para usar a conexão do moniker, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).

2.  Se você se conectar a um computador remoto em um domínio diferente ou usar um nome de usuário e senha diferentes, você deverá usar o método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .

    Como com um moniker, você usa **ConnectServer** para especificar as credenciais, o nível de autenticação e o namespace para a conexão remota. O exemplo de código a seguir descreve como usar o ConnectServer para acessar um computador remoto usando uma conta e senha de administrador.

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  Ao usar a função [**ConnectServer**](swbemlocator-connectserver.md) para conexões remotas, defina a representação e a autenticação no objeto de segurança obtido por uma chamada para [**SWbemServices. Security**](swbemservices-security-.md). Você pode usar a enumeração [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) para especificar o nível de representação.

    O exemplo de código a seguir define o nível de representação para o exemplo de código do VBScript anterior.

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    Observe que algumas conexões exigem um nível de autenticação específico. Para obter mais informações, consulte [definindo a segurança do processo de aplicativo cliente](setting-client-application-process-security.md) e [protegendo os clientes de script](securing-scripting-clients.md).

    Em particular, você deve definir o nível de autenticação para a privacidade do PCT de nível de autenticação **RPC \_ C \_ \_ \_ \_** ou 6 se o namespace ao qual você está se conectando no computador remoto exigir uma conexão criptografada antes de retornar os dados. Você também pode usar esse nível de autenticação, mesmo que o namespace não o exija. Isso garante que os dados sejam criptografados enquanto atravessam a rede. Se você tentar definir um nível de autenticação menor do que o permitido, uma mensagem de acesso negado será retornada. Para obter mais informações, consulte [exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md).

Depois de fazer a conexão, você poderá continuar a acessar os dados do WMI. Para obter mais informações, consulte [tarefas do WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md).

## <a name="examples"></a>Exemplos

Para obter um exemplo de VBScript maior, consulte a seção exemplos na página de referência [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .

O exemplo de código VBScript a seguir se conecta a um grupo de computadores remotos no mesmo domínio criando uma matriz de nomes de computador remoto e, em seguida, exibindo os nomes dos dispositivos Plug and Play — instâncias do [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)— em cada computador. Para executar o script abaixo, você deve ser um administrador nos computadores remotos. Observe que o " \\ \\ " necessário antes do nome do computador remoto é adicionado pelo script após a configuração de nível de representação. Para obter mais informações sobre caminhos WMI, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" & strComputer& "\Root\CIMv2") 
    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



O exemplo de código VBScript a seguir permite que você se conecte a um computador remoto usando credenciais diferentes. Por exemplo, um computador remoto em um domínio diferente ou se conectar a um computador remoto que requer um nome de usuário e uma senha diferentes. Nesse caso, use a conexão [**SWbemServices. ConnectServer**](swbemlocator-connectserver.md) .


```VB
' Full Computer Name
' can be found by right-clicking My Computer,
' then click Properties, then click the Computer Name tab)
' or use the computer's IP address
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
