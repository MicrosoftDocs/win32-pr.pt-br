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
# <a name="obtaining-data-from-a-remote-computer"></a><span data-ttu-id="773ec-104">Obtendo dados de um computador remoto</span><span class="sxs-lookup"><span data-stu-id="773ec-104">Obtaining Data from a Remote Computer</span></span>

<span data-ttu-id="773ec-105">Você pode obter dados ou gerenciar recursos em computadores remotos, bem como no computador local.</span><span class="sxs-lookup"><span data-stu-id="773ec-105">You can obtain data or manage resources on remote computers as well as the local computer.</span></span> <span data-ttu-id="773ec-106">Conectar-se a um computador remoto em um script de Gerenciamento Remoto do Windows é muito semelhante a fazer uma conexão local.</span><span class="sxs-lookup"><span data-stu-id="773ec-106">Connecting to a remote computer in a Windows Remote Management script is very similar to making a local connection.</span></span> <span data-ttu-id="773ec-107">Os dados da instância WMI estão disponíveis e, se o computador remoto tiver um hardware BMC que possa se comunicar usando o protocolo WS-Management, os dados da [IPMI (interface de gerenciamento de plataforma inteligente)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) também estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="773ec-107">WMI instance data is available and, if the remote computer has BMC hardware that can communicate using the WS-Management protocol, then [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) data is also available.</span></span> <span data-ttu-id="773ec-108">Para obter mais informações, consulte [gerenciamento remoto do Windows e WMI](windows-remote-management-and-wmi.md) e [Gerenciamento de hardware remoto](remote-hardware-management.md).</span><span class="sxs-lookup"><span data-stu-id="773ec-108">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md) and [Remote Hardware Management](remote-hardware-management.md).</span></span>

<span data-ttu-id="773ec-109">Talvez seja necessário criar um objeto [**ConnectionOptions**](connectionoptions.md) para especificar informações sobre o tipo de autenticação solicitado para o logon.</span><span class="sxs-lookup"><span data-stu-id="773ec-109">You may need to create a [**ConnectionOptions**](connectionoptions.md) object to specify information about the type of authentication requested for the logon.</span></span>

<span data-ttu-id="773ec-110">Se a conta no computador remoto tiver o mesmo nome de usuário e senha de logon, as únicas informações adicionais necessárias serão o transporte, o nome de domínio e o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="773ec-110">If the account on the remote computer has the same logon username and password, the only extra information you need is the transport, the domain name, and the computer name.</span></span> <span data-ttu-id="773ec-111">Devido ao [UAC (controle de conta de usuário)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), a conta remota deve ser uma conta de domínio e um membro do grupo de administradores do computador remoto.</span><span class="sxs-lookup"><span data-stu-id="773ec-111">Because of [User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), the remote account must be a domain account and a member of the remote computer Administrators group.</span></span> <span data-ttu-id="773ec-112">Se a conta for um membro do computador local do grupo Administradores, o UAC não permitirá o acesso ao serviço WinRM.</span><span class="sxs-lookup"><span data-stu-id="773ec-112">If the account is a local computer member of the Administrators group, then UAC does not allow access to the WinRM service.</span></span> <span data-ttu-id="773ec-113">Para acessar um serviço WinRM remoto em um grupo de trabalho, a filtragem do UAC para contas locais deve ser desabilitada criando a seguinte entrada do Registro DWORD e definindo seu valor como 1: **\[ HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \] LocalAccountTokenFilterPolicy**.</span><span class="sxs-lookup"><span data-stu-id="773ec-113">To access a remote WinRM service in a workgroup, UAC filtering for local accounts must be disabled by creating the following DWORD registry entry and setting its value to 1: **\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\System\] LocalAccountTokenFilterPolicy**.</span></span>

<span data-ttu-id="773ec-114">**Para se conectar a um computador remoto usando seu nome de usuário e senha de logon**</span><span class="sxs-lookup"><span data-stu-id="773ec-114">**To connect to a remote computer using your logon username and password**</span></span>

1.  <span data-ttu-id="773ec-115">Especifique o computador de destino com um nome de domínio totalmente qualificado ou um endereço IP e atribua isso a uma constante.</span><span class="sxs-lookup"><span data-stu-id="773ec-115">Specify the target computer with a fully qualified domain name or an IP address and assign this to a constant.</span></span> <span data-ttu-id="773ec-116">Se um endereço IPv6 for especificado, o endereço deverá ser colocado entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="773ec-116">If an IPv6 address is specified, then the address must be enclosed in square brackets.</span></span>

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  <span data-ttu-id="773ec-117">Crie um objeto [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="773ec-117">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  <span data-ttu-id="773ec-118">Crie a sessão, especificando o transporte, HTTP ou HTTPS, e concatenando-a com a constante que representa o computador de destino.</span><span class="sxs-lookup"><span data-stu-id="773ec-118">Create the session, specifying the transport, HTTP or HTTPS, and concatenating it with the constant representing the target computer.</span></span>

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

<span data-ttu-id="773ec-119">O exemplo de código VBScript a seguir mostra o script completo.</span><span class="sxs-lookup"><span data-stu-id="773ec-119">The following VBScript code example shows the complete script.</span></span> <span data-ttu-id="773ec-120">O script inclui uma sub-rotina para transformar os dados do XML bruto para o formato legível por humanos.</span><span class="sxs-lookup"><span data-stu-id="773ec-120">The script includes a subroutine to transform the data from raw XML to human-readable form.</span></span> <span data-ttu-id="773ec-121">Para obter mais informações, consulte [exibindo a saída XML de scripts do WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="773ec-121">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>


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



<span data-ttu-id="773ec-122">**Para se conectar a um computador remoto usando uma conta diferente**</span><span class="sxs-lookup"><span data-stu-id="773ec-122">**To connect to a remote computer using a different account**</span></span>

1.  <span data-ttu-id="773ec-123">Especifique o computador de destino com um nome de domínio totalmente qualificado ou um endereço IP e atribua isso a uma constante.</span><span class="sxs-lookup"><span data-stu-id="773ec-123">Specify the target computer with a fully qualified domain name or an IP address and assign this to a constant.</span></span> <span data-ttu-id="773ec-124">Se um endereço IPv6 for especificado, o endereço deverá ser colocado entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="773ec-124">If an IPv6 address is specified, then the address must be enclosed in square brackets.</span></span>

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  <span data-ttu-id="773ec-125">Crie um objeto [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="773ec-125">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  <span data-ttu-id="773ec-126">Chame o método [**WSMan. Createconnectoptions**](wsman-createconnectionoptions.md) para criar um objeto [**ConnectionOptions**](connectionoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="773ec-126">Call the [**WSMan.CreateConnectionOptions**](wsman-createconnectionoptions.md) method to create a [**ConnectionOptions**](connectionoptions.md) object.</span></span> <span data-ttu-id="773ec-127">A conta no computador remoto deve ser um membro do grupo de administradores do computador local.</span><span class="sxs-lookup"><span data-stu-id="773ec-127">The account on the remote computer must be a member of the local computer administrators group.</span></span>

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  <span data-ttu-id="773ec-128">Na chamada [**WSman. CreateSession**](wsman-createsession.md) , especifique os sinalizadores de conexão de sessão apropriados no parâmetro *flags* .</span><span class="sxs-lookup"><span data-stu-id="773ec-128">On the [**WSman.CreateSession**](wsman-createsession.md) call, specify the appropriate session connection flags in the *flags* parameter.</span></span> <span data-ttu-id="773ec-129">Para obter mais informações, consulte [constantes de sessão](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="773ec-129">For more information, see [Session Constants](session-constants.md).</span></span> <span data-ttu-id="773ec-130">Especifique o computador de destino com um nome de computador totalmente qualificado ou um endereço IP e o transporte — http ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="773ec-130">Specify the target computer with a fully qualified computer name or an IP address and the transport—http or https.</span></span> <span data-ttu-id="773ec-131">Esse script solicita a autenticação [*Kerberos*](windows-remote-management-glossary.md) do serviço WinRM remoto.</span><span class="sxs-lookup"><span data-stu-id="773ec-131">This script requests [*Kerberos*](windows-remote-management-glossary.md) authentication from the remote WinRM service.</span></span>

    <span data-ttu-id="773ec-132">Ao contrário dos scripts WMI, você pode usar vários métodos de autenticação em scripts do WinRM.</span><span class="sxs-lookup"><span data-stu-id="773ec-132">Unlike WMI scripts, you can use several methods of authentication in WinRM scripts.</span></span> <span data-ttu-id="773ec-133">Para obter mais informações, consulte [autenticação para conexões remotas](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="773ec-133">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  <span data-ttu-id="773ec-134">Depois que o objeto de sessão estiver disponível, você poderá chamar qualquer um dos métodos de objeto de [**sessão**](session.md) para obter dados de um recurso.</span><span class="sxs-lookup"><span data-stu-id="773ec-134">After the session object is available, you can call any of the [**Session**](session.md) object methods to obtain data for a resource.</span></span> <span data-ttu-id="773ec-135">Você pode obter dados para qualquer recurso que esteja disponível no computador no qual a sessão está em execução.</span><span class="sxs-lookup"><span data-stu-id="773ec-135">You can get data for any resource that is available on the computer on which the session is running.</span></span> <span data-ttu-id="773ec-136">Para obter mais informações, consulte [obtendo dados do computador local](obtaining-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="773ec-136">For more information, see [Obtaining Data from the Local Computer](obtaining-data-from-the-local-computer.md).</span></span>

<span data-ttu-id="773ec-137">O exemplo de código VBScript a seguir mostra o script completo.</span><span class="sxs-lookup"><span data-stu-id="773ec-137">The following VBScript code example shows the complete script.</span></span> <span data-ttu-id="773ec-138">O script inclui uma sub-rotina para transformar os dados do XML bruto para o formato legível por humanos.</span><span class="sxs-lookup"><span data-stu-id="773ec-138">The script includes a subroutine to transform the data from raw XML to human-readable form.</span></span> <span data-ttu-id="773ec-139">Para obter mais informações, consulte [exibindo a saída XML de scripts do WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="773ec-139">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span> <span data-ttu-id="773ec-140">O script especifica a autenticação Kerberos, mas se o computador remoto estiver em um grupo de trabalho em vez de em um domínio, a especificação de Kerberos gerará um erro.</span><span class="sxs-lookup"><span data-stu-id="773ec-140">The script specifies Kerberos authentication, but if the remote computer is in a workgroup rather than a domain, specifying Kerberos generates an error.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="773ec-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="773ec-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="773ec-142">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="773ec-142">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="773ec-143">Usando Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="773ec-143">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="773ec-144">Referência de Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="773ec-144">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 