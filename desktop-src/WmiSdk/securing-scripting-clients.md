---
description: Scripts e Visual Basic aplicativos devem definir a segurança DCOM, especialmente para acesso remoto, e também podem precisar habilitar privilégios.
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: Protegendo clientes de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c58a3dbade78b1dd81b0bf89eb867d8cd5c2f265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165205"
---
# <a name="securing-scripting-clients"></a><span data-ttu-id="fb69f-103">Protegendo clientes de script</span><span class="sxs-lookup"><span data-stu-id="fb69f-103">Securing Scripting Clients</span></span>

<span data-ttu-id="fb69f-104">Scripts e Visual Basic aplicativos devem definir a segurança DCOM, especialmente para acesso remoto, e também podem precisar habilitar privilégios.</span><span class="sxs-lookup"><span data-stu-id="fb69f-104">Scripts and Visual Basic applications must set DCOM security, especially for remote access, and may also need to enable privileges.</span></span>

## <a name="default-access-permissions"></a><span data-ttu-id="fb69f-105">Permissões de acesso padrão</span><span class="sxs-lookup"><span data-stu-id="fb69f-105">Default Access Permissions</span></span>

<span data-ttu-id="fb69f-106">O acesso ao WMI é diferente entre computadores locais e remotos.</span><span class="sxs-lookup"><span data-stu-id="fb69f-106">WMI access differs between local and remote computers.</span></span> <span data-ttu-id="fb69f-107">Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="fb69f-107">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="fb69f-108">A seguir estão as permissões de acesso padrão por conta:</span><span class="sxs-lookup"><span data-stu-id="fb69f-108">The following are the default access permissions by account:</span></span>

-   <span data-ttu-id="fb69f-109">Todos, LocalService, NetworkService</span><span class="sxs-lookup"><span data-stu-id="fb69f-109">Everyone, LocalService, NetworkService</span></span>

    <span data-ttu-id="fb69f-110">Permissão para ler ou gravar dados e para executar [*métodos de provedor*](gloss-p.md) no computador local.</span><span class="sxs-lookup"><span data-stu-id="fb69f-110">Permission to read or write data and to run [*provider methods*](gloss-p.md) on the local computer.</span></span> <span data-ttu-id="fb69f-111">Essas contas não podem criar novas classes ou instalar novos provedores.</span><span class="sxs-lookup"><span data-stu-id="fb69f-111">These accounts cannot create new classes or install new providers.</span></span>

-   <span data-ttu-id="fb69f-112">Contas de administrador</span><span class="sxs-lookup"><span data-stu-id="fb69f-112">Administrator accounts</span></span>

    <span data-ttu-id="fb69f-113">Controle total no computador local.</span><span class="sxs-lookup"><span data-stu-id="fb69f-113">Full control on local computer.</span></span> <span data-ttu-id="fb69f-114">Ao se conectar a um computador remoto, a conta deve ser um administrador local no computador remoto também.</span><span class="sxs-lookup"><span data-stu-id="fb69f-114">When connecting to a remote computer, the account must be a local administrator on the remote computer also.</span></span>

## <a name="securing-a-scripting-client"></a><span data-ttu-id="fb69f-115">Protegendo um cliente de script</span><span class="sxs-lookup"><span data-stu-id="fb69f-115">Securing a Scripting Client</span></span>

<span data-ttu-id="fb69f-116">Os aplicativos de script e Visual Basic do WMI devem definir os níveis de segurança do DCOM adequadamente para os sistemas operacionais aos quais eles estão direcionados.</span><span class="sxs-lookup"><span data-stu-id="fb69f-116">WMI scripting and Visual Basic applications must set DCOM security levels appropriately for the operating systems they are targeting.</span></span> <span data-ttu-id="fb69f-117">Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="fb69f-117">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="fb69f-118">Ao se conectar a um computador remoto, talvez seja necessário alterar o serviço (NTLM ou Kerberos) que manipula a autenticação.</span><span class="sxs-lookup"><span data-stu-id="fb69f-118">When connecting to a remote computer, you may need to change the service (NTLM or Kerberos) that handles authentication.</span></span> <span data-ttu-id="fb69f-119">Para obter mais informações, consulte [definindo o serviço de autenticação usando o VBScript](setting-the-authentication-service-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="fb69f-119">For more information, see [Setting the Authentication Service Using VBScript](setting-the-authentication-service-using-vbscript.md).</span></span>

<span data-ttu-id="fb69f-120">O acesso a algumas classes ou dados WMI pode exigir um privilégio que não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="fb69f-120">Access to some WMI classes or data may require a privilege that is not enabled.</span></span> <span data-ttu-id="fb69f-121">Por exemplo, você deve incluir o privilégio de segurança ao se conectar à classe [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fb69f-121">For example, you must include the Security privilege when connecting to the [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) class.</span></span> <span data-ttu-id="fb69f-122">Para obter mais informações, consulte [executando operações privilegiadas usando o VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="fb69f-122">For more information, see [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="fb69f-123">Se você estiver acessando o WMI de uma página de Active Server (ASP), algumas configurações do IIS serão necessárias.</span><span class="sxs-lookup"><span data-stu-id="fb69f-123">If you are accessing WMI from an Active Server Page (ASP), then some IIS configuration is required.</span></span> <span data-ttu-id="fb69f-124">Para obter mais informações, consulte [Configuring IIS 5,0 and posterior for WMI ASP scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="fb69f-124">For more information, see [Configuring IIS 5.0 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span></span>

<span data-ttu-id="fb69f-125">Você pode estar tentando se conectar a um namespace que requer uma conexão criptografada, em outras palavras, uma que exija um nível de autenticação de pktPrivacy.</span><span class="sxs-lookup"><span data-stu-id="fb69f-125">You may be trying to connect to a namespace which requires an encrypted connection, in other words, one that requires an authentication level of pktPrivacy.</span></span> <span data-ttu-id="fb69f-126">Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="fb69f-126">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

 

 
