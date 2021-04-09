---
title: Sistema de nomes de domínio
description: O DNS (sistema de nomes de domínio), um serviço localizador no Microsoft Windows, é um protocolo padrão do setor que localiza computadores em uma rede baseada em IP.
ms.assetid: 4d1c2151-3995-4e7f-881b-4466bd7b7bb7
keywords:
- DNS
- DNS, (consulte sistema de nome de domínio)
- Sistema de nomes de domínio
- Sistema de nomes de domínio, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d705c15fccb0ab237bc610ae4129f6d7002c4a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104012066"
---
# <a name="domain-name-system"></a><span data-ttu-id="e4fe3-107">Sistema de nomes de domínio</span><span class="sxs-lookup"><span data-stu-id="e4fe3-107">Domain Name System</span></span>

## <a name="purpose"></a><span data-ttu-id="e4fe3-108">Finalidade</span><span class="sxs-lookup"><span data-stu-id="e4fe3-108">Purpose</span></span>

<span data-ttu-id="e4fe3-109">O DNS (sistema de nomes de domínio), um serviço localizador no Microsoft Windows, é um protocolo padrão do setor que localiza computadores em uma rede baseada em IP.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-109">Domain Name System (DNS), a locator service in Microsoft Windows, is an industry-standard protocol that locates computers on an IP-based network.</span></span> <span data-ttu-id="e4fe3-110">Redes IP, como as redes Internet e Windows, dependem de endereços baseados em número para processar dados.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-110">IP networks, such as the Internet and Windows networks, rely on number-based addresses to process data.</span></span> <span data-ttu-id="e4fe3-111">No entanto, os usuários podem lembrar endereços de nomes com mais facilidade, portanto, é necessário converter nomes amigáveis (como `www.microsoft.com` ) em endereços que a rede possa reconhecer (como 207.46.131.137).</span><span class="sxs-lookup"><span data-stu-id="e4fe3-111">Users however, can more easily remember name addresses, so it is necessary to translate user-friendly names (such as `www.microsoft.com`) into addresses that the network can recognize (such as 207.46.131.137).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="e4fe3-112">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="e4fe3-112">Where applicable</span></span>

<span data-ttu-id="e4fe3-113">O Windows e o Active Directory usam o DNS.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-113">Windows and Active Directory use DNS.</span></span> <span data-ttu-id="e4fe3-114">O DNS é o serviço localizador primário para a Internet e Active Directory e, portanto, o DNS é considerado um serviço base para Windows e Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-114">DNS is the primary locator service for the Internet and Active Directory, and therefore, DNS is considered a base service for Windows and Active Directory.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e4fe3-115">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="e4fe3-115">Developer audience</span></span>

<span data-ttu-id="e4fe3-116">O Windows fornece funções que permitem que os programadores de aplicativos usem o DNS, como consulta de DNS programática, comparação de registros e pesquisa de nomes.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-116">Windows provides functions that enable application programmers to use DNS, such as programmatic DNS query, record compare, and name lookup.</span></span>

<span data-ttu-id="e4fe3-117">Os componentes de DNS programáveis são projetados para uso por programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-117">Programmable DNS components are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="e4fe3-118">É necessário ter familiaridade com a rede e o DNS.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-118">Familiarity with networking and DNS is required.</span></span> <span data-ttu-id="e4fe3-119">Os programadores devem estar familiarizados com o pacote de protocolo IP, bem como as operações de DNS e o protocolo DNS.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-119">Programmers should be familiar with the IP-protocol suite, as well as the DNS protocol and DNS operations.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e4fe3-120">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="e4fe3-120">Run-time requirements</span></span>

<span data-ttu-id="e4fe3-121">O DNS é usado em todas as redes IP que exigem um serviço de localizador compatível com a Internet.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-121">DNS is used on all IP networks that require an Internet-compatible locator service.</span></span> <span data-ttu-id="e4fe3-122">No entanto, a API DNS requer o Windows 2000 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-122">However, the DNS API requires Windows 2000 or later.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e4fe3-123">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e4fe3-123">In this section</span></span>



| <span data-ttu-id="e4fe3-124">Tópico</span><span class="sxs-lookup"><span data-stu-id="e4fe3-124">Topic</span></span>                                                             | <span data-ttu-id="e4fe3-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4fe3-125">Description</span></span>                                                                          |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4fe3-126">Documentos de padrões de DNS</span><span class="sxs-lookup"><span data-stu-id="e4fe3-126">DNS Standards Documents</span></span>](dns-standards-documents.md)<br/> | <span data-ttu-id="e4fe3-127">Links para documentos de padrões de DNS públicos.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-127">Links to public DNS standards documents.</span></span><br/>                                  |
| [<span data-ttu-id="e4fe3-128">Sobre o DNS</span><span class="sxs-lookup"><span data-stu-id="e4fe3-128">About DNS</span></span>](about-dns.md)<br/>                             | <span data-ttu-id="e4fe3-129">Informações gerais sobre o DNS.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-129">General information about DNS.</span></span><br/>                                            |
| [<span data-ttu-id="e4fe3-130">Referência de DNS</span><span class="sxs-lookup"><span data-stu-id="e4fe3-130">DNS Reference</span></span>](dns-reference.md)<br/>                     | <span data-ttu-id="e4fe3-131">Documentação de referência para DNS.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-131">Reference documentation for DNS.</span></span><br/>                                          |
| [<span data-ttu-id="e4fe3-132">Provedor WMI de DNS</span><span class="sxs-lookup"><span data-stu-id="e4fe3-132">DNS WMI Provider</span></span>](dns-wmi-provider.md)<br/>               | <span data-ttu-id="e4fe3-133">Informações gerais e documentação de referência para o provedor WMI de DNS.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-133">General information and reference documentation for the DNS WMI provider.</span></span><br/> |
| [<span data-ttu-id="e4fe3-134">Glossário</span><span class="sxs-lookup"><span data-stu-id="e4fe3-134">Glossary</span></span>](glossary-gly.md)<br/>                           | <span data-ttu-id="e4fe3-135">Glossário de termos e definições de DNS.</span><span class="sxs-lookup"><span data-stu-id="e4fe3-135">Glossary of DNS terms and definitions.</span></span><br/>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="e4fe3-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e4fe3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4fe3-137">DHCP</span><span class="sxs-lookup"><span data-stu-id="e4fe3-137">DHCP</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[<span data-ttu-id="e4fe3-138">Auxiliar de protocolo de Internet</span><span class="sxs-lookup"><span data-stu-id="e4fe3-138">Internet Protocol Helper</span></span>](/windows/desktop/IpHlp/ip-helper-start-page)
</dt> <dt>

<span data-ttu-id="e4fe3-139">[Serviços de diretório](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="e4fe3-139">[Directory Services](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)</span></span>
</dt> </dl>

 

