---
title: Modelo de execução
description: Modelo de execução
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, modelo de execução
- modelo de execução OpenGL
- OpenGL, modelo de cliente/servidor
- modelo de cliente/servidor OpenGL
- OpenGL, rede transparente
- framebuffers, modelo de execução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86012912f9bd963da0489b83cc4a5c1e7e1722ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916533"
---
# <a name="execution-model"></a><span data-ttu-id="dc0b5-109">Modelo de execução</span><span class="sxs-lookup"><span data-stu-id="dc0b5-109">Execution Model</span></span>

<span data-ttu-id="dc0b5-110">O modelo de interpretação de comandos OpenGL é cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="dc0b5-110">The model for interpretation of OpenGL commands is client/server.</span></span> <span data-ttu-id="dc0b5-111">O código do aplicativo (o cliente) emite comandos, que são interpretados e processados pelo OpenGL (o servidor).</span><span class="sxs-lookup"><span data-stu-id="dc0b5-111">Application code (the client) issues commands, which are interpreted and processed by OpenGL (the server).</span></span> <span data-ttu-id="dc0b5-112">O servidor pode ou não operar no mesmo computador que o cliente.</span><span class="sxs-lookup"><span data-stu-id="dc0b5-112">The server may or may not operate on the same computer as the client.</span></span> <span data-ttu-id="dc0b5-113">Nesse sentido, o OpenGL é transparente para a rede.</span><span class="sxs-lookup"><span data-stu-id="dc0b5-113">In this sense, OpenGL is network-transparent.</span></span> <span data-ttu-id="dc0b5-114">Um servidor pode manter vários contextos OpenGL, cada um dos quais é um estado de OpenGL encapsulado.</span><span class="sxs-lookup"><span data-stu-id="dc0b5-114">A server can maintain several OpenGL contexts, each of which is an encapsulated OpenGL state.</span></span> <span data-ttu-id="dc0b5-115">Um cliente pode se conectar a qualquer um desses contextos.</span><span class="sxs-lookup"><span data-stu-id="dc0b5-115">A client can connect to any one of these contexts.</span></span> <span data-ttu-id="dc0b5-116">O protocolo de rede necessário pode ser implementado aumentando um protocolo já existente (como o do sistema X Window) ou usando um protocolo independente.</span><span class="sxs-lookup"><span data-stu-id="dc0b5-116">The required network protocol can be implemented by augmenting an already existing protocol (such as that of the X Window System) or by using an independent protocol.</span></span> <span data-ttu-id="dc0b5-117">Nenhum comando OpenGL é fornecido para obter a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc0b5-117">No OpenGL commands are provided for obtaining user input.</span></span>

<span data-ttu-id="dc0b5-118">O sistema de janelas que aloca recursos framebuffer, por fim, controla os efeitos dos comandos OpenGL no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="dc0b5-118">The window system that allocates framebuffer resources ultimately controls the effects of OpenGL commands on the framebuffer.</span></span> <span data-ttu-id="dc0b5-119">O sistema de janelas:</span><span class="sxs-lookup"><span data-stu-id="dc0b5-119">The window system:</span></span>

-   <span data-ttu-id="dc0b5-120">Determina quais partes do framebuffer OpenGL podem acessar em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="dc0b5-120">Determines which portions of the framebuffer OpenGL may access at any given time.</span></span>
-   <span data-ttu-id="dc0b5-121">Comunica-se com OpenGL como essas partes são estruturadas.</span><span class="sxs-lookup"><span data-stu-id="dc0b5-121">Communicates to OpenGL how those portions are structured.</span></span>

<span data-ttu-id="dc0b5-122">Portanto, não há comandos OpenGL para configurar o framebuffer ou inicializar OpenGL.</span><span class="sxs-lookup"><span data-stu-id="dc0b5-122">Therefore, there are no OpenGL commands to configure the framebuffer or initialize OpenGL.</span></span> <span data-ttu-id="dc0b5-123">A configuração do buffer de quadro é feita fora do OpenGL em conjunto com o sistema de janelas; A inicialização do OpenGL ocorre quando o sistema de janelas aloca uma janela para a renderização OpenGL.</span><span class="sxs-lookup"><span data-stu-id="dc0b5-123">Frame buffer configuration is done outside of OpenGL in conjunction with the window system; OpenGL initialization takes place when the window system allocates a window for OpenGL rendering.</span></span>

 

 




