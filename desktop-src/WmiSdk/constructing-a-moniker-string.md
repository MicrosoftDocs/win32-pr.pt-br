---
description: O formato de cadeia de caracteres do moniker é semelhante ao de um caminho de objeto WMI padrão. Para obter mais informações, consulte requisitos de caminho do objeto WMI.
ms.assetid: 1aacc523-2a2f-43f5-96a3-aa0387cbae3e
ms.tgt_platform: multiple
title: Construindo uma cadeia de caracteres de moniker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e54e29b3c8f14890dc1cedd5907059308e8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296636"
---
# <a name="constructing-a-moniker-string"></a><span data-ttu-id="26d1d-104">Construindo uma cadeia de caracteres de moniker</span><span class="sxs-lookup"><span data-stu-id="26d1d-104">Constructing a Moniker String</span></span>

<span data-ttu-id="26d1d-105">O formato de cadeia de caracteres do moniker é semelhante ao de um caminho de objeto WMI padrão.</span><span class="sxs-lookup"><span data-stu-id="26d1d-105">The moniker string format is similar to that of a standard WMI object path.</span></span> <span data-ttu-id="26d1d-106">Para obter mais informações, consulte [requisitos de caminho do objeto WMI](wmi-object-path-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="26d1d-106">For more information, see [WMI Object Path Requirements](wmi-object-path-requirements.md).</span></span>

<span data-ttu-id="26d1d-107">Um moniker tem as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="26d1d-107">A moniker has the following parts:</span></span>

-   <span data-ttu-id="26d1d-108">O prefixo WinMgmts: (obrigatório).</span><span class="sxs-lookup"><span data-stu-id="26d1d-108">The prefix WinMgmts: (mandatory).</span></span> <span data-ttu-id="26d1d-109">O prefixo instrui o WSH (Windows Script Host) que o código a seguir usará os [objetos da API de script](scripting-api-objects.md).</span><span class="sxs-lookup"><span data-stu-id="26d1d-109">The prefix instructs the Windows Script Host (WSH) that the following code will be using the [Scripting API objects](scripting-api-objects.md).</span></span>
-   <span data-ttu-id="26d1d-110">Um componente de configurações de segurança (opcional)</span><span class="sxs-lookup"><span data-stu-id="26d1d-110">A security settings component (optional)</span></span>
-   <span data-ttu-id="26d1d-111">Um componente de caminho do objeto WMI (opcional)</span><span class="sxs-lookup"><span data-stu-id="26d1d-111">A WMI object path component (optional)</span></span>

<span data-ttu-id="26d1d-112">Você não pode especificar uma senha em uma cadeia de caracteres do moniker WMI.</span><span class="sxs-lookup"><span data-stu-id="26d1d-112">You cannot specify a password in a WMI moniker string.</span></span> <span data-ttu-id="26d1d-113">Se você precisar alterar a senha (parâmetro *strPassword* ) ou o tipo de autenticação (parâmetro *strAuthority* ) ao se conectar ao WMI, chame [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="26d1d-113">If you must change the password (*strPassword* parameter) or the type of authentication (*strAuthority* parameter) when connecting to WMI, then call [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="26d1d-114">Lembre-se de que você só pode especificar a senha e a autoridade em conexões com computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="26d1d-114">Be aware that you can only specify the password and authority in connections to remote computers.</span></span> <span data-ttu-id="26d1d-115">A tentativa de defini-los em um script em execução no computador local resulta em um erro.</span><span class="sxs-lookup"><span data-stu-id="26d1d-115">Attempting to set these in a script that is running on the local computer results in a error.</span></span> <span data-ttu-id="26d1d-116">Para obter mais informações sobre quando as configurações de segurança e os componentes do caminho do objeto são usados, consulte [configurações de segurança do WMI](/previous-versions/tn-archive/ee156574(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="26d1d-116">For more information about when the security settings and object path components are used, see [WMI Security Settings](/previous-versions/tn-archive/ee156574(v=technet.10)).</span></span>

<span data-ttu-id="26d1d-117">O moniker a seguir especifica o objeto [**SWbemServices**](swbemservices.md) que representa o padrão raiz do namespace \\ , com a representação on e o privilégio wbemPrivilegeDebug (SeDebugPrivilege) habilitado e o privilégio wbemPrivilegeSecurity (SeSecurityPrivilege) desabilitado.</span><span class="sxs-lookup"><span data-stu-id="26d1d-117">The following moniker specifies the [**SWbemServices**](swbemservices.md) object that represents the namespace root\\default, with impersonation on and the wbemPrivilegeDebug (SeDebugPrivilege) privilege enabled, and the wbemPrivilegeSecurity (SeSecurityPrivilege) privilege disabled.</span></span>


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> <span data-ttu-id="26d1d-118">Todas as literais de cadeia de caracteres não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="26d1d-118">All string literals are case-insensitive.</span></span>
>
> <span data-ttu-id="26d1d-119">O prefixo "!" em um privilégio indica que o privilégio deve ser desabilitado; a omissão desse prefixo indica que o privilégio deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="26d1d-119">The "!" prefix on a privilege indicates that the privilege is to be disabled; the omission of this prefix implies that the privilege is to be enabled.</span></span>
>
> <span data-ttu-id="26d1d-120">O prefixo "!" é usado no nome do computador ou namespace quando as configurações de segurança são especificadas entre colchetes antes do nome do computador ou namespace.</span><span class="sxs-lookup"><span data-stu-id="26d1d-120">The "!" prefix is used on the computer name or namespace when security settings are specified in brackets before the computer name or namespace.</span></span>

 

<span data-ttu-id="26d1d-121">As atribuições padrão a seguir são permitidas ao especificar o caminho do objeto:</span><span class="sxs-lookup"><span data-stu-id="26d1d-121">The following default assignments are allowed when specifying the object path:</span></span>

-   <span data-ttu-id="26d1d-122">O nome da máquina do computador pode ser omitido do caminho do objeto; nesse caso, o nome do computador local é assumido.</span><span class="sxs-lookup"><span data-stu-id="26d1d-122">The computer machine name can be omitted from the object path, in which case the local machine name is assumed.</span></span>
-   <span data-ttu-id="26d1d-123">O namespace pode ser omitido do caminho do objeto; nesse caso, o namespace padrão é assumido.</span><span class="sxs-lookup"><span data-stu-id="26d1d-123">The namespace can be omitted from the object path, in which case the default namespace is assumed.</span></span>

    <span data-ttu-id="26d1d-124">Isso é determinado pelo valor da chave do registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **scripting** \\ **padrão namespace**, o valor padrão é "root \\ CIMv2".</span><span class="sxs-lookup"><span data-stu-id="26d1d-124">This is determined by the value of the registry key **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Namespace**, the default value is "Root\\CIMv2".</span></span>

-   <span data-ttu-id="26d1d-125">Uma classe ou instância também pode ser especificada; nesse caso, o objeto retornado é um objeto WMI em vez de um objeto de serviços.</span><span class="sxs-lookup"><span data-stu-id="26d1d-125">A class or instance can also be specified, in which case the returned object is a WMI object rather than a services object.</span></span>

> [!Note]  
> <span data-ttu-id="26d1d-126">Se uma classe ou instância for especificada, você não poderá omitir o namespace ao especificar o nome da máquina do computador.</span><span class="sxs-lookup"><span data-stu-id="26d1d-126">If a class or instance is specified, you cannot omit the namespace when specifying the computer machine name.</span></span>

 

<span data-ttu-id="26d1d-127">Para obter uma referência das constantes de privilégio usadas na cadeia de caracteres do moniker WMI, consulte [constantes de privilégio](privilege-constants.md)e os descritores de "nome curto de script".</span><span class="sxs-lookup"><span data-stu-id="26d1d-127">For a reference of the Privilege Constants used on WMI moniker string, see [Privilege Constants](privilege-constants.md), and the "Scripting short name" descriptors.</span></span>

## <a name="valid-moniker-strings"></a><span data-ttu-id="26d1d-128">Cadeias de caracteres de moniker válidas</span><span class="sxs-lookup"><span data-stu-id="26d1d-128">Valid Moniker Strings</span></span>

<span data-ttu-id="26d1d-129">Os exemplos a seguir mostram cadeias de caracteres de moniker válidas.</span><span class="sxs-lookup"><span data-stu-id="26d1d-129">The following examples show valid moniker strings.</span></span>

<span data-ttu-id="26d1d-130">O moniker a seguir identifica o namespace padrão no computador local.</span><span class="sxs-lookup"><span data-stu-id="26d1d-130">The following moniker identifies the default namespace on the local computer.</span></span> <span data-ttu-id="26d1d-131">Um objeto [**SWbemServices**](swbemservices.md) é retornado.</span><span class="sxs-lookup"><span data-stu-id="26d1d-131">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
WinMgmts:
```



<span data-ttu-id="26d1d-132">O moniker a seguir identifica o namespace padrão no computador meuservidor.</span><span class="sxs-lookup"><span data-stu-id="26d1d-132">The following moniker identifies the default namespace on the computer myServer.</span></span> <span data-ttu-id="26d1d-133">Um objeto [**SWbemServices**](swbemservices.md) é retornado.</span><span class="sxs-lookup"><span data-stu-id="26d1d-133">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts://myServer"
```



<span data-ttu-id="26d1d-134">O moniker a seguir identifica o \\ namespace raiz cimv2 no computador meuservidor.</span><span class="sxs-lookup"><span data-stu-id="26d1d-134">The following moniker identifies the root\\cimv2 namespace on the myServer computer.</span></span> <span data-ttu-id="26d1d-135">Um objeto [**SWbemServices**](swbemservices.md) é retornado.</span><span class="sxs-lookup"><span data-stu-id="26d1d-135">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts://myServer/root/cimv2"
```



<span data-ttu-id="26d1d-136">O moniker a seguir identifica o \\ namespace raiz cimv2 no servidor local.</span><span class="sxs-lookup"><span data-stu-id="26d1d-136">The following moniker identifies the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="26d1d-137">Um objeto [**SWbemServices**](swbemservices.md) é retornado.</span><span class="sxs-lookup"><span data-stu-id="26d1d-137">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts:root/cimv2"
```



<span data-ttu-id="26d1d-138">O moniker a seguir identifica a classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) no \\ namespace raiz cimv2 no servidor meuservidor.</span><span class="sxs-lookup"><span data-stu-id="26d1d-138">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the root\\cimv2 namespace on the myServer server.</span></span> <span data-ttu-id="26d1d-139">Um objeto [**SWbemObject**](swbemobject.md) é retornado.</span><span class="sxs-lookup"><span data-stu-id="26d1d-139">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



<span data-ttu-id="26d1d-140">O moniker a seguir identifica a classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) no \\ namespace raiz cimv2 no servidor local.</span><span class="sxs-lookup"><span data-stu-id="26d1d-140">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="26d1d-141">Um objeto [**SWbemObject**](swbemobject.md) é retornado.</span><span class="sxs-lookup"><span data-stu-id="26d1d-141">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



<span data-ttu-id="26d1d-142">O moniker a seguir identifica a classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) no namespace padrão no servidor local.</span><span class="sxs-lookup"><span data-stu-id="26d1d-142">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the default namespace on the local server.</span></span> <span data-ttu-id="26d1d-143">Um objeto [**SWbemObject**](swbemobject.md) é retornado.</span><span class="sxs-lookup"><span data-stu-id="26d1d-143">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



<span data-ttu-id="26d1d-144">O moniker a seguir identifica a instância [**do \_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondente à unidade C: no namespace de script padrão no servidor local.</span><span class="sxs-lookup"><span data-stu-id="26d1d-144">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the default scripting namespace on the local server.</span></span> <span data-ttu-id="26d1d-145">Um objeto [**SWbemObject**](swbemobject.md) é retornado.</span><span class="sxs-lookup"><span data-stu-id="26d1d-145">An [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="26d1d-146">O namespace padrão para scripts é determinado pela definição de configuração de namespace padrão, conforme especificado no controle WMI.</span><span class="sxs-lookup"><span data-stu-id="26d1d-146">The default namespace for scripting is determined by the default namespace configuration setting as specified in the WMI Control.</span></span> <span data-ttu-id="26d1d-147">Para obter mais informações, consulte [definindo a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="26d1d-147">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



<span data-ttu-id="26d1d-148">O moniker a seguir identifica a instância [**do \_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondente à unidade C: no \\ namespace raiz cimv2 no servidor meuservidor.</span><span class="sxs-lookup"><span data-stu-id="26d1d-148">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the root\\cimv2 namespace on the myServer server.</span></span> <span data-ttu-id="26d1d-149">Um objeto [**SWbemObject**](swbemobject.md) é retornado.</span><span class="sxs-lookup"><span data-stu-id="26d1d-149">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



<span data-ttu-id="26d1d-150">O moniker a seguir identifica a instância [**do \_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondente à unidade C: no \\ namespace raiz cimv2 no servidor local.</span><span class="sxs-lookup"><span data-stu-id="26d1d-150">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="26d1d-151">Um objeto [**SWbemObject**](swbemobject.md) é retornado.</span><span class="sxs-lookup"><span data-stu-id="26d1d-151">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



<span data-ttu-id="26d1d-152">O moniker a seguir identifica a instância [**do \_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondente à unidade C: no namespace padrão no servidor local.</span><span class="sxs-lookup"><span data-stu-id="26d1d-152">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the default namespace on the local server.</span></span> <span data-ttu-id="26d1d-153">Um objeto [**SWbemObject**](swbemobject.md) é retornado.</span><span class="sxs-lookup"><span data-stu-id="26d1d-153">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



<span data-ttu-id="26d1d-154">O moniker a seguir define o nível de representação para representar e define o \_ privilégio de depuração se.</span><span class="sxs-lookup"><span data-stu-id="26d1d-154">The following moniker sets the impersonation level to impersonate and sets the SE\_DEBUG privilege.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



<span data-ttu-id="26d1d-155">O moniker a seguir define o nível de representação para representar e define o \_ privilégio de depuração se.</span><span class="sxs-lookup"><span data-stu-id="26d1d-155">The following moniker sets the impersonation level to impersonate and sets the SE\_DEBUG privilege.</span></span> <span data-ttu-id="26d1d-156">Ele também revoga o privilégio de \_ desligamento se.</span><span class="sxs-lookup"><span data-stu-id="26d1d-156">It also revokes the SE\_SHUTDOWN privilege.</span></span>


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



<span data-ttu-id="26d1d-157">O moniker a seguir recupera descrições localizadas do inglês americano para a classe **MyClass** do \\ namespace WMI raiz.</span><span class="sxs-lookup"><span data-stu-id="26d1d-157">The following moniker retrieves American English localized descriptions for the **myclass** class from the root\\wmi namespace.</span></span>


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



<span data-ttu-id="26d1d-158">O moniker a seguir solicita a autenticação Kerberos usando o servidor principal mydomain \\ .</span><span class="sxs-lookup"><span data-stu-id="26d1d-158">The following moniker requests Kerberos authentication using the principal mydomain\\server.</span></span>


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



<span data-ttu-id="26d1d-159">O moniker a seguir solicita a autenticação NTLM usando o domínio mydomain.</span><span class="sxs-lookup"><span data-stu-id="26d1d-159">The following moniker requests NTLM authentication using the mydomain domain.</span></span>


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



<span data-ttu-id="26d1d-160">O exemplo de código VBScript a seguir mostra como combinar parâmetros de segurança e localidade em um moniker.</span><span class="sxs-lookup"><span data-stu-id="26d1d-160">The following VBScript code example shows how to combine security and locale parameters in a moniker.</span></span>


```VB
'*****************************************************************
'   Name    :  Moniker.vbs
'
'   Purpose :  This example shows how to set various 
'              parameters in a moniker. 
'****************************************************************

Set myobj = GetObject("WINMGMTS:" _
            & "{impersonationLevel=impersonate," _
            & "authenticationLevel=pktPrivacy," _
            & "authority=ntlmdomain:mydomain," _
            & "(Debug,!Shutdown)}" _
            & "[locale=ms_409]" _
            & "!\\User1\ROOT\CIMV2:Win32_LogicalDisk=""C:""")

wscript.echo "File system = " & myobj.filesystem
```



> [!Note]
>
> Embora os monikers forneçam acesso mais direto a objetos, em determinadas circunstâncias, o uso repetido de monikers pode ser menos eficiente do que o código equivalente que se conecta explicitamente ao WMI. <span data-ttu-id="26d1d-162">Se o desempenho do aplicativo for uma consideração, considere usar os mecanismos alternativos.</span><span class="sxs-lookup"><span data-stu-id="26d1d-162">If application performance is a consideration, consider using the alternative mechanisms.</span></span>
>
> <span data-ttu-id="26d1d-163">Não é possível usar a função **GetObject** fornecida pelo VBScript para atualizar ou definir dados ao executar scripts inseridos em uma página HTML, pois o Microsoft Internet Explorer nega o uso dessa chamada por motivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="26d1d-163">It is not possible to use the **GetObject** function provided by VBScript to update or set data when running scripts embedded within an HTML page, as Microsoft Internet Explorer denies the use of this call for security reasons.</span></span>

 

 

 
