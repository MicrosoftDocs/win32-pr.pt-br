---
description: Os comandos netsh para IPv6 fornecem uma ferramenta de linha de comando que você pode usar para consultar e configurar interfaces, endereços, caches e rotas IPv6. Os comandos IPv6 da interface netsh têm suporte no Windows XP com Service Pack 1 (SP1) e posterior.
ms.assetid: 68e17a55-4dd5-40cd-8996-25fa278ddd19
title: Netsh.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab092def0dc12071ee9dd62fd7554a53c9a7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090369"
---
# <a name="netshexe"></a><span data-ttu-id="baf6a-104">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="baf6a-104">Netsh.exe</span></span>

<span data-ttu-id="baf6a-105">Os comandos netsh para IPv6 fornecem uma ferramenta de linha de comando que você pode usar para consultar e configurar interfaces, endereços, caches e rotas IPv6.</span><span class="sxs-lookup"><span data-stu-id="baf6a-105">The Netsh commands for IPv6 provide a command-line tool that you can use to query and configure IPv6 interfaces, address, caches, and routes.</span></span> <span data-ttu-id="baf6a-106">Os comandos IPv6 da interface netsh têm suporte no Windows XP com Service Pack 1 (SP1) e posterior.</span><span class="sxs-lookup"><span data-stu-id="baf6a-106">The Netsh interface IPv6 commands are supported on Windows XP with Service Pack 1 (SP1) and later.</span></span>

<span data-ttu-id="baf6a-107">Netsh.exe tem muitos subcomandos para IPv6.</span><span class="sxs-lookup"><span data-stu-id="baf6a-107">Netsh.exe has many subcommands for IPv6.</span></span> <span data-ttu-id="baf6a-108">Uma lista completa de opções para a interface netsh IPv6 está disponível no prompt de comando do Windows XP com SP1 e posterior, digitando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="baf6a-108">A complete list of options for Netsh Interface IPv6 is available from the command prompt on Windows XP with SP1 and later by typing the following:</span></span>

<span data-ttu-id="baf6a-109">**interface netsh IPv6/?**</span><span class="sxs-lookup"><span data-stu-id="baf6a-109">**netsh interface ipv6 /?**</span></span>

<span data-ttu-id="baf6a-110">A documentação sobre todos os comandos **netsh** para IPv6 também está disponível online no TechNet.</span><span class="sxs-lookup"><span data-stu-id="baf6a-110">Documentation on all of the **netsh** commands for IPv6 is also available online on Technet.</span></span> <span data-ttu-id="baf6a-111">Para obter mais informações sobre o **netsh** no Windows Server 2008, consulte [comandos netsh para interface (IPv4 e IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="baf6a-111">For more information on **netsh** on Windows Server 2008, please see [Netsh commands for Interface (IPv4 and IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)).</span></span> <span data-ttu-id="baf6a-112">Para obter mais informações sobre o **netsh** no Windows Server 2003, consulte [comandos netsh para interface IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="baf6a-112">For more information on **netsh** on Windows Server 2003, please see [Netsh commands for Interface IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).</span></span>

<span data-ttu-id="baf6a-113">Estes são alguns comandos usados com frequência para IPv6, embora haja suporte para muitos outros comandos:</span><span class="sxs-lookup"><span data-stu-id="baf6a-113">The following are a few commonly used commands for IPv6, although many other commands are supported:</span></span>

<dl> <dt>

<span data-ttu-id="baf6a-114"><span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**Adicionar endereço IPv6 da interface netsh**</span><span class="sxs-lookup"><span data-stu-id="baf6a-114"><span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface ipv6 add address**</span></span>
</dt> <dd>

<span data-ttu-id="baf6a-115">Adiciona um endereço IPv6 a uma interface específica no computador local.</span><span class="sxs-lookup"><span data-stu-id="baf6a-115">Adds an IPv6 address to a specific interface on the local computer.</span></span> <span data-ttu-id="baf6a-116">Este comando tem parâmetros de subopção que devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="baf6a-116">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="baf6a-117"><span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface ipv6 add DNS**</span><span class="sxs-lookup"><span data-stu-id="baf6a-117"><span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface ipv6 add dns**</span></span>
</dt> <dd>

<span data-ttu-id="baf6a-118">Adiciona um endereço IPv6 do servidor DNS à lista configurada estaticamente de servidores DNS para a interface especificada no computador local.</span><span class="sxs-lookup"><span data-stu-id="baf6a-118">Adds a DNS server IPv6 address to the statically-configured list of DNS servers for the specified interface on the local computer.</span></span> <span data-ttu-id="baf6a-119">Este comando tem parâmetros de subopção que devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="baf6a-119">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="baf6a-120"><span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface IPv6 adicionar rota**</span><span class="sxs-lookup"><span data-stu-id="baf6a-120"><span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add route**</span></span>
</dt> <dd>

<span data-ttu-id="baf6a-121">Adiciona uma rota para um endereço de prefixo IPv6 especificado no computador local.</span><span class="sxs-lookup"><span data-stu-id="baf6a-121">Adds a route for a specified IPv6 prefix address on the local computer.</span></span> <span data-ttu-id="baf6a-122">Este comando tem parâmetros de subopção que devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="baf6a-122">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="baf6a-123"><span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**excluir endereço IPv6 da interface netsh**</span><span class="sxs-lookup"><span data-stu-id="baf6a-123"><span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**netsh interface ipv6 delete address**</span></span>
</dt> <dd>

<span data-ttu-id="baf6a-124">Exclui o endereço IPv6 especificado de uma interface específica no computador local.</span><span class="sxs-lookup"><span data-stu-id="baf6a-124">Deletes the specified IPv6 address from a specific interface on the local computer.</span></span> <span data-ttu-id="baf6a-125">Este comando tem parâmetros de subopção que devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="baf6a-125">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="baf6a-126"><span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface IPv6 Delete DNS**</span><span class="sxs-lookup"><span data-stu-id="baf6a-126"><span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface ipv6 delete dns**</span></span>
</dt> <dd>

<span data-ttu-id="baf6a-127">Exclui um endereço do servidor DNS da lista de servidores DNS configurada estaticamente para a interface especificada no computador local.</span><span class="sxs-lookup"><span data-stu-id="baf6a-127">Deletes a DNS server address from the statically-configured list of DNS servers for the specified interface on the local computer.</span></span> <span data-ttu-id="baf6a-128">Este comando tem parâmetros de subopção que devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="baf6a-128">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="baf6a-129"><span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**interface netsh interface IPv6 Delete**</span><span class="sxs-lookup"><span data-stu-id="baf6a-129"><span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**netsh interface ipv6 delete interface**</span></span>
</dt> <dd>

<span data-ttu-id="baf6a-130">Exclui uma interface especificada da pilha IPv6 no computador local.</span><span class="sxs-lookup"><span data-stu-id="baf6a-130">Deletes a specified interface from the IPv6 stack on the local computer.</span></span> <span data-ttu-id="baf6a-131">Este comando tem parâmetros de subopção que devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="baf6a-131">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="baf6a-132"><span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface IPv6 excluir rota**</span><span class="sxs-lookup"><span data-stu-id="baf6a-132"><span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface ipv6 delete route**</span></span>
</dt> <dd>

<span data-ttu-id="baf6a-133">Exclui uma rota para um endereço de prefixo IPv6 especificado no computador local.</span><span class="sxs-lookup"><span data-stu-id="baf6a-133">Deletes a route for a specified IPv6 prefix address on the local computer.</span></span> <span data-ttu-id="baf6a-134">Este comando tem parâmetros de subopção que devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="baf6a-134">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="baf6a-135"><span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**despejo de IPv6 da interface netsh**</span><span class="sxs-lookup"><span data-stu-id="baf6a-135"><span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**netsh interface ipv6 dump**</span></span>
</dt> <dd>

<span data-ttu-id="baf6a-136">Cria um script que contém os comandos para criar a configuração atual.</span><span class="sxs-lookup"><span data-stu-id="baf6a-136">Creates a script that contains the commands to create the current configuration.</span></span> <span data-ttu-id="baf6a-137">Se for salvo em um arquivo, esse script poderá ser usado para restaurar as definições de configuração alteradas.</span><span class="sxs-lookup"><span data-stu-id="baf6a-137">If saved to a file, this script can be used to restore altered configuration settings.</span></span>

</dd> <dt>

<span data-ttu-id="baf6a-138"><span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**instalação do IPv6 da interface netsh**</span><span class="sxs-lookup"><span data-stu-id="baf6a-138"><span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**netsh interface ipv6 install**</span></span>
</dt> <dd>

<span data-ttu-id="baf6a-139">Instala o protocolo IPv6 no computador local.</span><span class="sxs-lookup"><span data-stu-id="baf6a-139">Installs the IPv6 protocol on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="baf6a-140"><span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**renovar IPv6 da interface netsh**</span><span class="sxs-lookup"><span data-stu-id="baf6a-140"><span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface ipv6 renew**</span></span>
</dt> <dd>

<span data-ttu-id="baf6a-141">Reinicia as interfaces IPv6 no computador local.</span><span class="sxs-lookup"><span data-stu-id="baf6a-141">Restarts the IPv6 interfaces on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="baf6a-142"><span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**redefinição de IPv6 da interface netsh**</span><span class="sxs-lookup"><span data-stu-id="baf6a-142"><span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**netsh interface ipv6 reset**</span></span>
</dt> <dd>

<span data-ttu-id="baf6a-143">Redefine o estado de configuração do IPv6 no computador local.</span><span class="sxs-lookup"><span data-stu-id="baf6a-143">Resets the IPv6 configuration state on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="baf6a-144"><span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**</span><span class="sxs-lookup"><span data-stu-id="baf6a-144"><span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**</span></span>
</dt> <dd>

<span data-ttu-id="baf6a-145">Exibe os parâmetros de configuração global para IPv6 no computador local.</span><span class="sxs-lookup"><span data-stu-id="baf6a-145">Displays the global configuration parameters for IPv6 on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="baf6a-146"><span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface IPv6 Mostrar endereço**</span><span class="sxs-lookup"><span data-stu-id="baf6a-146"><span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface ipv6 show address**</span></span>
</dt> <dd>

<span data-ttu-id="baf6a-147">Exibe todos os endereços IPv6 ou todos os endereços IPv6 em uma interface específica no computador local.</span><span class="sxs-lookup"><span data-stu-id="baf6a-147">Displays all IPv6 addresses or all IPv6 addresses on a specific interface on the local computer.</span></span> <span data-ttu-id="baf6a-148">Esse comando tem parâmetros de subopção que talvez precisem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="baf6a-148">This command has suboption parameters that may need to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="baf6a-149"><span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**desinstalação do IPv6 da interface netsh**</span><span class="sxs-lookup"><span data-stu-id="baf6a-149"><span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**netsh interface ipv6 uninstall**</span></span>
</dt> <dd>

<span data-ttu-id="baf6a-150">Desinstala o protocolo IPv6 no computador local.</span><span class="sxs-lookup"><span data-stu-id="baf6a-150">Uninstalls the IPv6 protocol on the local computer.</span></span>

</dd> </dl>

## <a name="netsh-commands-for-ipv4"></a><span data-ttu-id="baf6a-151">Comandos netsh para IPv4</span><span class="sxs-lookup"><span data-stu-id="baf6a-151">Netsh commands for IPv4</span></span>

<span data-ttu-id="baf6a-152">Comandos netsh semelhantes estão disponíveis para IPv4.</span><span class="sxs-lookup"><span data-stu-id="baf6a-152">Similar Netsh commands are available for IPv4.</span></span> <span data-ttu-id="baf6a-153">Uma lista completa de opções para comandos netsh para uso com IPv4 está disponível no prompt de comando do Windows XP com SP1 e posterior, digitando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="baf6a-153">A complete list of options for Netsh commands for use with IPv4 is available from the command prompt on Windows XP with SP1 and later by typing the following:</span></span>

<span data-ttu-id="baf6a-154">**netsh interface IP/?**</span><span class="sxs-lookup"><span data-stu-id="baf6a-154">**netsh interface ip /?**</span></span>

<span data-ttu-id="baf6a-155">A documentação sobre todos os comandos netsh para IPv4 também está disponível online no TechNet.</span><span class="sxs-lookup"><span data-stu-id="baf6a-155">Documentation on all of the Netsh commands for IPv4 is also available online on Technet.</span></span> <span data-ttu-id="baf6a-156">Para obter mais informações, consulte [comandos netsh para IP de interface](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="baf6a-156">For more information, please see [Netsh commands for Interface IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))</span></span>

 

 
