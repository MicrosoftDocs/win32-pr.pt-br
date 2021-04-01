---
title: Proteção de Acesso à Rede
description: 'Observação: a plataforma de proteção de acesso à rede não está disponível a partir da NAP (proteção de acesso à rede) do Windows 10 é um conjunto de componentes do sistema operacional que fornece uma plataforma para acesso protegido a redes privadas.'
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- Proteção de Acesso à Rede
- Proteção de acesso à rede, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b99348428a867be5bf846fd40b030b844460cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635669"
---
# <a name="network-access-protection"></a><span data-ttu-id="29e14-105">Proteção de Acesso à Rede</span><span class="sxs-lookup"><span data-stu-id="29e14-105">Network Access Protection</span></span>

## <a name="purpose"></a><span data-ttu-id="29e14-106">Finalidade</span><span class="sxs-lookup"><span data-stu-id="29e14-106">Purpose</span></span>

> [!Note]  
> <span data-ttu-id="29e14-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="29e14-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="29e14-108">A NAP (proteção de acesso à rede) é um conjunto de componentes do sistema operacional que fornece uma plataforma para acesso protegido a redes privadas.</span><span class="sxs-lookup"><span data-stu-id="29e14-108">Network Access Protection (NAP) is a set of operating system components that provide a platform for protected access to private networks.</span></span> <span data-ttu-id="29e14-109">A plataforma NAP fornece uma maneira integrada de avaliar o estado de integridade do sistema de um cliente de rede que está tentando se conectar ou se comunicar em uma rede e restringir o acesso do cliente de rede até que os requisitos da política de integridade sejam atendidos.</span><span class="sxs-lookup"><span data-stu-id="29e14-109">The NAP platform provides an integrated way of evaluating the system health state of a network client that is attempting to connect to or communicate on a network and restricting the access of the network client until health policy requirements have been met.</span></span>

<span data-ttu-id="29e14-110">A NAP é uma plataforma extensível que fornece uma infraestrutura e uma API definida para adicionar componentes que armazenam, relatam, validam e corrigem o estado de integridade do sistema de um computador.</span><span class="sxs-lookup"><span data-stu-id="29e14-110">NAP is an extensible platform that provides an infrastructure and an API set for adding components that store, report, validate, and correct a computer's system health state.</span></span> <span data-ttu-id="29e14-111">Por si só, a plataforma NAP não fornece componentes para acumular e avaliar os atributos do estado de integridade de um computador.</span><span class="sxs-lookup"><span data-stu-id="29e14-111">By itself, the NAP platform does not provide components to accumulate and evaluate attributes of a computer's health state.</span></span> <span data-ttu-id="29e14-112">Outros componentes, conhecidos como agentes de integridade do sistema (SHAs) e validadores da integridade do sistema (SHVs), fornecem validação de política de rede e conformidade de política de rede.</span><span class="sxs-lookup"><span data-stu-id="29e14-112">Other components, known as system health agents (SHAs) and system health validators (SHVs), provide network policy validation and network policy compliance.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="29e14-113">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="29e14-113">Where applicable</span></span>

<span data-ttu-id="29e14-114">A NAP foi projetada para ser extensível.</span><span class="sxs-lookup"><span data-stu-id="29e14-114">NAP is designed to be extensible.</span></span> <span data-ttu-id="29e14-115">Ele pode interoperar com qualquer software de fornecedor que forneça SHAs e SHVs ou que reconheça seu conjunto de API publicado.</span><span class="sxs-lookup"><span data-stu-id="29e14-115">It can interoperate with any vendor software that provides SHAs and SHVs or that recognizes its published API set.</span></span> <span data-ttu-id="29e14-116">A NAP ajuda a fornecer uma solução para os seguintes cenários comuns:</span><span class="sxs-lookup"><span data-stu-id="29e14-116">NAP helps provide a solution for the following common scenarios:</span></span>

-   <span data-ttu-id="29e14-117">Verifique a integridade e o status dos laptops móveis.</span><span class="sxs-lookup"><span data-stu-id="29e14-117">Check the health and status of roaming laptops.</span></span>
-   <span data-ttu-id="29e14-118">Garanta a integridade dos computadores desktop.</span><span class="sxs-lookup"><span data-stu-id="29e14-118">Ensure the health of desktop computers.</span></span>
-   <span data-ttu-id="29e14-119">Verifique a conformidade e a integridade dos computadores em escritórios remotos.</span><span class="sxs-lookup"><span data-stu-id="29e14-119">Verify the compliance and health of computers in remote offices.</span></span>
-   <span data-ttu-id="29e14-120">Determine a integridade dos laptops visitantes.</span><span class="sxs-lookup"><span data-stu-id="29e14-120">Determine the health of visiting laptops.</span></span>
-   <span data-ttu-id="29e14-121">Verifique a conformidade e a integridade de computadores domésticos não gerenciados.</span><span class="sxs-lookup"><span data-stu-id="29e14-121">Verify the compliance and health of unmanaged home computers.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="29e14-122">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="29e14-122">Developer audience</span></span>

<span data-ttu-id="29e14-123">A API de NAP foi projetada para desenvolvedores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="29e14-123">The NAP API is designed for C/C++ developers.</span></span> <span data-ttu-id="29e14-124">Para os métodos de imposição de NAP, os programadores devem estar familiarizados com os protocolos de rede e as tecnologias, como o serviço de usuário dial-in de autenticação remota (RADIUS), protocolo DHCP, redes virtuais privadas (VPNs), o padrão IEEE 802.1 X para acesso com e sem fio e IPsec (Internet Protocol Security).</span><span class="sxs-lookup"><span data-stu-id="29e14-124">For the NAP enforcement methods, programmers should be familiar with networking protocols and technologies such as Remote Authentication Dial-in User Service (RADIUS), Dynamic Host Configuration Protocol (DHCP), virtual private networks (VPNs), the IEEE 802.1X standard for wired and wireless access, and Internet Protocol security (IPsec).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="29e14-125">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="29e14-125">Run-time requirements</span></span>

<span data-ttu-id="29e14-126">A plataforma NAP requer servidores de infraestrutura NAP que executam o Windows Server 2008 ou posterior e clientes NAP que executam o Windows XP com Service Pack 3 (SP3), Windows Vista ou sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="29e14-126">The NAP platform requires NAP infrastructure servers running Windows Server 2008 or later and NAP clients running Windows XP with Service Pack 3 (SP3), Windows Vista, or later operating systems.</span></span> <span data-ttu-id="29e14-127">Para obter informações específicas sobre quais sistemas operacionais dão suporte a um determinado elemento de programação, consulte as seções de requisitos das APIs de NAP na documentação de referência de NAP.</span><span class="sxs-lookup"><span data-stu-id="29e14-127">For specific information about which operating systems support a particular programming element, refer to the Requirements sections of the NAP APIs in the NAP Reference documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="29e14-128">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="29e14-128">In this section</span></span>



| <span data-ttu-id="29e14-129">Tópico</span><span class="sxs-lookup"><span data-stu-id="29e14-129">Topic</span></span>                                         | <span data-ttu-id="29e14-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="29e14-130">Description</span></span>                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="29e14-131">Sobre a NAP</span><span class="sxs-lookup"><span data-stu-id="29e14-131">About NAP</span></span>](about-nap.md)<br/>         | <span data-ttu-id="29e14-132">Informações gerais sobre a API NAP.</span><span class="sxs-lookup"><span data-stu-id="29e14-132">General information about NAP API.</span></span><br/>                                     |
| [<span data-ttu-id="29e14-133">Usando NAP</span><span class="sxs-lookup"><span data-stu-id="29e14-133">Using NAP</span></span>](using-nap.md)<br/>         | <span data-ttu-id="29e14-134">Exemplos de uso para a API NAP.</span><span class="sxs-lookup"><span data-stu-id="29e14-134">Usage examples for NAP API.</span></span><br/>                                            |
| [<span data-ttu-id="29e14-135">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="29e14-135">NAP Reference</span></span>](nap-reference.md)<br/> | <span data-ttu-id="29e14-136">Documentação para interfaces NAP, estruturas e outros elementos de código.</span><span class="sxs-lookup"><span data-stu-id="29e14-136">Documentation for NAP interfaces, structures, and other code elements.</span></span><br/> |



 

 

 





