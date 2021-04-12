---
title: APIs estendidas do cliente DRM do Windows Media
description: APIs estendidas do cliente DRM do Windows Media
ms.assetid: c0397aa8-1f5a-48f5-a96b-555079e9a292
keywords:
- SDK do Windows Media Format, APIs estendidas do cliente DRM
- SDK do Windows Media Format, APIs estendidas do cliente
- SDK do Windows Media Format, APIs estendidas
- SDK do Windows Media Format, APIs
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), APIs
- APIs estendidas do cliente DRM, sobre
- APIs estendidas do cliente, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01c33ef3649f2cda63713ebd22a0116fdd025144
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366093"
---
# <a name="windows-media-drm-client-extended-apis"></a><span data-ttu-id="03fa2-116">APIs estendidas do cliente DRM do Windows Media</span><span class="sxs-lookup"><span data-stu-id="03fa2-116">Windows Media DRM Client Extended APIs</span></span>

<span data-ttu-id="03fa2-117">\[O recurso DRM do Windows Media foi preterido e não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="03fa2-117">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="03fa2-118">Em vez disso, use [o Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="03fa2-118">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="03fa2-119">Esta documentação descreve as APIs (interfaces de programação de aplicativo) do Microsoft Windows Media Digital Rights Management (DRM) cliente estendidas.</span><span class="sxs-lookup"><span data-stu-id="03fa2-119">This documentation describes the Microsoft Windows Media Digital Rights Management (DRM) Client Extended Application Programming Interfaces (APIs).</span></span> <span data-ttu-id="03fa2-120">As APIs estendidas do cliente DRM do Windows Media incluem objetos que podem ser usados para gerenciar as operações do Windows Media Digital Rights Management (DRM) em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="03fa2-120">The Windows Media DRM Client Extended APIs include objects that can be used to manage Windows Media Digital Rights Management (DRM) operations on a client computer.</span></span>

<span data-ttu-id="03fa2-121">O foco principal dessas APIs é o gerenciamento de licenças para conteúdo de mídia digital protegido.</span><span class="sxs-lookup"><span data-stu-id="03fa2-121">The primary focus of these APIs is the management of licenses for protected digital media content.</span></span> <span data-ttu-id="03fa2-122">Além disso, as APIs podem ser usadas para atualizar os componentes DRM no computador cliente e para criar aplicativos que transmitam conteúdo usando o Windows Media DRM para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="03fa2-122">In addition, the APIs can be used to update the DRM components on the client computer and to create applications that transmit content using Windows Media DRM for Network Devices.</span></span>

<span data-ttu-id="03fa2-123">Essas APIs constituem a contraparte do lado do cliente para o SDK do Windows Media Rights Manager.</span><span class="sxs-lookup"><span data-stu-id="03fa2-123">These APIs constitute the client-side counterpart to the Windows Media Rights Manager SDK.</span></span> <span data-ttu-id="03fa2-124">Onde o Windows Media Rights Manager é usado para criar serviços online que protegem arquivos e emitem licenças, as APIs estendidas do cliente DRM do Windows Media são usadas para criar aplicativos que consomem esse conteúdo.</span><span class="sxs-lookup"><span data-stu-id="03fa2-124">Where Windows Media Rights Manager is used to create online services that protect files and issue licenses, the Windows Media DRM Client Extended APIs are used to create applications that consume that content.</span></span>

<span data-ttu-id="03fa2-125">Este documento inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="03fa2-125">This document includes the following sections.</span></span>



| <span data-ttu-id="03fa2-126">Seção</span><span class="sxs-lookup"><span data-stu-id="03fa2-126">Section</span></span>                                                                                                  | <span data-ttu-id="03fa2-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="03fa2-127">Description</span></span>                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03fa2-128">Sobre as APIs estendidas do cliente DRM do Windows Media</span><span class="sxs-lookup"><span data-stu-id="03fa2-128">About the Windows Media DRM Client Extended APIs</span></span>](about-the-windows-media-drm-client-extended-apis.md) | <span data-ttu-id="03fa2-129">Fornece uma visão geral e informações básicas com as quais você deve estar familiarizado antes de desenvolver aplicativos que usam as APIs.</span><span class="sxs-lookup"><span data-stu-id="03fa2-129">Provides overview and background information that you should be familiar with before developing applications that use the APIs.</span></span>                                                        |
| [<span data-ttu-id="03fa2-130">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="03fa2-130">Programming Guide</span></span>](drm-programming-guide.md)                                                           | <span data-ttu-id="03fa2-131">Fornece instruções detalhadas para executar várias operações de DRM do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="03fa2-131">Provides detailed instructions for performing various client-side DRM operations.</span></span>                                                                                                      |
| [<span data-ttu-id="03fa2-132">Referência de programação</span><span class="sxs-lookup"><span data-stu-id="03fa2-132">Programming Reference</span></span>](drm-programming-reference.md)                                                   | <span data-ttu-id="03fa2-133">Fornece informações de referência sobre as interfaces, métodos, funções, estruturas, tipos de enumeração e constantes incluídas nas APIs estendidas do cliente DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="03fa2-133">Provides reference information about the interfaces, methods, functions, structures, enumeration types, and constants that are included in the Windows Media DRM Client Extended APIs.</span></span> |



 

 

 