---
description: O material a seguir fornece diretrizes sobre como usar a TAPI para escrever aplicativos de usuário final ou de comunicação de servidor. Essas informações também são altamente relevantes para os programadores de provedores de serviços.
ms.assetid: fb97aff7-910e-451f-b183-36324a459423
title: Aplicativos TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6836f33af120171016b080693ae7a8315f9b9d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757198"
---
# <a name="tapi-applications"></a><span data-ttu-id="0ee6d-104">Aplicativos TAPI</span><span class="sxs-lookup"><span data-stu-id="0ee6d-104">TAPI Applications</span></span>

<span data-ttu-id="0ee6d-105">O material a seguir fornece diretrizes sobre como usar a TAPI para escrever aplicativos de usuário final ou de comunicação de servidor.</span><span class="sxs-lookup"><span data-stu-id="0ee6d-105">The following material provides guidelines on using TAPI to write end-user or server communications applications.</span></span> <span data-ttu-id="0ee6d-106">Essas informações também são altamente relevantes para os programadores de provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="0ee6d-106">This information is also highly relevant to service provider programmers.</span></span>

<span data-ttu-id="0ee6d-107">A primeira decisão que um programador precisa fazer no uso da TAPI é o nível de serviço necessário.</span><span class="sxs-lookup"><span data-stu-id="0ee6d-107">The first decision a programmer needs to make in using TAPI is the level of service required.</span></span> <span data-ttu-id="0ee6d-108">Por exemplo, se um aplicativo exigir uma seleção de menu que possa discar um número de telefone, um aplicativo TAPI completo provavelmente não será necessário.</span><span class="sxs-lookup"><span data-stu-id="0ee6d-108">For example, if an application requires a menu selection that can dial a phone number, a full TAPI application is probably not required.</span></span> <span data-ttu-id="0ee6d-109">A telefonia assistida pode habilitar essa opção de forma rápida e simples.</span><span class="sxs-lookup"><span data-stu-id="0ee6d-109">Assisted Telephony can enable this option quickly and simply.</span></span> <span data-ttu-id="0ee6d-110">Consulte [os níveis de serviço TAPI](tapi-levels-of-service.md) para obter mais informações sobre a distinção entre aplicativos TAPI completos e telefonia assistida.</span><span class="sxs-lookup"><span data-stu-id="0ee6d-110">Please see [TAPI Levels of Service](tapi-levels-of-service.md) for more information on the distinction between full TAPI applications and Assisted Telephony.</span></span>

<span data-ttu-id="0ee6d-111">A segunda decisão importante é se usar a TAPI 2. x, a API baseada em C ou a TAPI 3. x, que se baseia em COM.</span><span class="sxs-lookup"><span data-stu-id="0ee6d-111">The second important decision is whether to use TAPI 2.x, the C-based API, or TAPI 3.x, which is based on COM.</span></span> <span data-ttu-id="0ee6d-112">Consulte [TAPI 3. x vs. TAPI 2. x](tapi-3-x-versus-tapi-2-x.md) para obter uma discussão sobre considerações importantes para decidir qual delas usar.</span><span class="sxs-lookup"><span data-stu-id="0ee6d-112">Please see [TAPI 3.x vs. TAPI 2.x](tapi-3-x-versus-tapi-2-x.md) for a discussion of important considerations in deciding which one to use.</span></span>

<span data-ttu-id="0ee6d-113">O diagrama a seguir ilustra os blocos de construção básicos de um aplicativo TAPI completo.</span><span class="sxs-lookup"><span data-stu-id="0ee6d-113">The following diagram illustrates the basic building blocks of a full TAPI application.</span></span> <span data-ttu-id="0ee6d-114">A TAPI 2. x e a TAPI 3. x são abordadas nessas seções.</span><span class="sxs-lookup"><span data-stu-id="0ee6d-114">TAPI 2.x and TAPI 3.x are both addressed in these sections.</span></span> <span data-ttu-id="0ee6d-115">Material que é altamente específico de um é abordado nas seções de visão geral para TAPI 2. x ou TAPI 3. x.</span><span class="sxs-lookup"><span data-stu-id="0ee6d-115">Material that is highly specific to one is addressed in the overview sections for TAPI 2.x or TAPI 3.x.</span></span>

![blocos de construção de um aplicativo TAPI](images/tapior3.png)

<span data-ttu-id="0ee6d-117">Os links a seguir fornecem conteúdo que corresponde às figuras na imagem acima:</span><span class="sxs-lookup"><span data-stu-id="0ee6d-117">The following links provide content that corresponds to the figures in the above image:</span></span>

| <span data-ttu-id="0ee6d-118">Figuras</span><span class="sxs-lookup"><span data-stu-id="0ee6d-118">Figure</span></span> | <span data-ttu-id="0ee6d-119">Documentação</span><span class="sxs-lookup"><span data-stu-id="0ee6d-119">Documentation</span></span>                                                                    |
|--------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0ee6d-120">1</span><span class="sxs-lookup"><span data-stu-id="0ee6d-120">1</span></span>      | [<span data-ttu-id="0ee6d-121">Inicialização TAPI</span><span class="sxs-lookup"><span data-stu-id="0ee6d-121">TAPI Initialization</span></span>](tapi-initialization.md)                                   |
| <span data-ttu-id="0ee6d-122">2</span><span class="sxs-lookup"><span data-stu-id="0ee6d-122">2</span></span>      | [<span data-ttu-id="0ee6d-123">Controle de sessão</span><span class="sxs-lookup"><span data-stu-id="0ee6d-123">Session Control</span></span>](session-control.md)                                           |
| <span data-ttu-id="0ee6d-124">3</span><span class="sxs-lookup"><span data-stu-id="0ee6d-124">3</span></span>      | [<span data-ttu-id="0ee6d-125">Controle de dispositivo</span><span class="sxs-lookup"><span data-stu-id="0ee6d-125">Device Control</span></span>](device-control.md)                                             |
| <span data-ttu-id="0ee6d-126">4</span><span class="sxs-lookup"><span data-stu-id="0ee6d-126">4</span></span>      | [<span data-ttu-id="0ee6d-127">Controle de mídia</span><span class="sxs-lookup"><span data-stu-id="0ee6d-127">Media Control</span></span>](media-control.md)                                               |
| <span data-ttu-id="0ee6d-128">5</span><span class="sxs-lookup"><span data-stu-id="0ee6d-128">5</span></span>      | [<span data-ttu-id="0ee6d-129">Sobre controles do Call Center</span><span class="sxs-lookup"><span data-stu-id="0ee6d-129">About Call Center Controls</span></span>](about-call-center-controls.md)                     |
| <span data-ttu-id="0ee6d-130">6</span><span class="sxs-lookup"><span data-stu-id="0ee6d-130">6</span></span>      | [<span data-ttu-id="0ee6d-131">Conferência de telefonia IP de reunião</span><span class="sxs-lookup"><span data-stu-id="0ee6d-131">Rendezvous IP Telephony Conferencing</span></span>](rendezvous-ip-telephony-conferencing.md) |
| <span data-ttu-id="0ee6d-132">7</span><span class="sxs-lookup"><span data-stu-id="0ee6d-132">7</span></span>      | [<span data-ttu-id="0ee6d-133">Desligamento TAPI</span><span class="sxs-lookup"><span data-stu-id="0ee6d-133">TAPI Shutdown</span></span>](tapi-shutdown.md)                                               |



 

 

 



