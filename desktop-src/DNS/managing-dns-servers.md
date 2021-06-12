---
title: Gerenciando servidores DNS
description: Saiba mais sobre como gerenciar servidores DNS. Um servidor DNS é um computador que conclui o processo de resolução de nomes no DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d797e05bc326b35e48173082d9b36a2b334fd9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010763"
---
# <a name="managing-dns-servers"></a><span data-ttu-id="01b14-104">Gerenciando servidores DNS</span><span class="sxs-lookup"><span data-stu-id="01b14-104">Managing DNS Servers</span></span>

<span data-ttu-id="01b14-105">Um servidor DNS é um computador que conclui o processo de resolução de nomes no DNS.</span><span class="sxs-lookup"><span data-stu-id="01b14-105">A DNS Server is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="01b14-106">Os servidores DNS contêm arquivos, chamados de *arquivos de zona*, que permitem que eles resolvam nomes para endereços IP (ou vice-versa).</span><span class="sxs-lookup"><span data-stu-id="01b14-106">DNS Servers contain files, called *zone files*, that enable them to resolve names to IP addresses (or vice versa).</span></span> <span data-ttu-id="01b14-107">Quando consultado, um servidor DNS responde de uma destas três maneiras:</span><span class="sxs-lookup"><span data-stu-id="01b14-107">When queried, a DNS Server responds in one of three ways:</span></span>

-   <span data-ttu-id="01b14-108">O servidor retorna a resolução de nome ou as informações de resolução de IP solicitadas.</span><span class="sxs-lookup"><span data-stu-id="01b14-108">The server returns the requested name-resolution or IP-resolution information.</span></span>
-   <span data-ttu-id="01b14-109">O servidor retorna um ponteiro para outro servidor DNS que pode atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="01b14-109">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="01b14-110">O servidor indica que ele não tem as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="01b14-110">The server indicates that it does not have the requested information.</span></span>

<span data-ttu-id="01b14-111">Os servidores DNS podem, durante o curso de preparação, retornar as informações de resolução solicitadas, consultar outros servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="01b14-111">DNS Servers might, during the course of preparing to return the requested resolution information, query other DNS Servers.</span></span> <span data-ttu-id="01b14-112">Mas, além disso, os servidores DNS não executam nenhuma operação diferente daquelas mencionadas na lista anterior.</span><span class="sxs-lookup"><span data-stu-id="01b14-112">But beyond that, DNS Servers do not perform any operations other than those mentioned in the previous list.</span></span>

<span data-ttu-id="01b14-113">Há três tipos principais de servidores DNS – servidores primários, servidores secundários e servidores de cache.</span><span class="sxs-lookup"><span data-stu-id="01b14-113">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span> <span data-ttu-id="01b14-114">Consulte [servidores DNS](dns-servers.md) para obter mais informações sobre esses servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="01b14-114">See [DNS Servers](dns-servers.md) for more information on these DNS Servers.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="01b14-115">Etapas de administração</span><span class="sxs-lookup"><span data-stu-id="01b14-115">Administration Steps</span></span>

<span data-ttu-id="01b14-116">O provedor WMI de DNS permite a administração de servidores DNS a partir do próprio servidor ou de hosts remotos.</span><span class="sxs-lookup"><span data-stu-id="01b14-116">The DNS WMI Provider enables the administration of DNS Servers from the server itself, or from remote hosts.</span></span> <span data-ttu-id="01b14-117">As etapas gerais necessárias para administrar um servidor DNS usando o provedor WMI de DNS são:</span><span class="sxs-lookup"><span data-stu-id="01b14-117">The general steps necessary to administer a DNS Server using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="01b14-118">Conectando-se ao provedor WMI de DNS</span><span class="sxs-lookup"><span data-stu-id="01b14-118">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="01b14-119">Obtendo uma instância de servidor</span><span class="sxs-lookup"><span data-stu-id="01b14-119">Getting a server instance</span></span>
-   <span data-ttu-id="01b14-120">Listando ou modificando uma propriedade de servidor ou usando um método</span><span class="sxs-lookup"><span data-stu-id="01b14-120">Listing or modifying a server property, or using a method</span></span>

<span data-ttu-id="01b14-121">Para ilustrar como implementar essas etapas de administração, são fornecidos exemplos.</span><span class="sxs-lookup"><span data-stu-id="01b14-121">To illustrate how to implement those administration steps, examples are provided.</span></span> <span data-ttu-id="01b14-122">As tarefas a seguir estão vinculadas a seus exemplos de script associados.</span><span class="sxs-lookup"><span data-stu-id="01b14-122">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="01b14-123">Interrompendo um servidor DNS</span><span class="sxs-lookup"><span data-stu-id="01b14-123">Stopping a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="01b14-124">Iniciando um servidor DNS</span><span class="sxs-lookup"><span data-stu-id="01b14-124">Starting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="01b14-125">Reiniciando um servidor DNS</span><span class="sxs-lookup"><span data-stu-id="01b14-125">Restarting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="01b14-126">Adicionando um endereço IP</span><span class="sxs-lookup"><span data-stu-id="01b14-126">Adding an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="01b14-127">Removendo um endereço IP</span><span class="sxs-lookup"><span data-stu-id="01b14-127">Removing an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="01b14-128">Listando propriedades do servidor DNS</span><span class="sxs-lookup"><span data-stu-id="01b14-128">Listing DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="01b14-129">Exibindo tipos de Propriedade do servidor DNS</span><span class="sxs-lookup"><span data-stu-id="01b14-129">Displaying DNS Server Property Types</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="01b14-130">Modificando Propriedades do servidor DNS</span><span class="sxs-lookup"><span data-stu-id="01b14-130">Modifying DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




