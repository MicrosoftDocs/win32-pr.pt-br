---
title: BITS Compact Server
description: O Serviço de Transferência Inteligente em Segundo Plano (BITS) Compact Server é um servidor de arquivos HTTP/HTTPS autônomo que fornece a capacidade de transferir um número limitado de arquivos grandes de forma assíncrona entre computadores.
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40e2840c24e15379fac11a5a12ed76c225e7be5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823883"
---
# <a name="bits-compact-server"></a><span data-ttu-id="b81f9-103">BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="b81f9-103">BITS Compact Server</span></span>

<span data-ttu-id="b81f9-104">O Serviço de Transferência Inteligente em Segundo Plano (BITS) Compact Server é um servidor de arquivos HTTP/HTTPS autônomo que fornece a capacidade de transferir um número limitado de arquivos grandes de forma assíncrona entre computadores.</span><span class="sxs-lookup"><span data-stu-id="b81f9-104">The Background Intelligent Transfer Service (BITS) Compact Server is a stand-alone HTTP/HTTPS file server that provides the ability to transfer a limited number of large files asynchronously between computers.</span></span> <span data-ttu-id="b81f9-105">O servidor Compact é criado como um serviço NT e usa HTTP.SYS.</span><span class="sxs-lookup"><span data-stu-id="b81f9-105">The Compact Server is built as an NT Service and uses HTTP.SYS.</span></span>

<span data-ttu-id="b81f9-106">O BITS Compact Server destina-se a ser usado por clientes empresariais e de pequenas empresas sob as seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="b81f9-106">The BITS Compact Server is intended for use by enterprise and small business customers under the following conditions:</span></span>

-   <span data-ttu-id="b81f9-107">O uso antecipado é de, no máximo, 25 grupos de URLs, e cada grupo de URLs dá suporte a três transferências de arquivo simultâneas.</span><span class="sxs-lookup"><span data-stu-id="b81f9-107">The anticipated usage is a maximum of 25 URL groups, and each URL group supports 3 simultaneous file transfers.</span></span>
-   <span data-ttu-id="b81f9-108">As transferências de arquivos ocorrem entre computadores no mesmo domínio ou domínios mutuamente confiáveis.</span><span class="sxs-lookup"><span data-stu-id="b81f9-108">File transfers occur between computers in the same domain or mutually trusted domains.</span></span>
-   <span data-ttu-id="b81f9-109">As transferências de arquivo não são destinadas a clientes voltados para a Internet.</span><span class="sxs-lookup"><span data-stu-id="b81f9-109">File transfers are not intended for Internet-facing clients.</span></span>

## <a name="installing-the-bits-compact-server"></a><span data-ttu-id="b81f9-110">Instalando o BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="b81f9-110">Installing the BITS Compact Server</span></span>

<span data-ttu-id="b81f9-111">O BITS Compact Server é um componente de servidor opcional.</span><span class="sxs-lookup"><span data-stu-id="b81f9-111">The BITS Compact Server is an optional server component.</span></span> <span data-ttu-id="b81f9-112">Você pode usar uma das seguintes opções para instalar o BITS Compact Server:</span><span class="sxs-lookup"><span data-stu-id="b81f9-112">You can use one of the following options to install the BITS Compact Server:</span></span>

-   <span data-ttu-id="b81f9-113">Gerenciador do Servidor</span><span class="sxs-lookup"><span data-stu-id="b81f9-113">Server Manager</span></span>

-   <span data-ttu-id="b81f9-114">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b81f9-114">Windows PowerShell</span></span>

-   <span data-ttu-id="b81f9-115">Gerenciador de Pacotes</span><span class="sxs-lookup"><span data-stu-id="b81f9-115">Package Manager</span></span>

<span data-ttu-id="b81f9-116">**Para instalar o BITS Compact Server usando Gerenciador do Servidor**</span><span class="sxs-lookup"><span data-stu-id="b81f9-116">**To install the BITS Compact Server by using Server Manager**</span></span>

1.  <span data-ttu-id="b81f9-117">Na seção **Resumo de recursos** do **Gerenciador do servidor**, clique em **Adicionar recursos**.</span><span class="sxs-lookup"><span data-stu-id="b81f9-117">In the **Features Summary** section of the **Server Manager**, click **Add Features**.</span></span>
2.  <span data-ttu-id="b81f9-118">No Assistente para adicionar recursos, selecione **serviço de transferência inteligente em segundo plano (bits)** e o **Compact Server**.</span><span class="sxs-lookup"><span data-stu-id="b81f9-118">In the Add Features Wizard, select **Background Intelligent Transfer Service (BITS)** and **Compact Server**.</span></span>
3.  <span data-ttu-id="b81f9-119">Siga as instruções do assistente, incluindo a instalação do software necessário, se indicado.</span><span class="sxs-lookup"><span data-stu-id="b81f9-119">Follow the wizard instructions, including installing the required software if indicated.</span></span>

<span data-ttu-id="b81f9-120">Para obter mais informações, consulte a ajuda online do **Gerenciador do servidor** .</span><span class="sxs-lookup"><span data-stu-id="b81f9-120">For more information, see the **Server Manager** online help.</span></span>

<span data-ttu-id="b81f9-121">**Para instalar o BITS Compact Server usando o Windows PowerShell**</span><span class="sxs-lookup"><span data-stu-id="b81f9-121">**To install the BITS Compact Server by using Windows PowerShell**</span></span>

1.  <span data-ttu-id="b81f9-122">Em um prompt de comando do Windows PowerShell, digite o seguinte comando: **Import-Module ServerManager**.</span><span class="sxs-lookup"><span data-stu-id="b81f9-122">In a Windows PowerShell command prompt, type the following command: **Import-Module ServerManager**.</span></span> <span data-ttu-id="b81f9-123">Em seguida, pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="b81f9-123">Then press Enter.</span></span>
2.  <span data-ttu-id="b81f9-124">Digite o seguinte comando: **Add-WINDOWSFEATURE bits-Compact-Server**.</span><span class="sxs-lookup"><span data-stu-id="b81f9-124">Type the following command: **Add-WindowsFeature BITS-Compact-Server**.</span></span> <span data-ttu-id="b81f9-125">Em seguida, pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="b81f9-125">Then press Enter.</span></span>

<span data-ttu-id="b81f9-126">O exemplo com base em texto a seguir demonstra como instalar o BITS Compact Server usando cmdlets do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b81f9-126">The following text-based example demonstrates installing the BITS Compact Server using Windows PowerShell cmdlets.</span></span>

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

<span data-ttu-id="b81f9-127">Para obter informações sobre como usar cmdlets, consulte a documentação do [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="b81f9-127">For information about using cmdlets, see the [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) documentation.</span></span>

<span data-ttu-id="b81f9-128">Para obter mais informações sobre o cmdlet Import-Module, consulte [Import-Module](/previous-versions//dd347701(v=technet.10)) na biblioteca do Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="b81f9-128">For more information about the Import-Module cmdlet, see [Import-Module](/previous-versions//dd347701(v=technet.10)) in the Microsoft TechNet Library.</span></span> <span data-ttu-id="b81f9-129">Para obter ajuda na linha de comando, digite **Get-Help Import-Module**.</span><span class="sxs-lookup"><span data-stu-id="b81f9-129">For help at the command line, type **get-help import-module**.</span></span>

<span data-ttu-id="b81f9-130">Para obter mais informações sobre o cmdlet Add-WindowsFeature, consulte [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) na biblioteca do Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="b81f9-130">For more information about the Add-WindowsFeature cmdlet, see [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) in the Microsoft TechNet Library.</span></span> <span data-ttu-id="b81f9-131">Para obter ajuda na linha de comando, digite **Get-Help Add-WindowsFeature**.</span><span class="sxs-lookup"><span data-stu-id="b81f9-131">For help at the command line, type **get-help Add-WindowsFeature**.</span></span>

<span data-ttu-id="b81f9-132">**Para instalar o BITS Compact Server usando o Gerenciador de pacotes**</span><span class="sxs-lookup"><span data-stu-id="b81f9-132">**To install the BITS Compact Server by using Package Manager**</span></span>

-   <span data-ttu-id="b81f9-133">Digite o seguinte comando: **PkgMgr.exe/IU: LightweightServer**.</span><span class="sxs-lookup"><span data-stu-id="b81f9-133">Enter the following command: **PkgMgr.exe /iu:LightweightServer**.</span></span>

> [!Note]  
> <span data-ttu-id="b81f9-134">As configurações serão perdidas se o serviço do Compact Server for reiniciado ou se o computador for reinicializado.</span><span class="sxs-lookup"><span data-stu-id="b81f9-134">The settings are lost if the Compact Server service is restarted or if the computer is rebooted.</span></span>

 

## <a name="bits-compact-server-remote-management"></a><span data-ttu-id="b81f9-135">Gerenciamento remoto do BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="b81f9-135">BITS Compact Server Remote Management</span></span>

<span data-ttu-id="b81f9-136">O BITS Compact Server com gerenciamento remoto de BITS permite transferências de arquivos remotas mais seguras.</span><span class="sxs-lookup"><span data-stu-id="b81f9-136">The BITS Compact Server with BITS Remote Management enables more secure remote file transfers.</span></span> <span data-ttu-id="b81f9-137">O gerenciamento remoto de BITS usa um provedor de Instrumentação de Gerenciamento do Windows (WMI) para permitir que um administrador de sistema ou um aplicativo de controlador crie remotamente trabalhos de transferência de BITS nos clientes e publique arquivos para hospedagem no BITS Compact Server.</span><span class="sxs-lookup"><span data-stu-id="b81f9-137">BITS Remote Management uses a Windows Management Instrumentation (WMI) provider to let a system administrator or a controller application remotely create BITS transfer jobs on the clients and to publish files for hosting on the BITS Compact Server.</span></span> <span data-ttu-id="b81f9-138">O provedor BITS também pode ser usado para permitir que um aplicativo use remotamente o cliente BITS em conjunto com o BITS Compact Server para transferir arquivos de um computador remoto para outro computador remoto.</span><span class="sxs-lookup"><span data-stu-id="b81f9-138">The BITS provider can also be used to enable an application to remotely use the BITS client in conjunction with the BITS Compact Server to transfer files from one remote computer to another remote computer.</span></span>

<span data-ttu-id="b81f9-139">Para obter mais informações, consulte a documentação do [provedor bits](/previous-versions/windows/desktop/bitsprov/bits-provider) .</span><span class="sxs-lookup"><span data-stu-id="b81f9-139">For more information, see the [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b81f9-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b81f9-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b81f9-141">Provedor de BITS</span><span class="sxs-lookup"><span data-stu-id="b81f9-141">BITS provider</span></span>](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 