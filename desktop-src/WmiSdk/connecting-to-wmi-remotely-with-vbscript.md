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
ms.openlocfilehash: 07cff2f0cd0ca06de059d9b39e36d715b5555eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793668"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a><span data-ttu-id="82e95-104">Conectando-se ao WMI remotamente com o VBScript</span><span class="sxs-lookup"><span data-stu-id="82e95-104">Connecting to WMI Remotely with VBScript</span></span>

<span data-ttu-id="82e95-105">Você pode criar uma conexão remota com o WMI com o VBScript criando um objeto de conexão.</span><span class="sxs-lookup"><span data-stu-id="82e95-105">You can create a remote connection to WMI with VBScript by creating a connection object.</span></span> <span data-ttu-id="82e95-106">Esse objeto contém o nome do computador, o namespace WMI ao qual você deseja se conectar, bem como quaisquer credenciais relevantes e níveis de autenticação.</span><span class="sxs-lookup"><span data-stu-id="82e95-106">This object contains the name of the computer, the WMI namespace you want to connect to, as well as any relevant credentials and authentication levels.</span></span>

<span data-ttu-id="82e95-107">**Para se conectar a um sistema remoto usando o VBScript**</span><span class="sxs-lookup"><span data-stu-id="82e95-107">**To connect to a remote system using VBScript**</span></span>

1.  <span data-ttu-id="82e95-108">Especifique as informações de conexão, como o nome do computador remoto, as credenciais e o nível de autenticação para a conexão.</span><span class="sxs-lookup"><span data-stu-id="82e95-108">Specify the connection information such as the remote computer name, credentials, and the authentication level for the connection.</span></span>

    <span data-ttu-id="82e95-109">Se você estiver se conectando a um computador remoto usando as mesmas credenciais (domínio e nome de usuário) com as quais você fez logon, poderá especificar as informações de conexão em um [moniker](constructing-a-moniker-string.md) [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), conforme descrito no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="82e95-109">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you can specify the connection information in a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)[moniker](constructing-a-moniker-string.md), as described in the following code sample.</span></span>

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    <span data-ttu-id="82e95-110">Em termos gerais, você deve especificar o namespace do WMI para se conectar ao no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="82e95-110">Generally speaking, you should specify the WMI namespace to connect to on the remote computer.</span></span> <span data-ttu-id="82e95-111">Isso ocorre porque é possível que o namespace padrão não seja o mesmo em computadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="82e95-111">This is because it is possible that the default namespace is not the same on different computers.</span></span> <span data-ttu-id="82e95-112">Especificar o namespace garante que você se conecte ao mesmo namespace em todos os computadores.</span><span class="sxs-lookup"><span data-stu-id="82e95-112">Specifying the namespace ensures that you connect to the same namespace on all computers.</span></span>

    <span data-ttu-id="82e95-113">Para obter mais informações sobre as constantes do VBScript e cadeias de caracteres de script para usar a conexão do moniker, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="82e95-113">For more information on VBScript constants and scripting strings for using the moniker connection, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

2.  <span data-ttu-id="82e95-114">Se você se conectar a um computador remoto em um domínio diferente ou usar um nome de usuário e senha diferentes, você deverá usar o método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="82e95-114">If you connect to a remote computer in a different domain or using a different user name and password, then you must use the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

    <span data-ttu-id="82e95-115">Como com um moniker, você usa **ConnectServer** para especificar as credenciais, o nível de autenticação e o namespace para a conexão remota.</span><span class="sxs-lookup"><span data-stu-id="82e95-115">As with a moniker, you use **ConnectServer** to specify the credentials, authentication level, and namespace for the remote connection.</span></span> <span data-ttu-id="82e95-116">O exemplo de código a seguir descreve como usar o ConnectServer para acessar um computador remoto usando uma conta e senha de administrador.</span><span class="sxs-lookup"><span data-stu-id="82e95-116">The following code sample describes using ConnectServer to access a remote computer using an administrator account and password.</span></span>

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  <span data-ttu-id="82e95-117">Ao usar a função [**ConnectServer**](swbemlocator-connectserver.md) para conexões remotas, defina a representação e a autenticação no objeto de segurança obtido por uma chamada para [**SWbemServices. Security**](swbemservices-security-.md).</span><span class="sxs-lookup"><span data-stu-id="82e95-117">When using the [**ConnectServer**](swbemlocator-connectserver.md) function for remote connections, set impersonation and authentication on the security object obtained by a call to [**SWbemServices.Security**](swbemservices-security-.md).</span></span> <span data-ttu-id="82e95-118">Você pode usar a enumeração [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) para especificar o nível de representação.</span><span class="sxs-lookup"><span data-stu-id="82e95-118">You can use the enumeration [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) to specify impersonation level.</span></span>

    <span data-ttu-id="82e95-119">O exemplo de código a seguir define o nível de representação para o exemplo de código do VBScript anterior.</span><span class="sxs-lookup"><span data-stu-id="82e95-119">The following code sample sets the impersonation level for the previous VBScript code sample.</span></span>

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    <span data-ttu-id="82e95-120">Observe que algumas conexões exigem um nível de autenticação específico.</span><span class="sxs-lookup"><span data-stu-id="82e95-120">Note that some connections require a specific authentication level.</span></span> <span data-ttu-id="82e95-121">Para obter mais informações, consulte [definindo a segurança do processo de aplicativo cliente](setting-client-application-process-security.md) e [protegendo os clientes de script](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="82e95-121">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md) and [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

    <span data-ttu-id="82e95-122">Em particular, você deve definir o nível de autenticação para a privacidade do PCT de nível de autenticação **RPC \_ C \_ \_ \_ \_** ou 6 se o namespace ao qual você está se conectando no computador remoto exigir uma conexão criptografada antes de retornar os dados.</span><span class="sxs-lookup"><span data-stu-id="82e95-122">In particular, you should set the authentication level to **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or 6 if the namespace to which you are connecting on the remote computer requires an encrypted connection before it will return data.</span></span> <span data-ttu-id="82e95-123">Você também pode usar esse nível de autenticação, mesmo que o namespace não o exija.</span><span class="sxs-lookup"><span data-stu-id="82e95-123">You can also use this authentication level, even if the namespace does not require it.</span></span> <span data-ttu-id="82e95-124">Isso garante que os dados sejam criptografados enquanto atravessam a rede.</span><span class="sxs-lookup"><span data-stu-id="82e95-124">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="82e95-125">Se você tentar definir um nível de autenticação menor do que o permitido, uma mensagem de acesso negado será retornada.</span><span class="sxs-lookup"><span data-stu-id="82e95-125">If you attempt to set a lower authentication level than is allowed, an access denied message will be returned.</span></span> <span data-ttu-id="82e95-126">Para obter mais informações, consulte [exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="82e95-126">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="82e95-127">Depois de fazer a conexão, você poderá continuar a acessar os dados do WMI.</span><span class="sxs-lookup"><span data-stu-id="82e95-127">Once you have made your connection, you can continue to access WMI data.</span></span> <span data-ttu-id="82e95-128">Para obter mais informações, consulte [tarefas do WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md).</span><span class="sxs-lookup"><span data-stu-id="82e95-128">For more information, see [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span>

## <a name="examples"></a><span data-ttu-id="82e95-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="82e95-129">Examples</span></span>

<span data-ttu-id="82e95-130">Para obter um exemplo de VBScript maior, consulte a seção exemplos na página de referência [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="82e95-130">For a larger VBScript sample, see the Examples section in the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) reference page.</span></span>

<span data-ttu-id="82e95-131">O exemplo de código VBScript a seguir se conecta a um grupo de computadores remotos no mesmo domínio criando uma matriz de nomes de computador remoto e, em seguida, exibindo os nomes dos dispositivos Plug and Play — instâncias do [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)— em cada computador.</span><span class="sxs-lookup"><span data-stu-id="82e95-131">The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer.</span></span> <span data-ttu-id="82e95-132">Para executar o script abaixo, você deve ser um administrador nos computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="82e95-132">To run the script below, you must be an administrator on the remote computers.</span></span> <span data-ttu-id="82e95-133">Observe que o " \\ \\ " necessário antes do nome do computador remoto é adicionado pelo script após a configuração de nível de representação.</span><span class="sxs-lookup"><span data-stu-id="82e95-133">Note that the "\\\\" required before the remote computer name is added by the script following the impersonation level setting.</span></span> <span data-ttu-id="82e95-134">Para obter mais informações sobre caminhos WMI, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="82e95-134">For more information about WMI paths, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>


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



<span data-ttu-id="82e95-135">O exemplo de código VBScript a seguir permite que você se conecte a um computador remoto usando credenciais diferentes.</span><span class="sxs-lookup"><span data-stu-id="82e95-135">The following VBScript code example enables you to connect to a remote computer using different credentials.</span></span> <span data-ttu-id="82e95-136">Por exemplo, um computador remoto em um domínio diferente ou se conectar a um computador remoto que requer um nome de usuário e uma senha diferentes.</span><span class="sxs-lookup"><span data-stu-id="82e95-136">For example, a remote computer in a different domain or connecting to a remote computer requiring a different user name and password.</span></span> <span data-ttu-id="82e95-137">Nesse caso, use a conexão [**SWbemServices. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="82e95-137">In this case, use the [**SWbemServices.ConnectServer**](swbemlocator-connectserver.md) connection.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="82e95-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82e95-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82e95-139">Conectando-se ao WMI em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="82e95-139">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
