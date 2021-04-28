---
description: Novos binários Low-Level
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Novos binários Low-Level
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b4640d31b115dc85ecde9f9423997468ddc8456
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088064"
---
# <a name="new-low-level-binaries"></a><span data-ttu-id="b56bd-103">Novos binários Low-Level</span><span class="sxs-lookup"><span data-stu-id="b56bd-103">New Low-Level Binaries</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="b56bd-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="b56bd-104">Affected Platforms</span></span>

<span data-ttu-id="b56bd-105">**Clientes** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="b56bd-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="b56bd-106">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b56bd-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="b56bd-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="b56bd-107">Feature Impact</span></span>

<span data-ttu-id="b56bd-108">**Severidade** -média</span><span class="sxs-lookup"><span data-stu-id="b56bd-108">**Severity** - Medium</span></span>  
<span data-ttu-id="b56bd-109">**Frequência** -alta</span><span class="sxs-lookup"><span data-stu-id="b56bd-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="b56bd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b56bd-110">Description</span></span>

<span data-ttu-id="b56bd-111">Para melhorar a eficiência da engenharia interna e melhorar a base para o trabalho futuro, nós realocamos algumas funcionalidades para novos binários de nível baixo.</span><span class="sxs-lookup"><span data-stu-id="b56bd-111">To improve internal engineering efficiencies and improve foundations for future work, we have relocated some functionality to new low-level binaries.</span></span> <span data-ttu-id="b56bd-112">Essa refatoração possibilitará que futuras instalações do Windows forneçam subconjuntos de funcionalidade para reduzir a área da superfície (requisitos de disco e memória, manutenção e superfície de ataque).</span><span class="sxs-lookup"><span data-stu-id="b56bd-112">This refactoring will make it possible for future installs of Windows to provide subsets of functionality to reduce surface area (disk and memory requirements, servicing, and attack surface).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="b56bd-113">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="b56bd-113">Manifestation of Impact</span></span>

<span data-ttu-id="b56bd-114">Como um exemplo de funcionalidade que mudamos para binários de nível baixo, kernelbase.dll Obtém a funcionalidade de kernel32.dll e advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="b56bd-114">As an example of functionality that we moved to low-level binaries, kernelbase.dll gets functionality from kernel32.dll and advapi32.dll.</span></span> <span data-ttu-id="b56bd-115">Isso significa que o binário existente agora encaminha as chamadas para o novo binário em vez de tratá-los diretamente; o encaminhamento pode ser estático (a tabela de exportação mostra o redirecionamento) ou tempo de execução (a dll tem uma rotina de stub que chama para o novo binário).</span><span class="sxs-lookup"><span data-stu-id="b56bd-115">This means that the existing binary now forwards calls down to the new binary rather than handling them directly; the forwarding can be static (the export table shows the redirection), or runtime (the dll has a stub routine that calls down to the new binary).</span></span> <span data-ttu-id="b56bd-116">Isso afetará aplicativos de nível inferior, como aplicativos de segurança e de backup que dependem de APIs e deslocamentos internos.</span><span class="sxs-lookup"><span data-stu-id="b56bd-116">This will impact low-level applications such as security and backup applications that are dependent upon internal APIs and offsets.</span></span>

## <a name="solution"></a><span data-ttu-id="b56bd-117">Solução</span><span class="sxs-lookup"><span data-stu-id="b56bd-117">Solution</span></span>

<span data-ttu-id="b56bd-118">O único impacto é o código que faz suposições ao tentar examinar a kernel32.dll ou a tabela de exportação de advapi32.dll na memória, como um aplicativo antivírus pode fazer isso.</span><span class="sxs-lookup"><span data-stu-id="b56bd-118">The only impact is to code that makes assumptions when attempting to look at the kernel32.dll or the advapi32.dll export table in memory, such as an anti-virus application might do.</span></span> <span data-ttu-id="b56bd-119">Use APIs publicadas e não os detalhes de sua implementação.</span><span class="sxs-lookup"><span data-stu-id="b56bd-119">Use published APIs and not the details of their implementation.</span></span> <span data-ttu-id="b56bd-120">Esse é apenas um exemplo de implementação em um detalhe da implementação de uma API.</span><span class="sxs-lookup"><span data-stu-id="b56bd-120">This is just one example of implementing around a detail of implementation for an API.</span></span>

 

 



