---
title: Obtendo dados de um computador remoto
description: Você pode obter dados ou gerenciar recursos em computadores remotos, bem como no computador local. Conectar-se a um computador remoto em um script de Gerenciamento Remoto do Windows é muito semelhante a fazer uma conexão local.
ms.assetid: 578eee80-a6c1-4456-9683-14e0a3386248
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cfc95a73dab4c9a0f19481b7ba41f3c40a3862d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823779"
---
# <a name="obtaining-data-from-a-remote-computer"></a>Obtendo dados de um computador remoto

Você pode obter dados ou gerenciar recursos em computadores remotos, bem como no computador local. Conectar-se a um computador remoto em um script de Gerenciamento Remoto do Windows é muito semelhante a fazer uma conexão local. Os dados da instância WMI estão disponíveis e, se o computador remoto tiver um hardware BMC que possa se comunicar usando o protocolo WS-Management, os dados da [IPMI (interface de gerenciamento de plataforma inteligente)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) também estarão disponíveis. Para obter mais informações, consulte [gerenciamento remoto do Windows e WMI](windows-remote-management-and-wmi.md) e [Gerenciamento de hardware remoto](remote-hardware-management.md).

Talvez seja necessário criar um objeto [**ConnectionOptions**](connectionoptions.md) para especificar informações sobre o tipo de autenticação solicitado para o logon.

Se a conta no computador remoto tiver o mesmo nome de usuário e senha de logon, as únicas informações adicionais necessárias serão o transporte, o nome de domínio e o nome do computador. Devido ao [UAC (controle de conta de usuário)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), a conta remota deve ser uma conta de domínio e um membro do grupo de administradores do computador remoto. Se a conta for um membro do computador local do grupo Administradores, o UAC não permitirá o acesso ao serviço WinRM. Para acessar um serviço WinRM remoto em um grupo de trabalho, a filtragem do UAC para contas locais deve ser desabilitada criando a seguinte entrada do Registro DWORD e definindo seu valor como 1: **\[ HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \] LocalAccountTokenFilterPolicy**.

**Para se conectar a um computador remoto usando seu nome de usuário e senha de logon**

1.  Especifique o computador de destino com um nome de domínio totalmente qualificado ou um endereço IP e atribua isso a uma constante. Se um endereço IPv6 for especificado, o endereço deverá ser colocado entre colchetes.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Crie um objeto [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  Crie a sessão, especificando o transporte, HTTP ou HTTPS, e concatenando-a com a constante que representa o computador de destino.

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

O exemplo de código VBScript a seguir mostra o script completo. O script inclui uma sub-rotina para transformar os dados do XML bruto para o formato legível por humanos. Para obter mais informações, consulte [exibindo a saída XML de scripts do WinRM](displaying-xml-output-from-winrm-scripts.md).


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



**Para se conectar a um computador remoto usando uma conta diferente**

1.  Especifique o computador de destino com um nome de domínio totalmente qualificado ou um endereço IP e atribua isso a uma constante. Se um endereço IPv6 for especificado, o endereço deverá ser colocado entre colchetes.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Crie um objeto [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  Chame o método [**WSMan. Createconnectoptions**](wsman-createconnectionoptions.md) para criar um objeto [**ConnectionOptions**](connectionoptions.md) . A conta no computador remoto deve ser um membro do grupo de administradores do computador local.

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  Na chamada [**WSman. CreateSession**](wsman-createsession.md) , especifique os sinalizadores de conexão de sessão apropriados no parâmetro *flags* . Para obter mais informações, consulte [constantes de sessão](session-constants.md). Especifique o computador de destino com um nome de computador totalmente qualificado ou um endereço IP e o transporte — http ou HTTPS. Esse script solicita a autenticação [*Kerberos*](windows-remote-management-glossary.md) do serviço WinRM remoto.

    Ao contrário dos scripts WMI, você pode usar vários métodos de autenticação em scripts do WinRM. Para obter mais informações, consulte [autenticação para conexões remotas](authentication-for-remote-connections.md).

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  Depois que o objeto de sessão estiver disponível, você poderá chamar qualquer um dos métodos de objeto de [**sessão**](session.md) para obter dados de um recurso. Você pode obter dados para qualquer recurso que esteja disponível no computador no qual a sessão está em execução. Para obter mais informações, consulte [obtendo dados do computador local](obtaining-data-from-the-local-computer.md).

O exemplo de código VBScript a seguir mostra o script completo. O script inclui uma sub-rotina para transformar os dados do XML bruto para o formato legível por humanos. Para obter mais informações, consulte [exibindo a saída XML de scripts do WinRM](displaying-xml-output-from-winrm-scripts.md). O script especifica a autenticação Kerberos, mas se o computador remoto estiver em um grupo de trabalho em vez de em um domínio, a especificação de Kerberos gerará um erro.


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("Wsman.Automation")
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "Username"
objConnectionOptions.Password = "Password"
iFlags = objWsman.SessionFlagUseKerberos Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
  iFlags, objConnectionOptions)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[Usando Gerenciamento Remoto do Windows](using-windows-remote-management.md)
</dt> <dt>

[Referência de Gerenciamento Remoto do Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 