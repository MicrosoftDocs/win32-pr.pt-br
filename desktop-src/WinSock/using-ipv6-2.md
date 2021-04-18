---
description: No Windows XP posterior, uma nova ferramenta de linha de comando é fornecida para configurar e gerenciar o IPv4. Essa ferramenta usa o \# comando &0034; netsh interface ip&\# 0034; para configurar e gerenciar o IPv4.
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: Usando IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f759d938ebebbc0ddfbb2326dfb10932c16310a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807787"
---
# <a name="using-ipv6"></a><span data-ttu-id="40333-104">Usando IPv6</span><span class="sxs-lookup"><span data-stu-id="40333-104">Using IPv6</span></span>

<span data-ttu-id="40333-105">No Windows XP posterior, uma nova ferramenta de linha de comando é fornecida para configurar e gerenciar o IPv4.</span><span class="sxs-lookup"><span data-stu-id="40333-105">On Windows XP a later, a new command-line tool is provided for configuring and managing IPv4.</span></span> <span data-ttu-id="40333-106">Essa ferramenta usa o comando "netsh interface IP" para configurar e gerenciar o IPv4.</span><span class="sxs-lookup"><span data-stu-id="40333-106">This tool uses the "netsh interface ip" command for configuring and managing IPv4.</span></span>

<span data-ttu-id="40333-107">No Windows XP com Service Pack 1 (SP1) e posterior, essa nova ferramenta de linha de comando foi aprimorada para dar suporte à configuração e ao gerenciamento do IPv6.</span><span class="sxs-lookup"><span data-stu-id="40333-107">On Windows XP with Service Pack 1 (SP1) and later, this new command-line tool was enhanced to support the configuration and management of IPv6.</span></span> <span data-ttu-id="40333-108">Essa ferramenta aprimorada é o comando "netsh interface IPv6".</span><span class="sxs-lookup"><span data-stu-id="40333-108">This enhanced tool is the "netsh interface ipv6" command.</span></span> <span data-ttu-id="40333-109">As alterações de configuração feitas usando os comandos Netsh.exe são permanentes e não são perdidas quando o computador ou o protocolo IPv6 é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="40333-109">Configuration changes made using the Netsh.exe commands are permanent and are not lost when the computer or the IPv6 protocol is restarted.</span></span>

<span data-ttu-id="40333-110">O comando a seguir está disponível no Windows XP com SP1 e versões posteriores para consultar e configurar o IPv6 em um computador local:</span><span class="sxs-lookup"><span data-stu-id="40333-110">The following command is available on Windows XP with SP1 and later to query and configure IPv6 on a local computer:</span></span>

-   [<span data-ttu-id="40333-111">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="40333-111">Netsh.exe</span></span>](netsh-exe.md)

<span data-ttu-id="40333-112">Antes do Windows XP com Service Pack 1 (SP1), a configuração e o gerenciamento do IPv6 usaram várias ferramentas de linha de comando mais antigas para configurar e gerenciar o IPv6.</span><span class="sxs-lookup"><span data-stu-id="40333-112">Prior to Windows XP with Service Pack 1 (SP1), IPv6 configuration and management used several older command-line tools to configure and manage IPv6.</span></span> <span data-ttu-id="40333-113">Usando essas ferramentas mais antigas, as alterações de IPv6 não são permanentes e são perdidas quando o computador ou o protocolo IPv6 foi reiniciado.</span><span class="sxs-lookup"><span data-stu-id="40333-113">Using these older tools, the IPv6 changes are not permanent and are lost when the computer or the IPv6 protocol was restarted.</span></span>

<span data-ttu-id="40333-114">Os comandos mais antigos a seguir estão disponíveis no Windows XP</span><span class="sxs-lookup"><span data-stu-id="40333-114">The following older commands are available on Windows XP</span></span>

-   [<span data-ttu-id="40333-115">Net.exe</span><span class="sxs-lookup"><span data-stu-id="40333-115">Net.exe</span></span>](net-exe-2.md)
-   [<span data-ttu-id="40333-116">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="40333-116">Ipv6.exe</span></span>](ipv6-exe-2.md)
-   [<span data-ttu-id="40333-117">Ipsec6.exe</span><span class="sxs-lookup"><span data-stu-id="40333-117">Ipsec6.exe</span></span>](ipsec6-exe-2.md)

<span data-ttu-id="40333-118">Essas ferramentas mais antigas também foram fornecidas na versão prévia da tecnologia IPv6 para Windows 2000</span><span class="sxs-lookup"><span data-stu-id="40333-118">These older tools were also provided in the IPv6 Technology Preview for Windows 2000</span></span>

<span data-ttu-id="40333-119">As alterações de configuração usando essas ferramentas mais antigas podem ser mantidas colocando-as como linhas de comando em um arquivo de script de comando (. cmd) que é executado após a reinicialização do computador ou do protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="40333-119">Configuration changes using these older tools could be maintained by placing them as command lines in a command script file (.cmd) that is run after restarting the computer or the IPv6 protocol.</span></span> <span data-ttu-id="40333-120">Para restabelecer as alterações de configuração automaticamente após a reinicialização, é possível usar as tarefas agendadas do Windows para executar o arquivo. cmd quando o computador é iniciado.</span><span class="sxs-lookup"><span data-stu-id="40333-120">To reinstate configuration changes automatically after restarting, is was possible to use the Windows Scheduled Tasks to run the .cmd file when the computer starts.</span></span>

<span data-ttu-id="40333-121">Essas ferramentas mais antigas não são fornecidas no Windows Server 2003 e posterior.</span><span class="sxs-lookup"><span data-stu-id="40333-121">These older tools are not provided on Windows Server 2003 and later.</span></span> <span data-ttu-id="40333-122">A ferramenta "netsh interface IPv6" é fornecida para configurar e gerenciar o IPv6 a partir da linha de comando no Windows Server 2003 e posterior.</span><span class="sxs-lookup"><span data-stu-id="40333-122">The "netsh interface ipv6" tool is provided for configuring and managing IPv6 from the command-line on Windows Server 2003 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40333-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40333-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40333-124">Protocolo IP versão 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="40333-124">Internet Protocol Version 6 (IPv6)</span></span>](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[<span data-ttu-id="40333-125">Guia IPv6 para aplicativos do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="40333-125">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="40333-126">Versão prévia da tecnologia IPv6 para Windows 2000</span><span class="sxs-lookup"><span data-stu-id="40333-126">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



