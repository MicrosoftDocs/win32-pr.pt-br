---
description: .
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: MSMQ (enfileiramento de mensagens da Microsoft)-remoção do serviço de suporte ao cliente do Windows 2000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54688ee4ad24eb691c95e4d70ce0acb881e212eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011546"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a><span data-ttu-id="a8efb-103">MSMQ (enfileiramento de mensagens da Microsoft)-remoção do serviço de suporte ao cliente do Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8efb-103">Microsoft Message Queuing (MSMQ) - Removal of Windows 2000 Client Support Service</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="a8efb-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="a8efb-104">Affected Platforms</span></span>

<span data-ttu-id="a8efb-105">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a8efb-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="a8efb-106">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="a8efb-106">Feature Impact</span></span>

 <span data-ttu-id="a8efb-107">**Severidade** -alta</span><span class="sxs-lookup"><span data-stu-id="a8efb-107">**Severity** - High</span></span>  
<span data-ttu-id="a8efb-108">**Frequência** -baixa</span><span class="sxs-lookup"><span data-stu-id="a8efb-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="a8efb-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8efb-109">Description</span></span>

<span data-ttu-id="a8efb-110">O serviço de suporte ao cliente do Windows 2000 é um componente opcional do servidor de enfileiramento de mensagens que você pode instalar em um computador do controlador de domínio Windows 2003 ou Windows 2008.</span><span class="sxs-lookup"><span data-stu-id="a8efb-110">The Windows 2000 Client Support Service is an optional component of the Message Queuing Server that you can install on a Windows 2003 or Windows 2008 domain controller machine.</span></span> <span data-ttu-id="a8efb-111">Esse serviço permite que os clientes do Windows 2000 operem em um modo integrado ao domínio com qualquer servidor de enfileiramento de mensagens instalado em computadores Windows 2003/2008.</span><span class="sxs-lookup"><span data-stu-id="a8efb-111">This service allows Windows 2000 clients to operate in a domain-integrated mode with any Message Queuing server installed on Windows 2003/2008 machines.</span></span> <span data-ttu-id="a8efb-112">Os clientes MSMQ que operam no Windows XP para cima não precisam desse serviço.</span><span class="sxs-lookup"><span data-stu-id="a8efb-112">MSMQ Clients operating on Windows XP upwards do not need this service.</span></span>

### <a name="manifestation-of-impact"></a><span data-ttu-id="a8efb-113">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="a8efb-113">Manifestation of Impact</span></span>

<span data-ttu-id="a8efb-114">Essa alteração afeta o Windows 2000 ao interoperar em um domínio do Windows 7 em que todos os controladores de domínio são Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a8efb-114">This change impacts Windows 2000 when interoperating in a Windows 7 domain where all domain controllers are Windows Server 2008 R2.</span></span> <span data-ttu-id="a8efb-115">Se um cliente atualizar para o domínio do Windows 7, os aplicativos MSMQ existentes em qualquer computador com Windows 2000 no domínio não poderão operar em um modo integrado ao domínio, a menos que esses clientes atualizem para uma versão superior do Windows.</span><span class="sxs-lookup"><span data-stu-id="a8efb-115">If a customer upgrades to the Windows 7 domain, the existing MSMQ applications on any Windows 2000 machines in the domain will not be able to operate in a domain-integrated mode unless these clients upgrade to a higher Windows version.</span></span>

### <a name="mitigation"></a><span data-ttu-id="a8efb-116">Atenuação</span><span class="sxs-lookup"><span data-stu-id="a8efb-116">Mitigation</span></span>

<span data-ttu-id="a8efb-117">Os usuários que têm computadores cliente com Windows 2000 em um domínio do Windows 7 podem configurar um controlador de domínio do Windows 2003/2008 no domínio e instalar o serviço de suporte ao cliente MSMQ Windows 2000 nesse controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="a8efb-117">Users who have Windows 2000 Client machines on a Windows 7 domain can configure a Windows 2003/2008 domain controller in the domain and install the MSMQ Windows 2000 Client Support Service on this domain controller.</span></span>

### <a name="leveraging-feature-capabilities"></a><span data-ttu-id="a8efb-118">Aproveitando os recursos do recurso</span><span class="sxs-lookup"><span data-stu-id="a8efb-118">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="a8efb-119">Os usuários que têm computadores cliente com Windows 2000 executando o MSMQ devem atualizar para uma versão superior do Windows para aproveitar a implementação baseada em Active Directory do servidor MSMQ.</span><span class="sxs-lookup"><span data-stu-id="a8efb-119">Users who have Windows 2000 Client machines running MSMQ should upgrade to a higher Windows version in order to take advantage of the Active Directory-based implementation of the MSMQ Server.</span></span>

### <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="a8efb-120">Compatibilidade, desempenho, confiabilidade e teste de usabilidade</span><span class="sxs-lookup"><span data-stu-id="a8efb-120">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="a8efb-121">Os usuários que têm computadores cliente com Windows 2000 executando o MSMQ em um domínio do Windows 7 com um ou mais controladores de domínio de nível inferior devem verificar se seus aplicativos estão funcionais nesse domínio misto.</span><span class="sxs-lookup"><span data-stu-id="a8efb-121">Users who have Windows 2000 Client machines running MSMQ on a Windows 7 domain with one or more down-level domain controllers should verify that their applications are functional on this mixed domain.</span></span>

 

 



