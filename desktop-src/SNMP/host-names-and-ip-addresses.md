---
title: Nomes de host e endereços IP
description: As redes TCP/IP exigem que os nomes de host sejam resolvidos para endereços IP antes que as informações de endereço possam ser usadas para criar uma conexão.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Endereços IP e nomes de host SNMP
- Nomes de host, resolvendo SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f711be9e1fda5dc936db6628cccc21093aa09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635595"
---
# <a name="host-names-and-ip-addresses"></a><span data-ttu-id="88d68-105">Nomes de host e endereços IP</span><span class="sxs-lookup"><span data-stu-id="88d68-105">Host Names and IP Addresses</span></span>

<span data-ttu-id="88d68-106">As redes TCP/IP exigem que os nomes de host sejam resolvidos para endereços IP antes que as informações de endereço possam ser usadas para criar uma conexão.</span><span class="sxs-lookup"><span data-stu-id="88d68-106">TCP/IP networks require host names to be resolved to IP addresses before the address information can be used to create a connection.</span></span> <span data-ttu-id="88d68-107">Os computadores em execução no sistema operacional Windows usam um arquivo de host que, para essa finalidade, mapeia nomes de host para endereços IP.</span><span class="sxs-lookup"><span data-stu-id="88d68-107">Computers running on the Windows operating system use a host file that, for this purpose, maps host names to IP addresses.</span></span>

<span data-ttu-id="88d68-108">O arquivo de host é um arquivo de texto que lista nomes de host explícitos e endereços IP.</span><span class="sxs-lookup"><span data-stu-id="88d68-108">The host file is a text file that lists explicit host names and IP addresses.</span></span> <span data-ttu-id="88d68-109">O arquivo de host é carregado automaticamente na memória na inicialização e consultado quando um nome de host requer resolução.</span><span class="sxs-lookup"><span data-stu-id="88d68-109">The host file is automatically loaded into memory on startup and consulted when a host name requires resolution.</span></span> <span data-ttu-id="88d68-110">Se o arquivo de host não contiver as informações de mapeamento necessárias para resolver um nome de host específico para seu endereço IP, uma consulta de resolução será feita em um servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="88d68-110">If the host file does not contain the mapping information that is required to resolve a specific host name to its IP address, a resolution query is made to a DNS server.</span></span>

<span data-ttu-id="88d68-111">O SNMP usa o WINS (Windows Internet Serviço de Nomenclatura) para resolução de nomes de host.</span><span class="sxs-lookup"><span data-stu-id="88d68-111">SNMP uses the Windows Internet Naming Service (WINS) for host name resolution.</span></span> <span data-ttu-id="88d68-112">O WINS torna possível mapear nomes NetBIOS ou nomes de computador para endereços IP em redes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="88d68-112">WINS makes it possible to map NetBIOS names, or machine names, to IP addresses on TCP/IP networks.</span></span> <span data-ttu-id="88d68-113">Se o computador não puder acessar um servidor WINS, o serviço SNMP usará o arquivo de host para resolver nomes de host para endereços IP.</span><span class="sxs-lookup"><span data-stu-id="88d68-113">If the computer cannot access a WINS server, the SNMP service uses the host file to resolve host names to IP addresses.</span></span>

<span data-ttu-id="88d68-114">O serviço SNMP dá suporte ao uso de nomes de host e endereços IP.</span><span class="sxs-lookup"><span data-stu-id="88d68-114">The SNMP service supports the use of both host names and IP addresses.</span></span> <span data-ttu-id="88d68-115">No entanto, quando você tem a opção de usar nomes de host ou endereços IP para identificar locais de rede, seus aplicativos de gerenciamento SNMP devem usar nomes de host.</span><span class="sxs-lookup"><span data-stu-id="88d68-115">However, when you have a choice between using host names or IP addresses to identify network locations, your SNMP management applications should use host names.</span></span> <span data-ttu-id="88d68-116">Se você usar nomes de host, adicione todos os mapeamentos de nome de host e endereço IP dos sistemas participantes ao arquivo de host.</span><span class="sxs-lookup"><span data-stu-id="88d68-116">If you use host names, add all host name and IP address mappings of the participating systems to the host file.</span></span>

 

 




