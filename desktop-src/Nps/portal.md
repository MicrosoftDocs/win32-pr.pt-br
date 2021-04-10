---
title: Servidor de Políticas de Rede
description: O NPS (servidor de diretivas de rede) é a implementação da Microsoft de um servidor RADIUS e proxy de autenticação remota.
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d1dfc680c8a23ca1e80f52230736b3ab586cc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294162"
---
# <a name="network-policy-server"></a><span data-ttu-id="a0a3f-103">Servidor de Políticas de Rede</span><span class="sxs-lookup"><span data-stu-id="a0a3f-103">Network Policy Server</span></span>

## <a name="purpose"></a><span data-ttu-id="a0a3f-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="a0a3f-104">Purpose</span></span>

<span data-ttu-id="a0a3f-105">O NPS (servidor de diretivas de rede) é a implementação da Microsoft de um servidor RADIUS e proxy de autenticação remota.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-105">Network Policy Server (NPS) is the Microsoft implementation of a Remote Authentication Dial-in User Service (RADIUS) server and proxy.</span></span> <span data-ttu-id="a0a3f-106">É o sucessor do IAS (serviço de autenticação da Internet).</span><span class="sxs-lookup"><span data-stu-id="a0a3f-106">It is the successor of Internet Authentication Service (IAS).</span></span>

<span data-ttu-id="a0a3f-107">Como um servidor RADIUS, o NPS executa autenticação, autorização e contabilidade para conexões sem fio, de comutador de autenticação e de VPN (rede virtual privada) e dial-up de acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-107">As a RADIUS server, NPS performs authentication, authorization, and accounting for wireless, authenticating switch, and remote access dial-up and virtual private network (VPN) connections.</span></span>

<span data-ttu-id="a0a3f-108">O NPS também é um servidor avaliador de integridade para NAP (proteção de acesso à rede).</span><span class="sxs-lookup"><span data-stu-id="a0a3f-108">NPS is also a health evaluator server for Network Access Protection (NAP).</span></span> <span data-ttu-id="a0a3f-109">O NPS executa a autenticação e a autorização de tentativas de conexão de rede e, com base nas políticas de integridade do sistema configuradas, avalia a conformidade da integridade do computador e determina como limitar o acesso à rede ou a comunicação de um computador não compatível.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-109">NPS performs authentication and authorization of network connection attempts and, based on configured system health policies, evaluates computer health compliance and determines how to limit a noncompliant computer's network access or communication.</span></span> <span data-ttu-id="a0a3f-110">Este é um novo recurso específico somente ao NPS; O IAS não oferece suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-110">This is a new feature specific to NPS only; IAS does not support it.</span></span> <span data-ttu-id="a0a3f-111">Consulte [serviço de autenticação da Internet e servidor de políticas de rede](internet-authentication-service-vs-network-policy-server.md) para obter uma lista completa dos recursos novos para o NPS.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-111">See [Internet Authentication Service and Network Policy Server](internet-authentication-service-vs-network-policy-server.md) for a complete list of features new to NPS.</span></span>

<span data-ttu-id="a0a3f-112">O NPS inclui dois conjuntos de API: API de extensões do NPS e API de SDO (objetos de dados do servidor).</span><span class="sxs-lookup"><span data-stu-id="a0a3f-112">NPS includes two API sets: NPS Extensions API and Server Data Objects (SDO) API.</span></span> <span data-ttu-id="a0a3f-113">Tanto a API de extensões NPS quanto a API de SDO também são compatíveis com o precurso do NPS, o serviço de autenticação da Internet.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-113">Both NPS Extensions API and SDO API are also supported by the precursor of NPS, the Internet Authentication Service.</span></span>

<span data-ttu-id="a0a3f-114">A API de extensões do NPS pode ser usada para estender os métodos de autenticação, autorização e contabilidade oferecidos pelo NPS e anteriormente pelo IAS.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-114">NPS Extensions API can be used to extend the authentication, authorization, and accounting methods offered by NPS and previously by IAS.</span></span>

<span data-ttu-id="a0a3f-115">A API de objetos de dados do servidor pode ser usada para manipular a configuração da diretiva de rede em um computador que executa o NPS ou o IAS.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-115">Server Data Objects API can be used to manipulate the network policy configuration on a computer that runs NPS or IAS.</span></span>

> [!Note]  
> <span data-ttu-id="a0a3f-116">As políticas de rede no NPS são equivalentes às políticas de acesso remoto no IAS.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-116">Network policies in NPS are equivalent to remote access policies in IAS.</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="a0a3f-117">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="a0a3f-117">Developer audience</span></span>

<span data-ttu-id="a0a3f-118">A API de extensões do NPS foi projetada para uso por programadores que usam o software de desenvolvimento C/C++.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-118">The NPS Extensions API is designed for use by programmers using C/C++ development software.</span></span> <span data-ttu-id="a0a3f-119">Os programadores devem estar familiarizados com os conceitos de rede e o protocolo RADIUS.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-119">Programmers should be familiar with networking concepts and the RADIUS protocol.</span></span> <span data-ttu-id="a0a3f-120">O RADIUS está documentado em [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) e [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="a0a3f-120">RADIUS is documented in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) and [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

<span data-ttu-id="a0a3f-121">A API de objetos de dados do servidor foi projetada para uso por programadores usando o software de desenvolvimento C/C++ ou Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-121">The Server Data Objects API is designed for use by programmers using C/C++ or Visual Basic development software.</span></span> <span data-ttu-id="a0a3f-122">Os programadores devem estar familiarizados com o RAS ( [serviço de acesso remoto](/windows/desktop/RRAS/remote-access-request-for-comments) ) e o protocolo RADIUS.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-122">Programmers should be familiar with [Remote Access Service](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) and the RADIUS protocol.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a0a3f-123">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="a0a3f-123">Run-time requirements</span></span>

<span data-ttu-id="a0a3f-124">A API de extensões do NPS tem suporte no Windows Server 2008 com a instalação do serviço de Internet comercial da Microsoft (MCIS).</span><span class="sxs-lookup"><span data-stu-id="a0a3f-124">NPS Extensions API is supported on Windows Server 2008 with the installation of the Microsoft Commercial Internet Service (MCIS).</span></span>

<span data-ttu-id="a0a3f-125">A API de objetos de dados do servidor tem suporte no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-125">Server Data Objects API is supported on Windows Server 2008.</span></span>

<span data-ttu-id="a0a3f-126">O NPS está disponível no Windows Server 2008 com a instalação do serviço de Internet comercial da Microsoft (MCIS).</span><span class="sxs-lookup"><span data-stu-id="a0a3f-126">NPS is available on Windows Server 2008 with the installation of the Microsoft Commercial Internet Service (MCIS).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a0a3f-127">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a0a3f-127">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a0a3f-128">Visão geral</span><span class="sxs-lookup"><span data-stu-id="a0a3f-128">Overview</span></span>](about-network-policy-server.md)
</dt> <dd>

<span data-ttu-id="a0a3f-129">Informações gerais sobre RADIUS, IAS e NPS.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-129">General information regarding RADIUS, IAS, and NPS.</span></span>

</dd> <dt>

[<span data-ttu-id="a0a3f-130">API de extensões do servidor de políticas de rede</span><span class="sxs-lookup"><span data-stu-id="a0a3f-130">Network Policy Server Extensions API</span></span>](ias-extensions.md)
</dt> <dd>

<span data-ttu-id="a0a3f-131">API para implementar DLLs de extensão usadas para autenticação, autorização e contabilidade.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-131">API for implementing extension DLLs used for authentication, authorization, and accounting.</span></span>

</dd> <dt>

[<span data-ttu-id="a0a3f-132">API de objetos de dados do servidor</span><span class="sxs-lookup"><span data-stu-id="a0a3f-132">Server Data Objects API</span></span>](server-data-objects.md)
</dt> <dd>

<span data-ttu-id="a0a3f-133">API para gerenciar a configuração de política de rede.</span><span class="sxs-lookup"><span data-stu-id="a0a3f-133">API for managing the network policy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="a0a3f-134">Programação do SQL</span><span class="sxs-lookup"><span data-stu-id="a0a3f-134">SQL Programmability</span></span>](sql-programmability.md)
</dt> <dd>

<span data-ttu-id="a0a3f-135">Exemplos de procedimentos armazenados usados para gerenciar o registro em log do NPS (IAS).</span><span class="sxs-lookup"><span data-stu-id="a0a3f-135">Samples of stored procedures used for managing NPS (IAS) logging.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="a0a3f-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0a3f-136">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a0a3f-137">[TechNet: servidor de políticas de rede](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="a0a3f-137">[TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="a0a3f-138">[TechNet: serviço de autenticação da Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="a0a3f-138">[TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="a0a3f-139">Proteção de acesso à rede</span><span class="sxs-lookup"><span data-stu-id="a0a3f-139">Network Access Protection</span></span>](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 