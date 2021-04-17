---
description: A interface de programação de aplicativos de telefonia da Microsoft (TAPI) versão 3,1 é uma API baseada em Component Object Model (COM) que mescla a telefonia clássica e IP.
ms.assetid: 79c4d2c9-953e-4e68-98b7-6a0dd9a04e0b
title: Interface de programação de aplicativo de telefonia versão 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d302f6ffe67094d436caf94cc8cf109e1e3c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756986"
---
# <a name="telephony-application-programming-interface-version-31"></a><span data-ttu-id="0f5ce-103">Interface de programação de aplicativo de telefonia versão 3,1</span><span class="sxs-lookup"><span data-stu-id="0f5ce-103">Telephony Application Programming Interface Version 3.1</span></span>

## <a name="purpose"></a><span data-ttu-id="0f5ce-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="0f5ce-104">Purpose</span></span>

<span data-ttu-id="0f5ce-105">A interface de programação de aplicativos de telefonia da Microsoft (TAPI) versão 3,1 é uma API baseada em Component Object Model (COM) que mescla a telefonia clássica e IP.</span><span class="sxs-lookup"><span data-stu-id="0f5ce-105">The Microsoft Telephony Application Programming Interface (TAPI) version 3.1 is a Component Object Model (COM)-based API that merges classic and IP telephony.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="0f5ce-106">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="0f5ce-106">Where applicable</span></span>

<span data-ttu-id="0f5ce-107">Os aplicativos TAPI possíveis incluem:</span><span class="sxs-lookup"><span data-stu-id="0f5ce-107">Possible TAPI applications include:</span></span>

-   <span data-ttu-id="0f5ce-108">Conferência de IP de multimídia multicast com qualidade de serviço (QOS)</span><span class="sxs-lookup"><span data-stu-id="0f5ce-108">Multicast multimedia IP conferencing with quality of service (QOS)</span></span>
-   <span data-ttu-id="0f5ce-109">Chamadas de voz pela Internet usando o protocolo H. 323</span><span class="sxs-lookup"><span data-stu-id="0f5ce-109">Voice calls over the Internet using the H.323 protocol</span></span>
-   <span data-ttu-id="0f5ce-110">Aplicativos de Call Center capazes de rastrear vários agentes</span><span class="sxs-lookup"><span data-stu-id="0f5ce-110">Call center applications capable of tracking multiple agents</span></span>
-   <span data-ttu-id="0f5ce-111">Chamadas de voz básicas na rede telefônica pública comutada (PSTN)</span><span class="sxs-lookup"><span data-stu-id="0f5ce-111">Basic voice calls on the Public Switched Telephone Network (PSTN)</span></span>
-   <span data-ttu-id="0f5ce-112">Controle de PBX</span><span class="sxs-lookup"><span data-stu-id="0f5ce-112">PBX control</span></span>
-   <span data-ttu-id="0f5ce-113">Sistemas de reação a voz interativa (IVR)</span><span class="sxs-lookup"><span data-stu-id="0f5ce-113">Interactive voice response (IVR) systems</span></span>
-   <span data-ttu-id="0f5ce-114">Mensagem de voz</span><span class="sxs-lookup"><span data-stu-id="0f5ce-114">Voice mail</span></span>

## <a name="developer-audience"></a><span data-ttu-id="0f5ce-115">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="0f5ce-115">Developer audience</span></span>

<span data-ttu-id="0f5ce-116">Você pode gravar aplicativos habilitados para TAPI em várias linguagens, incluindo Java, Visual Basic e C/C++.</span><span class="sxs-lookup"><span data-stu-id="0f5ce-116">You can write TAPI-enabled applications in many languages, including Java, Visual Basic, and C/C++.</span></span> <span data-ttu-id="0f5ce-117">É necessário ter familiaridade com com.</span><span class="sxs-lookup"><span data-stu-id="0f5ce-117">Familiarity with COM is required.</span></span> <span data-ttu-id="0f5ce-118">A experiência de desenvolvimento com telecomunicações ou outros aplicativos de telefonia é útil, mas não é necessária.</span><span class="sxs-lookup"><span data-stu-id="0f5ce-118">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="0f5ce-119">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="0f5ce-119">Run-time requirements</span></span>

<span data-ttu-id="0f5ce-120">A TAPI versão 3,1 permite o desenvolvimento de aplicativos de comunicação para sistemas operacionais Windows Server 2003, Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="0f5ce-120">TAPI version 3.1 enables development of communications applications for Windows Server 2003 operating systems, Windows XP, and Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0f5ce-121">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0f5ce-121">In this section</span></span>



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="0f5ce-122">Tópico</span><span class="sxs-lookup"><span data-stu-id="0f5ce-122">Topic</span></span></th><th><span data-ttu-id="0f5ce-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f5ce-123">Description</span></span></th></tr></thead><tbody><tr class="odd"><td><span data-ttu-id="0f5ce-124"><a href="tapi-3-1-overview.md">Visão geral</a></span><span class="sxs-lookup"><span data-stu-id="0f5ce-124"><a href="tapi-3-1-overview.md">Overview</a></span></span><br/></td><td><span data-ttu-id="0f5ce-125">Informações gerais sobre arquitetura e componentes TAPI.</span><span class="sxs-lookup"><span data-stu-id="0f5ce-125">General information about TAPI architecture and components.</span></span><br/></td></tr><tr class="even"><td><span data-ttu-id="0f5ce-126">Referência</span><span class="sxs-lookup"><span data-stu-id="0f5ce-126">Reference</span></span><br/></td><td><span data-ttu-id="0f5ce-127">Documentação para:</span><span class="sxs-lookup"><span data-stu-id="0f5ce-127">Documentation for:</span></span><br/><ul><li><span data-ttu-id="0f5ce-128"><a href="call-and-media-controls-reference.md">Referência de controles de chamada e de mídia</a></span><span class="sxs-lookup"><span data-stu-id="0f5ce-128"><a href="call-and-media-controls-reference.md">Call and Media Controls Reference</a></span></span></li><li><span data-ttu-id="0f5ce-129"><a href="call-center-controls-reference.md">Referência de controles do Call Center</a></span><span class="sxs-lookup"><span data-stu-id="0f5ce-129"><a href="call-center-controls-reference.md">Call Center Controls Reference</a></span></span></li><li><span data-ttu-id="0f5ce-130"><a href="rendezvous-ip-telephony-conferencing-reference.md">Referência de reunião</a></span><span class="sxs-lookup"><span data-stu-id="0f5ce-130"><a href="rendezvous-ip-telephony-conferencing-reference.md">Rendezvous Reference</a></span></span></li></ul></td></tr></tbody></table>



 

## <a name="related-topics"></a><span data-ttu-id="0f5ce-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f5ce-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f5ce-132">Visão geral de telefonia da Microsoft</span><span class="sxs-lookup"><span data-stu-id="0f5ce-132">Microsoft Telephony Overview</span></span>](microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="0f5ce-133">TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="0f5ce-133">TAPI 2.2</span></span>](./tapi-2-2-start-page.md)
</dt> <dt>

[<span data-ttu-id="0f5ce-134">Provedores de serviços TAPI</span><span class="sxs-lookup"><span data-stu-id="0f5ce-134">TAPI Service Providers</span></span>](./tapi-service-providers.md)
</dt> </dl>

 

