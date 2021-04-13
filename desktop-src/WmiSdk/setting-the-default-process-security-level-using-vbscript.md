---
title: Definir o nível de segurança do processo padrão com o VBScript
description: Um script pode usar a autenticação WMI padrão e as configurações de representação. No entanto, o script pode precisar de uma conexão com mais segurança ou pode se conectar a um namespace que requer uma conexão criptografada.
ms.assetid: cb477224-3117-45e4-9271-613b58e48b6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03fe69228021fe8d3f36f03e60cb2366b6132f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171800"
---
# <a name="set-the-default-process-security-level-with-vbscript"></a>Definir o nível de segurança do processo padrão com o VBScript

Um script pode usar a autenticação WMI padrão e as configurações de representação. No entanto, o script pode precisar de uma conexão com mais segurança ou pode se conectar a um namespace que requer uma conexão criptografada. Para obter mais informações, consulte [Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md) e [exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md).

No caso mais simples, um script pode usar as configurações de representação e de autenticação padrão. O WMI normalmente é executado em um host de serviço compartilhado e compartilha a mesma autenticação que outros processos no host. Se você quiser executar o processo WMI com um nível diferente de autenticação, execute o WMI com o comando [**winmgmt**](winmgmt.md) com a opção **/standalonehost** e defina o nível de autenticação para WMI em geral. Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).

O script a seguir usa as configurações padrão para representação e níveis de autenticação.


```VB
strComputer = "." 
Set objServices = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



Você também pode usar um [moniker](constructing-a-moniker-string.md) em uma chamada para [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)e definir as configurações de segurança padrão, como no exemplo a seguir.


```VB
strComputer = "." 
Set objServices = GetObject( _
    "winmgmts:{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!root/cimv2")
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



Para obter mais informações sobre como definir diferentes níveis de representação ou de autenticação em um script ou para definir os valores padrão para um computador, consulte os seguintes tópicos:

-   [Alterando as credenciais de autenticação padrão usando o VBScript](#changing-the-default-authentication-credentials-using-vbscript)
-   [Alterando as configurações de representação padrão usando o VBScript](#changing-the-default-impersonation-levels-using-vbscript)
-   [Definindo o nível de representação padrão usando o registro](#setting-the-default-impersonation-level-using-the-registry)
-   [Acessando o objeto SWbemSecurity no VBScript](#accessing-the-swbemsecurity-object-in-vbscript)
-   [**SWbemSecurity**](swbemsecurity.md)

## <a name="changing-the-default-authentication-credentials-using-vbscript"></a>Alterando as credenciais de autenticação padrão usando o VBScript

Você pode alterar o nível de autenticação em um script usando uma cadeia de caracteres de [moniker](constructing-a-moniker-string.md) e os objetos [**SWbemLocator**](swbemlocator.md) e [**SWbemSecurity**](swbemsecurity.md) .

O nível de autenticação deve ser definido de acordo com os requisitos do sistema operacional de destino ao qual você está se conectando. Para obter mais informações, consulte [conectando entre diferentes sistemas operacionais](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).

O exemplo de código VBScript a seguir mostra como alterar o nível de autenticação em um script que obtém os dados de espaço livre de um computador remoto chamado "Server1".


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{authenticationLevel=Pkt}!\\" _
    & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
    Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
        "FreeSpace: " & vbTab & objDisk.FreeSpace 
    NextstrComputer = "." 
    Set objServices = GetObject( "winmgmts:{impersonationLevel=impersonate," _
                               & "authenticationLevel=pktPrivacy}!root/cimv2")
    Set objProcessSet = objServices.ExecQuery("SELECT Name FROM Win32_Process",,48)
    For Each Process in objProcessSet
        WScript.Echo Process.Name
    Next
Next
```



Em conexões de moniker de script para WMI, use o nome curto mostrado na coluna "nome do moniker/descrição" da tabela a seguir. Por exemplo, no script a seguir, o nível de autenticação é definido como **WbemAuthenticationLevelPktIntegrity**.


```VB
SetobjWMIService = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!root\cimv2")
```



A tabela a seguir lista os níveis de autenticação que você pode definir. Esses níveis são definidos em Wbemdisp. tlb na enumeração [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).



| Nome/valor                                                      | Descrição                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WbemAuthenticationLevelDefault**<br/> 0<br/>      | Moniker: padrão<br/> O WMI usa a configuração padrão de autenticação do Windows. Essa é a configuração recomendada que permite que o WMI negocie para o nível exigido pelo servidor que retorna dados. No entanto, se o namespace exigir criptografia, use **WbemAuthenticationLevelPktPrivacy**.<br/> |
| **WbemAuthenticationLevelNone**<br/> 1<br/>         | Moniker: nenhum<br/> Não usa autenticação.<br/>                                                                                                                                                                                                                                            |
| **WbemAuthenticationLevelConnect**<br/> 2<br/>      | Moniker: conectar<br/> Autentica as credenciais do cliente somente quando o cliente estabelece uma relação com o servidor.<br/>                                                                                                                                                    |
| **WbemAuthenticationLevelCall**<br/> 3<br/>         | Chamar<br/> Autentica somente no início de cada chamada quando o servidor recebe a solicitação.<br/>                                                                                                                                                                                      |
| **WbemAuthenticationLevelPkt**<br/> 4<br/>          | Moniker: PKT<br/> Autentica que todos os dados recebidos são do cliente esperado.<br/>                                                                                                                                                                                                   |
| **WbemAuthenticationLevelPktIntegrity**<br/> 5<br/> | Moniker: PktIntegrity<br/> Autentica e verifica se nenhum dos dados transferidos entre o cliente e o servidor foi modificado.<br/>                                                                                                                                                  |
| **WbemAuthenticationLevelPktPrivacy**<br/> 6<br/>   | Moniker: PktPrivacy<br/> Autentica todos os níveis de representação anteriores e criptografa o valor do argumento de cada chamada de procedimento remoto. Use essa configuração se o namespace ao qual você está se conectando exigir uma conexão criptografada.<br/>                                               |



 

Para determinar uma chamada bem-sucedida, verifique o valor de retorno depois de alterar o nível de autenticação.

Por exemplo, como as conexões locais sempre têm um nível de autenticação de **wbemAuthenticationLevelPktPrivacy**, o exemplo a seguir falha ao definir o nível de autenticação porque ele se conecta ao computador local.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!" _
    & "\\" & strComputer & "\root\cimv2")
```



Um provedor pode definir a segurança em um namespace para que nenhum dado seja retornado, a menos que você use a privacidade de pacote (PktPrivacy) em sua conexão com esse namespace. Isso garante que os dados sejam criptografados enquanto atravessam a rede. Se você tentar definir um nível de autenticação inferior, receberá uma mensagem de acesso negado. Para obter mais informações, consulte [SECURING WMI namespaces](securing-wmi-namespaces.md).

## <a name="changing-the-default-impersonation-levels-using-vbscript"></a>Alterando os níveis de representação padrão usando o VBScript

Quando você faz chamadas para a API de script para WMI, é recomendável usar os padrões que o WMI fornece para o nível de representação. Chamadas remotas e alguns provedores com mais de um salto de rede exigem um nível de representação mais alto do que o WMI usa. Se o nível de representação não for suficiente, um provedor poderá recusar uma solicitação ou fornecer informações incompletas.

Se você não definir o nível de representação em um moniker ou definindo [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) em um objeto protegível, defina o nível de representação DCOM padrão para o sistema operacional. O nível de representação deve ser definido de acordo com os requisitos do sistema operacional de destino ao qual você está se conectando. Para obter mais informações, consulte [conectando entre diferentes sistemas operacionais](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).

O exemplo de código VBScript a seguir mostra a alteração do nível de representação no mesmo script mostrado acima.


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" _
                              & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
             "FreeSpace: " & vbTab & objDisk.FreeSpace 
Next
```



A tabela a seguir lista os níveis de autenticação em [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) que usam.



| Nome/valor                                                    | Descrição                                                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wbemImpersonationLevelAnonymous**<br/> 1<br/>   | Moniker: anônimo<br/> Oculta as credenciais do autor da chamada. Chamadas ao WMI podem falhar com esse nível de representação.<br/>                                                                                                  |
| **wbemImpersonationLevelIdentify**<br/> 2<br/>    | Moniker: identificar<br/> Permite que os objetos consultem as credenciais do autor da chamada. Chamadas ao WMI podem falhar com esse nível de representação.<br/>                                                                                 |
| **wbemImpersonationLevelImpersonate**<br/> 3<br/> | Moniker: representar<br/> Permite que os objetos utilizem as credenciais do autor da chamada. Esse é o nível de representação recomendado para a API de script para chamadas WMI.<br/>                                                        |
| **wbemImpersonationLevelDelegate**<br/> 4<br/>    | Moniker: delegado<br/> Autoriza que os objetos permitam que outros objetos utilizem as credenciais do autor da chamada. Essa representação funcionará com a API de script para chamadas WMI, mas pode constituir um risco de segurança desnecessário.<br/> |



 

O exemplo a seguir mostra como definir a representação em uma cadeia de caracteres do moniker ao obter uma instância específica do [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process).


```VB
Set object = GetObject("winmgmts:{impersonationLevel=impersonate}!root\cimv2:Win32_Process.Handle='0'")
```



Para obter mais informações, consulte [criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md).

## <a name="setting-the-default-impersonation-level-using-the-registry"></a>Definindo o nível de representação padrão usando o registro

Se você tiver acesso ao registro, também poderá definir a chave de registro de nível de representação padrão. Essa chave especifica qual nível de representação a API de script para WMI usa, a menos que especificado de outra forma. O caminho a seguir identifica o caminho do registro.

**HKEY \_ \_** Nível de \\  \\  \\  \\  \\ **representação padrão** do software Microsoft WBEM script do computador local

Por padrão, a chave do registro é definida como 3, especificando o nível de representação Impersonate. Alguns provedores podem exigir um nível mais alto de representação.

## <a name="accessing-the-swbemsecurity-object-in-vbscript"></a>Acessando o objeto SWbemSecurity no VBScript

A outra maneira de definir o nível de representação é a partir do objeto de segurança [**SWbemSecurity**](swbemsecurity.md) , que aparece como a propriedade de [**segurança \_**](swbemservices-security-.md) dos objetos [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemEventSource**](swbemeventsource.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) .

O WMI passa a configuração de segurança de um objeto pai para os descendentes do objeto original. Portanto, você pode definir o nível de representação de um objeto [**SWbemServices**](swbemservices.md) depois de fazer logon no WMI e em chamadas à API usando esse objeto ou objetos criados a partir dele, como objetos do tipo [**SWbemObject**](swbemobject.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Protegendo clientes de script](securing-scripting-clients.md)
</dt> </dl>

 

