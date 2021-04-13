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
# <a name="set-the-default-process-security-level-with-vbscript"></a><span data-ttu-id="a19e7-104">Definir o nível de segurança do processo padrão com o VBScript</span><span class="sxs-lookup"><span data-stu-id="a19e7-104">Set the default process security level with VBScript</span></span>

<span data-ttu-id="a19e7-105">Um script pode usar a autenticação WMI padrão e as configurações de representação.</span><span class="sxs-lookup"><span data-stu-id="a19e7-105">A script can use the default WMI authentication and impersonation settings.</span></span> <span data-ttu-id="a19e7-106">No entanto, o script pode precisar de uma conexão com mais segurança ou pode se conectar a um namespace que requer uma conexão criptografada.</span><span class="sxs-lookup"><span data-stu-id="a19e7-106">However, the script may need a connection with more security or may connect to a namespace that requires an encrypted connection.</span></span> <span data-ttu-id="a19e7-107">Para obter mais informações, consulte [Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md) e [exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="a19e7-107">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md) and [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="a19e7-108">No caso mais simples, um script pode usar as configurações de representação e de autenticação padrão.</span><span class="sxs-lookup"><span data-stu-id="a19e7-108">In the simplest case, a script can use the default authentication and impersonation settings.</span></span> <span data-ttu-id="a19e7-109">O WMI normalmente é executado em um host de serviço compartilhado e compartilha a mesma autenticação que outros processos no host.</span><span class="sxs-lookup"><span data-stu-id="a19e7-109">WMI normally runs in a shared service host and shares the same authentication as other processes in the host.</span></span> <span data-ttu-id="a19e7-110">Se você quiser executar o processo WMI com um nível diferente de autenticação, execute o WMI com o comando [**winmgmt**](winmgmt.md) com a opção **/standalonehost** e defina o nível de autenticação para WMI em geral.</span><span class="sxs-lookup"><span data-stu-id="a19e7-110">If you want to run the WMI process with a different level of authentication, run WMI with the [**winmgmt**](winmgmt.md) command with the **/standalonehost** switch and set the authentication level for WMI generally.</span></span> <span data-ttu-id="a19e7-111">Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="a19e7-111">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

<span data-ttu-id="a19e7-112">O script a seguir usa as configurações padrão para representação e níveis de autenticação.</span><span class="sxs-lookup"><span data-stu-id="a19e7-112">The following script uses default settings for impersonation and authentication levels.</span></span>


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



<span data-ttu-id="a19e7-113">Você também pode usar um [moniker](constructing-a-moniker-string.md) em uma chamada para [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)e definir as configurações de segurança padrão, como no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="a19e7-113">You can also use a [moniker](constructing-a-moniker-string.md) in a call to [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), and set the default security settings, as in the following example.</span></span>


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



<span data-ttu-id="a19e7-114">Para obter mais informações sobre como definir diferentes níveis de representação ou de autenticação em um script ou para definir os valores padrão para um computador, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="a19e7-114">For more information about setting different impersonation or authentication levels in a script, or for setting the default values for a computer, see the following topics:</span></span>

-   [<span data-ttu-id="a19e7-115">Alterando as credenciais de autenticação padrão usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="a19e7-115">Changing the Default Authentication Credentials Using VBScript</span></span>](#changing-the-default-authentication-credentials-using-vbscript)
-   [<span data-ttu-id="a19e7-116">Alterando as configurações de representação padrão usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="a19e7-116">Changing the Default Impersonation Settings Using VBScript</span></span>](#changing-the-default-impersonation-levels-using-vbscript)
-   [<span data-ttu-id="a19e7-117">Definindo o nível de representação padrão usando o registro</span><span class="sxs-lookup"><span data-stu-id="a19e7-117">Setting the Default Impersonation Level Using the Registry</span></span>](#setting-the-default-impersonation-level-using-the-registry)
-   [<span data-ttu-id="a19e7-118">Acessando o objeto SWbemSecurity no VBScript</span><span class="sxs-lookup"><span data-stu-id="a19e7-118">Accessing the SWbemSecurity Object in VBScript</span></span>](#accessing-the-swbemsecurity-object-in-vbscript)
-   [<span data-ttu-id="a19e7-119">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="a19e7-119">**SWbemSecurity**</span></span>](swbemsecurity.md)

## <a name="changing-the-default-authentication-credentials-using-vbscript"></a><span data-ttu-id="a19e7-120">Alterando as credenciais de autenticação padrão usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="a19e7-120">Changing the Default Authentication Credentials Using VBScript</span></span>

<span data-ttu-id="a19e7-121">Você pode alterar o nível de autenticação em um script usando uma cadeia de caracteres de [moniker](constructing-a-moniker-string.md) e os objetos [**SWbemLocator**](swbemlocator.md) e [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="a19e7-121">You can change the authentication level in a script using a [moniker](constructing-a-moniker-string.md) string, and the [**SWbemLocator**](swbemlocator.md) and [**SWbemSecurity**](swbemsecurity.md) objects.</span></span>

<span data-ttu-id="a19e7-122">O nível de autenticação deve ser definido de acordo com os requisitos do sistema operacional de destino ao qual você está se conectando.</span><span class="sxs-lookup"><span data-stu-id="a19e7-122">The authentication level must be set according to the requirements of the target operating system to which you are connecting.</span></span> <span data-ttu-id="a19e7-123">Para obter mais informações, consulte [conectando entre diferentes sistemas operacionais](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span><span class="sxs-lookup"><span data-stu-id="a19e7-123">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="a19e7-124">O exemplo de código VBScript a seguir mostra como alterar o nível de autenticação em um script que obtém os dados de espaço livre de um computador remoto chamado "Server1".</span><span class="sxs-lookup"><span data-stu-id="a19e7-124">The following VBScript code example shows how to change the authentication level in a script that obtains the free space data from a remote computer named "Server1".</span></span>


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



<span data-ttu-id="a19e7-125">Em conexões de moniker de script para WMI, use o nome curto mostrado na coluna "nome do moniker/descrição" da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a19e7-125">In script moniker connections to WMI, use the short name shown in the "Moniker name/description" column of the table below.</span></span> <span data-ttu-id="a19e7-126">Por exemplo, no script a seguir, o nível de autenticação é definido como **WbemAuthenticationLevelPktIntegrity**.</span><span class="sxs-lookup"><span data-stu-id="a19e7-126">For example, in the following script, the authentication level is set to **WbemAuthenticationLevelPktIntegrity**.</span></span>


```VB
SetobjWMIService = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!root\cimv2")
```



<span data-ttu-id="a19e7-127">A tabela a seguir lista os níveis de autenticação que você pode definir.</span><span class="sxs-lookup"><span data-stu-id="a19e7-127">The following table lists the authentication levels you can set.</span></span> <span data-ttu-id="a19e7-128">Esses níveis são definidos em Wbemdisp. tlb na enumeração [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="a19e7-128">These levels are defined in Wbemdisp.tlb in the enumeration [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span>



| <span data-ttu-id="a19e7-129">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="a19e7-129">Name/value</span></span>                                                      | <span data-ttu-id="a19e7-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="a19e7-130">Description</span></span>                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a19e7-131">**WbemAuthenticationLevelDefault**</span><span class="sxs-lookup"><span data-stu-id="a19e7-131">**WbemAuthenticationLevelDefault**</span></span><br/> <span data-ttu-id="a19e7-132">0</span><span class="sxs-lookup"><span data-stu-id="a19e7-132">0</span></span><br/>      | <span data-ttu-id="a19e7-133">Moniker: padrão</span><span class="sxs-lookup"><span data-stu-id="a19e7-133">Moniker: Default</span></span><br/> <span data-ttu-id="a19e7-134">O WMI usa a configuração padrão de autenticação do Windows.</span><span class="sxs-lookup"><span data-stu-id="a19e7-134">WMI uses the default Windows authentication setting.</span></span> <span data-ttu-id="a19e7-135">Essa é a configuração recomendada que permite que o WMI negocie para o nível exigido pelo servidor que retorna dados.</span><span class="sxs-lookup"><span data-stu-id="a19e7-135">This is the recommended setting that allows WMI to negotiate to the level required by the server returning data.</span></span> <span data-ttu-id="a19e7-136">No entanto, se o namespace exigir criptografia, use **WbemAuthenticationLevelPktPrivacy**.</span><span class="sxs-lookup"><span data-stu-id="a19e7-136">However, if the namespace requires encryption, use **WbemAuthenticationLevelPktPrivacy**.</span></span><br/> |
| <span data-ttu-id="a19e7-137">**WbemAuthenticationLevelNone**</span><span class="sxs-lookup"><span data-stu-id="a19e7-137">**WbemAuthenticationLevelNone**</span></span><br/> <span data-ttu-id="a19e7-138">1</span><span class="sxs-lookup"><span data-stu-id="a19e7-138">1</span></span><br/>         | <span data-ttu-id="a19e7-139">Moniker: nenhum</span><span class="sxs-lookup"><span data-stu-id="a19e7-139">Moniker: None</span></span><br/> <span data-ttu-id="a19e7-140">Não usa autenticação.</span><span class="sxs-lookup"><span data-stu-id="a19e7-140">Uses no authentication.</span></span><br/>                                                                                                                                                                                                                                            |
| <span data-ttu-id="a19e7-141">**WbemAuthenticationLevelConnect**</span><span class="sxs-lookup"><span data-stu-id="a19e7-141">**WbemAuthenticationLevelConnect**</span></span><br/> <span data-ttu-id="a19e7-142">2</span><span class="sxs-lookup"><span data-stu-id="a19e7-142">2</span></span><br/>      | <span data-ttu-id="a19e7-143">Moniker: conectar</span><span class="sxs-lookup"><span data-stu-id="a19e7-143">Moniker: Connect</span></span><br/> <span data-ttu-id="a19e7-144">Autentica as credenciais do cliente somente quando o cliente estabelece uma relação com o servidor.</span><span class="sxs-lookup"><span data-stu-id="a19e7-144">Authenticates the credentials of the client only when the client establishes a relationship with the server.</span></span><br/>                                                                                                                                                    |
| <span data-ttu-id="a19e7-145">**WbemAuthenticationLevelCall**</span><span class="sxs-lookup"><span data-stu-id="a19e7-145">**WbemAuthenticationLevelCall**</span></span><br/> <span data-ttu-id="a19e7-146">3</span><span class="sxs-lookup"><span data-stu-id="a19e7-146">3</span></span><br/>         | <span data-ttu-id="a19e7-147">Chamar</span><span class="sxs-lookup"><span data-stu-id="a19e7-147">Call</span></span><br/> <span data-ttu-id="a19e7-148">Autentica somente no início de cada chamada quando o servidor recebe a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a19e7-148">Authenticates only at the beginning of each call when the server receives the request.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="a19e7-149">**WbemAuthenticationLevelPkt**</span><span class="sxs-lookup"><span data-stu-id="a19e7-149">**WbemAuthenticationLevelPkt**</span></span><br/> <span data-ttu-id="a19e7-150">4</span><span class="sxs-lookup"><span data-stu-id="a19e7-150">4</span></span><br/>          | <span data-ttu-id="a19e7-151">Moniker: PKT</span><span class="sxs-lookup"><span data-stu-id="a19e7-151">Moniker: Pkt</span></span><br/> <span data-ttu-id="a19e7-152">Autentica que todos os dados recebidos são do cliente esperado.</span><span class="sxs-lookup"><span data-stu-id="a19e7-152">Authenticates that all data received is from the expected client.</span></span><br/>                                                                                                                                                                                                   |
| <span data-ttu-id="a19e7-153">**WbemAuthenticationLevelPktIntegrity**</span><span class="sxs-lookup"><span data-stu-id="a19e7-153">**WbemAuthenticationLevelPktIntegrity**</span></span><br/> <span data-ttu-id="a19e7-154">5</span><span class="sxs-lookup"><span data-stu-id="a19e7-154">5</span></span><br/> | <span data-ttu-id="a19e7-155">Moniker: PktIntegrity</span><span class="sxs-lookup"><span data-stu-id="a19e7-155">Moniker: PktIntegrity</span></span><br/> <span data-ttu-id="a19e7-156">Autentica e verifica se nenhum dos dados transferidos entre o cliente e o servidor foi modificado.</span><span class="sxs-lookup"><span data-stu-id="a19e7-156">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="a19e7-157">**WbemAuthenticationLevelPktPrivacy**</span><span class="sxs-lookup"><span data-stu-id="a19e7-157">**WbemAuthenticationLevelPktPrivacy**</span></span><br/> <span data-ttu-id="a19e7-158">6</span><span class="sxs-lookup"><span data-stu-id="a19e7-158">6</span></span><br/>   | <span data-ttu-id="a19e7-159">Moniker: PktPrivacy</span><span class="sxs-lookup"><span data-stu-id="a19e7-159">Moniker: PktPrivacy</span></span><br/> <span data-ttu-id="a19e7-160">Autentica todos os níveis de representação anteriores e criptografa o valor do argumento de cada chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="a19e7-160">Authenticates all previous impersonation levels and encrypts the argument value of each remote procedure call.</span></span> <span data-ttu-id="a19e7-161">Use essa configuração se o namespace ao qual você está se conectando exigir uma conexão criptografada.</span><span class="sxs-lookup"><span data-stu-id="a19e7-161">Use this setting if the namespace to which you are connecting requires an encrypted connection.</span></span><br/>                                               |



 

<span data-ttu-id="a19e7-162">Para determinar uma chamada bem-sucedida, verifique o valor de retorno depois de alterar o nível de autenticação.</span><span class="sxs-lookup"><span data-stu-id="a19e7-162">To determine a successful call, check the return value after you change the authentication level.</span></span>

<span data-ttu-id="a19e7-163">Por exemplo, como as conexões locais sempre têm um nível de autenticação de **wbemAuthenticationLevelPktPrivacy**, o exemplo a seguir falha ao definir o nível de autenticação porque ele se conecta ao computador local.</span><span class="sxs-lookup"><span data-stu-id="a19e7-163">For example, because local connections always have an authentication level of **wbemAuthenticationLevelPktPrivacy**, the following example fails to set the authentication level because it connects to the local computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!" _
    & "\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="a19e7-164">Um provedor pode definir a segurança em um namespace para que nenhum dado seja retornado, a menos que você use a privacidade de pacote (PktPrivacy) em sua conexão com esse namespace.</span><span class="sxs-lookup"><span data-stu-id="a19e7-164">A provider can set the security on a namespace so that no data is returned unless you use packet privacy (PktPrivacy) in your connection to that namespace.</span></span> <span data-ttu-id="a19e7-165">Isso garante que os dados sejam criptografados enquanto atravessam a rede.</span><span class="sxs-lookup"><span data-stu-id="a19e7-165">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="a19e7-166">Se você tentar definir um nível de autenticação inferior, receberá uma mensagem de acesso negado.</span><span class="sxs-lookup"><span data-stu-id="a19e7-166">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="a19e7-167">Para obter mais informações, consulte [SECURING WMI namespaces](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="a19e7-167">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="changing-the-default-impersonation-levels-using-vbscript"></a><span data-ttu-id="a19e7-168">Alterando os níveis de representação padrão usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="a19e7-168">Changing the Default Impersonation Levels Using VBScript</span></span>

<span data-ttu-id="a19e7-169">Quando você faz chamadas para a API de script para WMI, é recomendável usar os padrões que o WMI fornece para o nível de representação.</span><span class="sxs-lookup"><span data-stu-id="a19e7-169">When you make calls to the Scripting API for WMI, it is recommended that you use the defaults that WMI provides for the impersonation level.</span></span> <span data-ttu-id="a19e7-170">Chamadas remotas e alguns provedores com mais de um salto de rede exigem um nível de representação mais alto do que o WMI usa.</span><span class="sxs-lookup"><span data-stu-id="a19e7-170">Remote calls and some providers with more than one network hop require a higher impersonation level than WMI uses.</span></span> <span data-ttu-id="a19e7-171">Se o nível de representação não for suficiente, um provedor poderá recusar uma solicitação ou fornecer informações incompletas.</span><span class="sxs-lookup"><span data-stu-id="a19e7-171">If the impersonation level is not sufficient, a provider might refuse a request or provide incomplete information.</span></span>

<span data-ttu-id="a19e7-172">Se você não definir o nível de representação em um moniker ou definindo [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) em um objeto protegível, defina o nível de representação DCOM padrão para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a19e7-172">If you do not set the impersonation level in either a moniker or by setting [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) on a securable object, then set the default DCOM impersonation level for the operating system.</span></span> <span data-ttu-id="a19e7-173">O nível de representação deve ser definido de acordo com os requisitos do sistema operacional de destino ao qual você está se conectando.</span><span class="sxs-lookup"><span data-stu-id="a19e7-173">The impersonation level must be set according to the requirements of the target operating system to which you are connecting.</span></span> <span data-ttu-id="a19e7-174">Para obter mais informações, consulte [conectando entre diferentes sistemas operacionais](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span><span class="sxs-lookup"><span data-stu-id="a19e7-174">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="a19e7-175">O exemplo de código VBScript a seguir mostra a alteração do nível de representação no mesmo script mostrado acima.</span><span class="sxs-lookup"><span data-stu-id="a19e7-175">The following VBScript code example shows changing the impersonation level in the same script shown above.</span></span>


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



<span data-ttu-id="a19e7-176">A tabela a seguir lista os níveis de autenticação em [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) que usam.</span><span class="sxs-lookup"><span data-stu-id="a19e7-176">The following table lists the authentication levels in [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) that use.</span></span>



| <span data-ttu-id="a19e7-177">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="a19e7-177">Name/value</span></span>                                                    | <span data-ttu-id="a19e7-178">Descrição</span><span class="sxs-lookup"><span data-stu-id="a19e7-178">Description</span></span>                                                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a19e7-179">**wbemImpersonationLevelAnonymous**</span><span class="sxs-lookup"><span data-stu-id="a19e7-179">**wbemImpersonationLevelAnonymous**</span></span><br/> <span data-ttu-id="a19e7-180">1</span><span class="sxs-lookup"><span data-stu-id="a19e7-180">1</span></span><br/>   | <span data-ttu-id="a19e7-181">Moniker: anônimo</span><span class="sxs-lookup"><span data-stu-id="a19e7-181">Moniker: Anonymous</span></span><br/> <span data-ttu-id="a19e7-182">Oculta as credenciais do autor da chamada.</span><span class="sxs-lookup"><span data-stu-id="a19e7-182">Hides the credentials of the caller.</span></span> <span data-ttu-id="a19e7-183">Chamadas ao WMI podem falhar com esse nível de representação.</span><span class="sxs-lookup"><span data-stu-id="a19e7-183">Calls to WMI may fail with this impersonation level.</span></span><br/>                                                                                                  |
| <span data-ttu-id="a19e7-184">**wbemImpersonationLevelIdentify**</span><span class="sxs-lookup"><span data-stu-id="a19e7-184">**wbemImpersonationLevelIdentify**</span></span><br/> <span data-ttu-id="a19e7-185">2</span><span class="sxs-lookup"><span data-stu-id="a19e7-185">2</span></span><br/>    | <span data-ttu-id="a19e7-186">Moniker: identificar</span><span class="sxs-lookup"><span data-stu-id="a19e7-186">Moniker: Identify</span></span><br/> <span data-ttu-id="a19e7-187">Permite que os objetos consultem as credenciais do autor da chamada.</span><span class="sxs-lookup"><span data-stu-id="a19e7-187">Allows objects to query the credentials of the caller.</span></span> <span data-ttu-id="a19e7-188">Chamadas ao WMI podem falhar com esse nível de representação.</span><span class="sxs-lookup"><span data-stu-id="a19e7-188">Calls to WMI may fail with this impersonation level.</span></span><br/>                                                                                 |
| <span data-ttu-id="a19e7-189">**wbemImpersonationLevelImpersonate**</span><span class="sxs-lookup"><span data-stu-id="a19e7-189">**wbemImpersonationLevelImpersonate**</span></span><br/> <span data-ttu-id="a19e7-190">3</span><span class="sxs-lookup"><span data-stu-id="a19e7-190">3</span></span><br/> | <span data-ttu-id="a19e7-191">Moniker: representar</span><span class="sxs-lookup"><span data-stu-id="a19e7-191">Moniker: Impersonate</span></span><br/> <span data-ttu-id="a19e7-192">Permite que os objetos utilizem as credenciais do autor da chamada.</span><span class="sxs-lookup"><span data-stu-id="a19e7-192">Allows objects to use the credentials of the caller.</span></span> <span data-ttu-id="a19e7-193">Esse é o nível de representação recomendado para a API de script para chamadas WMI.</span><span class="sxs-lookup"><span data-stu-id="a19e7-193">This is the recommended impersonation level for Scripting API for WMI calls.</span></span><br/>                                                        |
| <span data-ttu-id="a19e7-194">**wbemImpersonationLevelDelegate**</span><span class="sxs-lookup"><span data-stu-id="a19e7-194">**wbemImpersonationLevelDelegate**</span></span><br/> <span data-ttu-id="a19e7-195">4</span><span class="sxs-lookup"><span data-stu-id="a19e7-195">4</span></span><br/>    | <span data-ttu-id="a19e7-196">Moniker: delegado</span><span class="sxs-lookup"><span data-stu-id="a19e7-196">Moniker: Delegate</span></span><br/> <span data-ttu-id="a19e7-197">Autoriza que os objetos permitam que outros objetos utilizem as credenciais do autor da chamada.</span><span class="sxs-lookup"><span data-stu-id="a19e7-197">Allows objects to permit other objects to use the credentials of the caller.</span></span> <span data-ttu-id="a19e7-198">Essa representação funcionará com a API de script para chamadas WMI, mas pode constituir um risco de segurança desnecessário.</span><span class="sxs-lookup"><span data-stu-id="a19e7-198">This impersonation will work with Scripting API for WMI calls but may constitute an unnecessary security risk.</span></span><br/> |



 

<span data-ttu-id="a19e7-199">O exemplo a seguir mostra como definir a representação em uma cadeia de caracteres do moniker ao obter uma instância específica do [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="a19e7-199">The following example shows how to set the impersonation in a moniker string when obtaining a specific instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>


```VB
Set object = GetObject("winmgmts:{impersonationLevel=impersonate}!root\cimv2:Win32_Process.Handle='0'")
```



<span data-ttu-id="a19e7-200">Para obter mais informações, consulte [criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="a19e7-200">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

## <a name="setting-the-default-impersonation-level-using-the-registry"></a><span data-ttu-id="a19e7-201">Definindo o nível de representação padrão usando o registro</span><span class="sxs-lookup"><span data-stu-id="a19e7-201">Setting the Default Impersonation Level Using the Registry</span></span>

<span data-ttu-id="a19e7-202">Se você tiver acesso ao registro, também poderá definir a chave de registro de nível de representação padrão.</span><span class="sxs-lookup"><span data-stu-id="a19e7-202">If you have access to the registry, you can also set the default impersonation level registry key.</span></span> <span data-ttu-id="a19e7-203">Essa chave especifica qual nível de representação a API de script para WMI usa, a menos que especificado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="a19e7-203">This key specifies which impersonation level the Scripting API for WMI uses unless otherwise specified.</span></span> <span data-ttu-id="a19e7-204">O caminho a seguir identifica o caminho do registro.</span><span class="sxs-lookup"><span data-stu-id="a19e7-204">The following path identifies the registry path.</span></span>

<span data-ttu-id="a19e7-205">**HKEY \_ \_** Nível de \\  \\  \\  \\  \\ **representação padrão** do software Microsoft WBEM script do computador local</span><span class="sxs-lookup"><span data-stu-id="a19e7-205">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Impersonation Level**</span></span>

<span data-ttu-id="a19e7-206">Por padrão, a chave do registro é definida como 3, especificando o nível de representação Impersonate.</span><span class="sxs-lookup"><span data-stu-id="a19e7-206">By default, the registry key is set to 3, specifying the Impersonate impersonation level.</span></span> <span data-ttu-id="a19e7-207">Alguns provedores podem exigir um nível mais alto de representação.</span><span class="sxs-lookup"><span data-stu-id="a19e7-207">Some providers may require a higher level of impersonation.</span></span>

## <a name="accessing-the-swbemsecurity-object-in-vbscript"></a><span data-ttu-id="a19e7-208">Acessando o objeto SWbemSecurity no VBScript</span><span class="sxs-lookup"><span data-stu-id="a19e7-208">Accessing the SWbemSecurity Object in VBScript</span></span>

<span data-ttu-id="a19e7-209">A outra maneira de definir o nível de representação é a partir do objeto de segurança [**SWbemSecurity**](swbemsecurity.md) , que aparece como a propriedade de [**segurança \_**](swbemservices-security-.md) dos objetos [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemEventSource**](swbemeventsource.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="a19e7-209">The other way you can set the impersonation level is from the [**SWbemSecurity**](swbemsecurity.md) security object, which appears as the [**Security\_**](swbemservices-security-.md) property of the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemEventSource**](swbemeventsource.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects.</span></span>

<span data-ttu-id="a19e7-210">O WMI passa a configuração de segurança de um objeto pai para os descendentes do objeto original.</span><span class="sxs-lookup"><span data-stu-id="a19e7-210">WMI passes the security setting of a parent object to the descendants of the original object.</span></span> <span data-ttu-id="a19e7-211">Portanto, você pode definir o nível de representação de um objeto [**SWbemServices**](swbemservices.md) depois de fazer logon no WMI e em chamadas à API usando esse objeto ou objetos criados a partir dele, como objetos do tipo [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="a19e7-211">Therefore, you can set the impersonation level of an [**SWbemServices**](swbemservices.md) object after logging on to WMI and API calls using this object or objects created from it, such as objects of type [**SWbemObject**](swbemobject.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a19e7-212">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a19e7-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a19e7-213">Conectando-se ao WMI em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="a19e7-213">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="a19e7-214">Protegendo clientes de script</span><span class="sxs-lookup"><span data-stu-id="a19e7-214">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

