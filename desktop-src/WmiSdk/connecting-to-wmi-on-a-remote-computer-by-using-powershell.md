---
description: Conectando-se ao WMI remotamente com o PowerShell
ms.assetid: 9a06f0c3-2845-48aa-9988-79cc4607ce19
ms.tgt_platform: multiple
title: Conectando-se ao WMI remotamente com o PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a2bb1ad982a20a10dbadd89856d118f1be9bd82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661844"
---
# <a name="connecting-to-wmi-remotely-with-powershell"></a><span data-ttu-id="d8429-103">Conectando-se ao WMI remotamente com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="d8429-103">Connecting to WMI Remotely with PowerShell</span></span>

<span data-ttu-id="d8429-104">O Windows PowerShell fornece um mecanismo simples para se conectar ao Instrumentação de Gerenciamento do Windows (WMI) em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="d8429-104">Windows PowerShell provides a simple mechanism to connect to Windows Management Instrumentation (WMI) on a remote computer.</span></span> <span data-ttu-id="d8429-105">As conexões remotas no WMI são afetadas pelo [Firewall do Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), pelas configurações do DCOM e pelo [UAC (controle de conta de usuário)](/previous-versions/aa905108(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="d8429-105">Remote connections in WMI are affected by the [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), DCOM settings, and [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)).</span></span> <span data-ttu-id="d8429-106">Para obter mais informações sobre como configurar conexões remotas, consulte [conectando-se ao WMI remotamente a partir do Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="d8429-106">For more information about configuring remote connections, see [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

<span data-ttu-id="d8429-107">Os exemplos neste tópico baseiam-se nos VBScripts de [se conectar ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="d8429-107">The examples in this topic are based on the VBScripts from [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="d8429-108">Todos os exemplos neste tópico usam o cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="d8429-108">All of the examples in this topic use the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="d8429-109">Para obter mais informações, consulte [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="d8429-109">For more information, see [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span></span>

## <a name="windows-powershell-examples"></a><span data-ttu-id="d8429-110">Exemplos do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d8429-110">Windows PowerShell examples</span></span>

<span data-ttu-id="d8429-111">Ao criar uma conexão com um computador remoto, um usuário pode especificar as informações de conexão, como o nome do computador remoto, as credenciais e o nível de autenticação da conexão.</span><span class="sxs-lookup"><span data-stu-id="d8429-111">When creating a connection to a remote computer, a user can specify the connection information such as the remote computer name, credentials, and the authentication level for the connection.</span></span> <span data-ttu-id="d8429-112">Os exemplos a seguir ilustram como se conectar a um computador remoto usando diferentes conjuntos de credenciais e como acessar informações do WMI.</span><span class="sxs-lookup"><span data-stu-id="d8429-112">The following examples illustrate how to connect to a remote computer by using different sets of credentials and how to access WMI information.</span></span>

<span data-ttu-id="d8429-113">O exemplo do Windows PowerShell a seguir mostra a configuração do nível de representação:</span><span class="sxs-lookup"><span data-stu-id="d8429-113">The following Windows PowerShell example shows setting the impersonation level:</span></span>


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



<span data-ttu-id="d8429-114">No exemplo anterior, o usuário se conecta a um computador remoto usando as mesmas credenciais (domínio e nome de usuário) com as quais ele fez logon.</span><span class="sxs-lookup"><span data-stu-id="d8429-114">In the preceding example, the user connects to a remote computer by using the same credentials (domain and user name) that they logged on with.</span></span> <span data-ttu-id="d8429-115">O usuário também solicitou o uso da representação.</span><span class="sxs-lookup"><span data-stu-id="d8429-115">The user also requested to use impersonation.</span></span> <span data-ttu-id="d8429-116">Ao contrário do exemplo original do VBScript, uma cadeia de caracteres do moniker não é necessária porque o nível de representação é definido pela propriedade "impersonation".</span><span class="sxs-lookup"><span data-stu-id="d8429-116">Unlike the original VBScript example, a moniker string is not needed because the impersonation level is set by the "Impersonation" property.</span></span> <span data-ttu-id="d8429-117">Por padrão, o nível de representação é definido como 3 (representar).</span><span class="sxs-lookup"><span data-stu-id="d8429-117">By default, the impersonation level is set to 3 (Impersonate).</span></span>

<span data-ttu-id="d8429-118">O exemplo lista todas as instâncias da classe [**de \_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) que estão sendo executadas no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="d8429-118">The example lists all the instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class that are running on remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="d8429-119">Você deve especificar o namespace do WMI para se conectar ao no computador remoto, pois é possível que o namespace padrão não seja o mesmo em computadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="d8429-119">You should specify the WMI namespace to connect to on the remote computer because it is possible that the default namespace is not the same on different computers.</span></span>

 

<span data-ttu-id="d8429-120">O exemplo do Windows PowerShell a seguir mostra como se conectar a um computador remoto com credenciais diferentes e definir o nível de representação como 3, que é Impersonate:</span><span class="sxs-lookup"><span data-stu-id="d8429-120">The following Windows PowerShell example shows how to connect to a remote computer with different credentials and to set the impersonation level to 3, which is Impersonate:</span></span>


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



<span data-ttu-id="d8429-121">No exemplo anterior, o nome do computador foi atribuído à variável $Computer.</span><span class="sxs-lookup"><span data-stu-id="d8429-121">In the preceding example, the computer name was assigned to the $Computer variable.</span></span> <span data-ttu-id="d8429-122">O usuário se conecta a um computador remoto usando credenciais específicas (domínio e nome de usuário) e solicita a representação para o nível de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d8429-122">The user connects to a remote computer by using specific credentials (domain and user name) and requests impersonation for the authentication level.</span></span>

> [!Note]  
> <span data-ttu-id="d8429-123">O caractere de acento grave ( \` ) é usado para indicar uma quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="d8429-123">The grave-accent character (\`) is used to indicate a line break.</span></span> <span data-ttu-id="d8429-124">É equivalente ao caractere de sublinhado ( \_ ) no VBScript.</span><span class="sxs-lookup"><span data-stu-id="d8429-124">It is equivalent to the underscore character (\_) in VBScript.</span></span>

 

<span data-ttu-id="d8429-125">O exemplo do Windows PowerShell a seguir se conecta a um grupo de computadores remotos no mesmo domínio criando uma matriz de nomes de computadores remotos e, em seguida, exibindo os nomes dos dispositivos Plug and Play — instâncias do [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)— em cada computador:</span><span class="sxs-lookup"><span data-stu-id="d8429-125">The following Windows PowerShell example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer:</span></span>


```PowerShell
$ArrComputers = "Computer1", "Computer2", "Computer3"
foreach ($Computer in $ArrComputers) 
{
write-host ""
write-host "===================================="
write-host "Computer: $Computer"
write-host "===================================="

write-host "-----------------------------------"
write-host "Win32_PnPEntity instance"
write-host "-----------------------------------"

$ColItems = Get-WmiObject -Class Win32_PnPEntity -Namespace "root\cimv2" -Computer $Computer
$ColItems[0..47] | Format-List Name, Status
}
```



> [!Note]  
> <span data-ttu-id="d8429-126">Para executar o script do Windows PowerShell anterior, você deve ser um administrador nos computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="d8429-126">To run the preceding Windows PowerShell script, you must be an administrator on the remote computers.</span></span> <span data-ttu-id="d8429-127">Além disso, relacionado ao exemplo anterior, observe o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d8429-127">Also, relating to the preceding example, note the following:</span></span>

 

-   <span data-ttu-id="d8429-128">Os nomes dos computadores na matriz devem ser colocados entre aspas porque são cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d8429-128">The computer names in the array must be enclosed in quotation marks because they are strings.</span></span>
-   <span data-ttu-id="d8429-129">Os objetos retornados pelo [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) são atribuídos à variável $ColItems.</span><span class="sxs-lookup"><span data-stu-id="d8429-129">The objects returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) are assigned to the $ColItems variable.</span></span>
-   <span data-ttu-id="d8429-130">O operador de intervalo \[ \] limitou a lista de dispositivos Plug and Play a 48 instâncias.</span><span class="sxs-lookup"><span data-stu-id="d8429-130">The range operator \[\] limited the list of Plug and Play devices to 48 instances.</span></span> <span data-ttu-id="d8429-131">Para obter mais informações, consulte [about \_ Operators](/previous-versions//dd347588(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="d8429-131">For more information, see [About\_Operators](/previous-versions//dd347588(v=technet.10)).</span></span>
-   <span data-ttu-id="d8429-132">O " \| " é o caractere de pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8429-132">The "\|" is the pipeline character.</span></span> <span data-ttu-id="d8429-133">O objeto retornado por ColItems é enviado para o cmdlet [Format-List]( /previous-versions//dd347700(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="d8429-133">The object returned by ColItems is sent to the [Format-List]( /previous-versions//dd347700(v=technet.10)) cmdlet.</span></span>

<span data-ttu-id="d8429-134">O exemplo do Windows PowerShell a seguir permite que você se conecte a um computador remoto em um domínio diferente.</span><span class="sxs-lookup"><span data-stu-id="d8429-134">The following Windows PowerShell example enables you to connect to a remote computer on a different domain.</span></span> <span data-ttu-id="d8429-135">Este exemplo também exibe os nomes de processo para instâncias [**do \_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="d8429-135">This example also displays the process names for instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) on the remote computer.</span></span>


```PowerShell
$Computer = "FullComputerName" 
$Domain = "DOMAIN"
$Credential = Get-Credential
$ColItems = Get-WmiObject -Class Win32_Process -Authority "ntlmdomain:$Domain" `
-Credential $Credential -Locale "MS_409" -Namespace "root\cimv2"  -ComputerName $Computer

foreach ($ObjItem in $colItems) 
{
write-host "Process Name:" $ObjItem.name
}
```



> [!Note]  
> <span data-ttu-id="d8429-136">Para executar o script do Windows PowerShell anterior, você deve ser um administrador no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="d8429-136">To run the preceding Windows PowerShell script, you must be an administrator on the remote computer.</span></span>

 

<span data-ttu-id="d8429-137">No exemplo anterior, o usuário se conecta a um computador remoto em um domínio diferente e especifica uma localidade preferencial.</span><span class="sxs-lookup"><span data-stu-id="d8429-137">In the preceding example, the user connects to a remote computer on a different domain and specifies a preferred locale.</span></span> <span data-ttu-id="d8429-138">O comando [Get-Credential](/previous-versions//dd315327(v=technet.10)) solicita as credenciais do usuário e atribui as credenciais a um objeto.</span><span class="sxs-lookup"><span data-stu-id="d8429-138">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) command requests the user's credentials and assigns the credentials to an object.</span></span> <span data-ttu-id="d8429-139">O exemplo também lista os nomes de instâncias da classe [**de \_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) que estão em execução no computador.</span><span class="sxs-lookup"><span data-stu-id="d8429-139">The example also lists the names of instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class that are running on the computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8429-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8429-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8429-141">Conectando-se ao WMI em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="d8429-141">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
