---
title: Gerenciando servidores DNS
description: Um servidor DNS é um computador que conclui o processo de resolução de nomes no DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe97e8b8b02e9d2198e49d0574b2d3fb8bc87df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636544"
---
# <a name="managing-dns-servers"></a><span data-ttu-id="9736f-103">Gerenciando servidores DNS</span><span class="sxs-lookup"><span data-stu-id="9736f-103">Managing DNS Servers</span></span>

<span data-ttu-id="9736f-104">Um servidor DNS é um computador que conclui o processo de resolução de nomes no DNS.</span><span class="sxs-lookup"><span data-stu-id="9736f-104">A DNS Server is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="9736f-105">Os servidores DNS contêm arquivos, chamados de *arquivos de zona*, que permitem que eles resolvam nomes para endereços IP (ou vice-versa).</span><span class="sxs-lookup"><span data-stu-id="9736f-105">DNS Servers contain files, called *zone files*, that enable them to resolve names to IP addresses (or vice versa).</span></span> <span data-ttu-id="9736f-106">Quando consultado, um servidor DNS responde de uma destas três maneiras:</span><span class="sxs-lookup"><span data-stu-id="9736f-106">When queried, a DNS Server responds in one of three ways:</span></span>

-   <span data-ttu-id="9736f-107">O servidor retorna a resolução de nome ou as informações de resolução de IP solicitadas.</span><span class="sxs-lookup"><span data-stu-id="9736f-107">The server returns the requested name-resolution or IP-resolution information.</span></span>
-   <span data-ttu-id="9736f-108">O servidor retorna um ponteiro para outro servidor DNS que pode atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="9736f-108">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="9736f-109">O servidor indica que ele não tem as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="9736f-109">The server indicates that it does not have the requested information.</span></span>

<span data-ttu-id="9736f-110">Os servidores DNS podem, durante o curso de preparação, retornar as informações de resolução solicitadas, consultar outros servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="9736f-110">DNS Servers might, during the course of preparing to return the requested resolution information, query other DNS Servers.</span></span> <span data-ttu-id="9736f-111">Mas, além disso, os servidores DNS não executam nenhuma operação diferente daquelas mencionadas na lista anterior.</span><span class="sxs-lookup"><span data-stu-id="9736f-111">But beyond that, DNS Servers do not perform any operations other than those mentioned in the previous list.</span></span>

<span data-ttu-id="9736f-112">Há três tipos principais de servidores DNS – servidores primários, servidores secundários e servidores de cache.</span><span class="sxs-lookup"><span data-stu-id="9736f-112">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span> <span data-ttu-id="9736f-113">Consulte [servidores DNS](dns-servers.md) para obter mais informações sobre esses servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="9736f-113">See [DNS Servers](dns-servers.md) for more information on these DNS Servers.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="9736f-114">Etapas de administração</span><span class="sxs-lookup"><span data-stu-id="9736f-114">Administration Steps</span></span>

<span data-ttu-id="9736f-115">O provedor WMI de DNS permite a administração de servidores DNS a partir do próprio servidor ou de hosts remotos.</span><span class="sxs-lookup"><span data-stu-id="9736f-115">The DNS WMI Provider enables the administration of DNS Servers from the server itself, or from remote hosts.</span></span> <span data-ttu-id="9736f-116">As etapas gerais necessárias para administrar um servidor DNS usando o provedor WMI de DNS são:</span><span class="sxs-lookup"><span data-stu-id="9736f-116">The general steps necessary to administer a DNS Server using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="9736f-117">Conectando-se ao provedor WMI de DNS</span><span class="sxs-lookup"><span data-stu-id="9736f-117">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="9736f-118">Obtendo uma instância de servidor</span><span class="sxs-lookup"><span data-stu-id="9736f-118">Getting a server instance</span></span>
-   <span data-ttu-id="9736f-119">Listando ou modificando uma propriedade de servidor ou usando um método</span><span class="sxs-lookup"><span data-stu-id="9736f-119">Listing or modifying a server property, or using a method</span></span>

<span data-ttu-id="9736f-120">Para ilustrar como implementar essas etapas de administração, são fornecidos exemplos.</span><span class="sxs-lookup"><span data-stu-id="9736f-120">To illustrate how to implement those administration steps, examples are provided.</span></span> <span data-ttu-id="9736f-121">As tarefas a seguir estão vinculadas a seus exemplos de script associados.</span><span class="sxs-lookup"><span data-stu-id="9736f-121">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="9736f-122">Interrompendo um servidor DNS</span><span class="sxs-lookup"><span data-stu-id="9736f-122">Stopping a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="9736f-123">Iniciando um servidor DNS</span><span class="sxs-lookup"><span data-stu-id="9736f-123">Starting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="9736f-124">Reiniciando um servidor DNS</span><span class="sxs-lookup"><span data-stu-id="9736f-124">Restarting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="9736f-125">Adicionando um endereço IP</span><span class="sxs-lookup"><span data-stu-id="9736f-125">Adding an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="9736f-126">Removendo um endereço IP</span><span class="sxs-lookup"><span data-stu-id="9736f-126">Removing an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="9736f-127">Listando propriedades do servidor DNS</span><span class="sxs-lookup"><span data-stu-id="9736f-127">Listing DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="9736f-128">Exibindo tipos de Propriedade do servidor DNS</span><span class="sxs-lookup"><span data-stu-id="9736f-128">Displaying DNS Server Property Types</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="9736f-129">Modificando Propriedades do servidor DNS</span><span class="sxs-lookup"><span data-stu-id="9736f-129">Modifying DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




