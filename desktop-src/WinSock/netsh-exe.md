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
# <a name="netshexe"></a>Netsh.exe

Os comandos netsh para IPv6 fornecem uma ferramenta de linha de comando que você pode usar para consultar e configurar interfaces, endereços, caches e rotas IPv6. Os comandos IPv6 da interface netsh têm suporte no Windows XP com Service Pack 1 (SP1) e posterior.

Netsh.exe tem muitos subcomandos para IPv6. Uma lista completa de opções para a interface netsh IPv6 está disponível no prompt de comando do Windows XP com SP1 e posterior, digitando o seguinte:

**interface netsh IPv6/?**

A documentação sobre todos os comandos **netsh** para IPv6 também está disponível online no TechNet. Para obter mais informações sobre o **netsh** no Windows Server 2008, consulte [comandos netsh para interface (IPv4 e IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)). Para obter mais informações sobre o **netsh** no Windows Server 2003, consulte [comandos netsh para interface IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).

Estes são alguns comandos usados com frequência para IPv6, embora haja suporte para muitos outros comandos:

<dl> <dt>

<span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**Adicionar endereço IPv6 da interface netsh**
</dt> <dd>

Adiciona um endereço IPv6 a uma interface específica no computador local. Este comando tem parâmetros de subopção que devem ser especificados.

</dd> <dt>

<span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface ipv6 add DNS**
</dt> <dd>

Adiciona um endereço IPv6 do servidor DNS à lista configurada estaticamente de servidores DNS para a interface especificada no computador local. Este comando tem parâmetros de subopção que devem ser especificados.

</dd> <dt>

<span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface IPv6 adicionar rota**
</dt> <dd>

Adiciona uma rota para um endereço de prefixo IPv6 especificado no computador local. Este comando tem parâmetros de subopção que devem ser especificados.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**excluir endereço IPv6 da interface netsh**
</dt> <dd>

Exclui o endereço IPv6 especificado de uma interface específica no computador local. Este comando tem parâmetros de subopção que devem ser especificados.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface IPv6 Delete DNS**
</dt> <dd>

Exclui um endereço do servidor DNS da lista de servidores DNS configurada estaticamente para a interface especificada no computador local. Este comando tem parâmetros de subopção que devem ser especificados.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**interface netsh interface IPv6 Delete**
</dt> <dd>

Exclui uma interface especificada da pilha IPv6 no computador local. Este comando tem parâmetros de subopção que devem ser especificados.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface IPv6 excluir rota**
</dt> <dd>

Exclui uma rota para um endereço de prefixo IPv6 especificado no computador local. Este comando tem parâmetros de subopção que devem ser especificados.

</dd> <dt>

<span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**despejo de IPv6 da interface netsh**
</dt> <dd>

Cria um script que contém os comandos para criar a configuração atual. Se for salvo em um arquivo, esse script poderá ser usado para restaurar as definições de configuração alteradas.

</dd> <dt>

<span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**instalação do IPv6 da interface netsh**
</dt> <dd>

Instala o protocolo IPv6 no computador local.

</dd> <dt>

<span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**renovar IPv6 da interface netsh**
</dt> <dd>

Reinicia as interfaces IPv6 no computador local.

</dd> <dt>

<span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**redefinição de IPv6 da interface netsh**
</dt> <dd>

Redefine o estado de configuração do IPv6 no computador local.

</dd> <dt>

<span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**
</dt> <dd>

Exibe os parâmetros de configuração global para IPv6 no computador local.

</dd> <dt>

<span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface IPv6 Mostrar endereço**
</dt> <dd>

Exibe todos os endereços IPv6 ou todos os endereços IPv6 em uma interface específica no computador local. Esse comando tem parâmetros de subopção que talvez precisem ser especificados.

</dd> <dt>

<span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**desinstalação do IPv6 da interface netsh**
</dt> <dd>

Desinstala o protocolo IPv6 no computador local.

</dd> </dl>

## <a name="netsh-commands-for-ipv4"></a>Comandos netsh para IPv4

Comandos netsh semelhantes estão disponíveis para IPv4. Uma lista completa de opções para comandos netsh para uso com IPv4 está disponível no prompt de comando do Windows XP com SP1 e posterior, digitando o seguinte:

**netsh interface IP/?**

A documentação sobre todos os comandos netsh para IPv4 também está disponível online no TechNet. Para obter mais informações, consulte [comandos netsh para IP de interface](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))

 

 
