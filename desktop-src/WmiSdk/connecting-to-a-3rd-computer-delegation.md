---
description: Quando você executa um script em um sistema local que obtém dados de um sistema remoto, o WMI fornece suas credenciais para o provedor de dados no sistema remoto.
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: Delegando com WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8a624f3d437d977ff73b3854a59cfd634350e7
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104370824"
---
# <a name="delegating-with-wmi"></a><span data-ttu-id="ca27b-103">Delegando com WMI</span><span class="sxs-lookup"><span data-stu-id="ca27b-103">Delegating with WMI</span></span>

<span data-ttu-id="ca27b-104">Quando você executa um script em um sistema local que obtém dados de um sistema remoto, o WMI fornece suas credenciais para o provedor de dados no sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="ca27b-104">When you run a script on a local system that obtains data from a remote system, WMI supplies your credentials to the provider of the data on the remote system.</span></span> <span data-ttu-id="ca27b-105">Isso requer apenas um nível de representação de **Impersonate**, pois apenas um salto de rede é necessário.</span><span class="sxs-lookup"><span data-stu-id="ca27b-105">This requires only an impersonation level of **Impersonate**, because only one network hop is required.</span></span> <span data-ttu-id="ca27b-106">No entanto, se o script se conectar ao WMI no sistema remoto e tentar abrir um arquivo de log em um sistema remoto adicional, o script falhará, a menos que o nível de representação seja **delegado**.</span><span class="sxs-lookup"><span data-stu-id="ca27b-106">However, if the script connects to WMI on the remote system and attempts to open a log file on an additional remote system, then the script fails unless the impersonation level is **Delegate**.</span></span> <span data-ttu-id="ca27b-107">O nível de representação de **delegado** é exigido por qualquer operação que envolva mais de um salto de rede.</span><span class="sxs-lookup"><span data-stu-id="ca27b-107">**Delegate** impersonation level is required by any operation that involves more than one network hop.</span></span> <span data-ttu-id="ca27b-108">Para obter mais informações sobre segurança DCOM no WMI, consulte [definindo a segurança do processo do aplicativo cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="ca27b-108">For more information about DCOM security in WMI, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="ca27b-109">Para obter mais informações sobre uma conexão de salto de uma rede entre dois computadores, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="ca27b-109">For more information about a one-network hop connection between two computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="ca27b-110">**Para usar a delegação para se conectar a um computador por meio de outro computador**</span><span class="sxs-lookup"><span data-stu-id="ca27b-110">**To use delegation to connect to a computer through another computer**</span></span>

1.  <span data-ttu-id="ca27b-111">Habilite a delegação no Active Directory (**Active Directory usuários e computadores** em **tarefas administrativas** do **painel de controle** ) no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="ca27b-111">Enable delegation in Active Directory (**Active Directory Users and Computers** in **Control Panel** **Administrative Tasks**) on the domain controller.</span></span> <span data-ttu-id="ca27b-112">A conta no sistema remoto deve ser marcada como **confiável para delegação** e a conta no sistema local não deve ser marcada, pois a **conta é confidencial e não pode ser delegada**.</span><span class="sxs-lookup"><span data-stu-id="ca27b-112">The account on the remote system must be marked as **Trusted for delegation** and the account on the local system must not be marked as **Account is sensitive and cannot be delegated**.</span></span> <span data-ttu-id="ca27b-113">o sistema local, o sistema remoto e o controlador de domínio devem ser membros do mesmo domínio ou em domínios confiáveis.</span><span class="sxs-lookup"><span data-stu-id="ca27b-113">the local system, the remote system, and the domain controller must be members of the same domain or in trusted domains.</span></span>

    <span data-ttu-id="ca27b-114">**Observação**  Usar a delegação é um risco de segurança, pois fornece aos processos fora do seu controle direto a capacidade de usar suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="ca27b-114">**Note**  Using delegation is a security risk because it gives processes outside of your direct control the ability to use your credentials.</span></span>

2.  <span data-ttu-id="ca27b-115">Modifique seu código da maneira a seguir para indicar que você deseja usar a delegação.</span><span class="sxs-lookup"><span data-stu-id="ca27b-115">Modify your code in the following manner to indicate that you want to use delegation.</span></span>

    <dl> <dt>

    <span data-ttu-id="ca27b-116"><span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell</span><span class="sxs-lookup"><span data-stu-id="ca27b-116"><span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell</span></span>
    </dt> <dd>

    <span data-ttu-id="ca27b-117">Defina o parâmetro *-Impersonation* no cmdlet do WMI como **delegado**.</span><span class="sxs-lookup"><span data-stu-id="ca27b-117">Set the *-Impersonation* parameter on the WMI cmdlet to **Delegate**.</span></span>

    </dd> <dt>

    <span data-ttu-id="ca27b-118"><span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript</span><span class="sxs-lookup"><span data-stu-id="ca27b-118"><span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript</span></span>
    </dt> <dd>

    <span data-ttu-id="ca27b-119">Defina o parâmetro *ImpersonationLevel* para **delegar** na chamada para [SWbemLocator. ConnectServer](swbemlocator-connectserver.md) ou **delegado** na cadeia de caracteres do [moniker](constructing-a-moniker-string.md) .</span><span class="sxs-lookup"><span data-stu-id="ca27b-119">Set the *impersonationLevel* parameter to **Delegate** in the call to [SWbemLocator.ConnectServer](swbemlocator-connectserver.md) or **Delegate** in the [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="ca27b-120">Você também pode definir a representação em um objeto [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="ca27b-120">You can also set the impersonation in a [**SWbemSecurity**](swbemsecurity.md)object.</span></span>

    </dd> <dt>

    <span data-ttu-id="ca27b-121"><span id="C__"></span><span id="c__"></span>C++</span><span class="sxs-lookup"><span data-stu-id="ca27b-121"><span id="C__"></span><span id="c__"></span>C++</span></span>
    </dt> <dd>

    <span data-ttu-id="ca27b-122">Defina o parâmetro de nível de representação para o **delegado de nível de imp do RPC \_ C \_ \_ \_** na chamada para [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="ca27b-122">Set the impersonation level parameter to **RPC\_C\_IMP\_LEVEL\_DELEGATE** in the call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="ca27b-123">Para obter mais informações sobre quando fazer essas chamadas, consulte [Inicializando com para um aplicativo WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="ca27b-123">For more information about when to make these calls, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="ca27b-124">Para passar a identidade do cliente para servidores COM remotos em C++, defina o encobrimento na chamada para [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="ca27b-124">To pass the client identity to remote COM servers in C++, set cloaking in the call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="ca27b-125">Para obter mais informações, consulte [encobrindo](../com/cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="ca27b-125">For more information, see [Cloaking](../com/cloaking.md).</span></span>

    </dd> </dl>

## <a name="examples"></a><span data-ttu-id="ca27b-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca27b-126">Examples</span></span>

<span data-ttu-id="ca27b-127">O exemplo de código a seguir mostra uma cadeia de caracteres do moniker que define a representação a ser **delegada**.</span><span class="sxs-lookup"><span data-stu-id="ca27b-127">The following code example shows a moniker string that sets the impersonation to **Delegate**.</span></span> <span data-ttu-id="ca27b-128">Lembre-se de que a autoridade deve ser definida como Kerberos.</span><span class="sxs-lookup"><span data-stu-id="ca27b-128">Be aware that the authority must be set to Kerberos.</span></span>


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



<span data-ttu-id="ca27b-129">O exemplo de código a seguir mostra como definir a representação para **delegar** (um valor de 4) usando [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="ca27b-129">The following code example shows how to set impersonation to **Delegate** (a value of 4) using [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span>


```vb
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = objLocator.ConnectServer(Computer_B, _
                                             "Root\CIMv2", _
                                             AdminAccount, _
                                             MyPassword, _
                                             "kerberos:Domain\Computer_B")
objWMIService.Security_.ImpersonationLevel = 4
```



## <a name="related-topics"></a><span data-ttu-id="ca27b-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca27b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca27b-131">Protegendo uma conexão WMI remota</span><span class="sxs-lookup"><span data-stu-id="ca27b-131">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> <dt>

[<span data-ttu-id="ca27b-132">Criando processos remotamente com o WMI</span><span class="sxs-lookup"><span data-stu-id="ca27b-132">Creating Processes Remotely with WMI</span></span>](creating-processes-remotely.md)
</dt> </dl>

 

 
