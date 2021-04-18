---
title: Plug-ins de interface do usuário do Windows Media Player
description: Plug-ins de interface do usuário do Windows Media Player
ms.assetid: 71f53abe-310f-429a-bb23-5291bebdc432
keywords:
- Windows Media Player, plug-ins
- Windows Media Player, plug-ins de interface do usuário
- Plug-ins do Windows Media Player, interface do usuário
- plug-ins, interface do usuário
- plug-ins de interface do usuário, sobre
- Plug-ins de interface do usuário, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24050f24ef4412d3de9efd5faac6c2af90451dc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105760571"
---
# <a name="windows-media-player-user-interface-plug-ins"></a><span data-ttu-id="5f6d7-109">Plug-ins de interface do usuário do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="5f6d7-109">Windows Media Player User Interface Plug-ins</span></span>

<span data-ttu-id="5f6d7-110">O Microsoft Windows Media Player fornece uma arquitetura que permite ao usuário instalar e ativar os programas de plug-in que adicionam a funcionalidade de interface do usuário ao modo completo do Player.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-110">Microsoft Windows Media Player provides an architecture that enables the user to install and activate plug-in programs that add user interface (UI) functionality to the full mode of the player.</span></span> <span data-ttu-id="5f6d7-111">Um plug-in de interface do usuário típico pode permitir que um usuário compre o CD que contém a faixa que está sendo executada ou acesse informações adicionais sobre o artista.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-111">A typical UI plug-in might allow a user to buy the CD that contains the currently playing track or to access additional information about the artist.</span></span> <span data-ttu-id="5f6d7-112">Esta seção do SDK (Software Development Kit) do Windows Media Player fornece as informações de programação necessárias para criar seu próprio plug-in de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-112">This section of the Windows Media Player Software Development Kit (SDK) provides you with the programming information you need to create your own UI plug-in.</span></span>

<span data-ttu-id="5f6d7-113">A documentação de plug-in da interface do usuário é dividida em três seções:</span><span class="sxs-lookup"><span data-stu-id="5f6d7-113">The UI plug-in documentation is divided into three sections:</span></span>



| <span data-ttu-id="5f6d7-114">Seção</span><span class="sxs-lookup"><span data-stu-id="5f6d7-114">Section</span></span>                                                                                            | <span data-ttu-id="5f6d7-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f6d7-115">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f6d7-116">Sobre plug-ins de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="5f6d7-116">About User Interface Plug-ins</span></span>](about-user-interface-plug-ins.md)                                 | <span data-ttu-id="5f6d7-117">Fornece uma visão geral da arquitetura usada para plug-ins de interface do usuário. Leia esta seção para aprender os conceitos gerais envolvidos nessa tecnologia.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-117">Provides an overview of the architecture used for UI plug-ins. Read this section to learn the general concepts involved with this technology.</span></span> |
| [<span data-ttu-id="5f6d7-118">Guia de programação de plug-ins de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="5f6d7-118">User Interface Plug-ins Programming Guide</span></span>](user-interface-plug-ins-programming-guide.md)         | <span data-ttu-id="5f6d7-119">Explica o que você precisa fazer para criar um plug-in de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-119">Explains what you need to do to create a UI plug-in.</span></span> <span data-ttu-id="5f6d7-120">Esta seção contém código de exemplo e procedimentos passo a passo.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-120">This section contains example code and step-by-step procedures.</span></span>                          |
| [<span data-ttu-id="5f6d7-121">Referência de programação de plug-ins de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="5f6d7-121">User Interface Plug-ins Programming Reference</span></span>](user-interface-plug-ins-programming-reference.md) | <span data-ttu-id="5f6d7-122">Fornece uma referência detalhada para a interface COM e os métodos com suporte pelo SDK do Windows Media Player para plug-ins de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-122">Provides a detailed reference for the COM interface and methods supported by the Windows Media Player SDK for UI plug-ins.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="5f6d7-123">O Windows Media Player 10 Mobile fornece o mesmo modelo de plug-in que o Windows Media Player para desktop.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-123">Windows Media Player 10 Mobile provides the same plug-in model as the desktop Windows Media Player.</span></span> <span data-ttu-id="5f6d7-124">Esse modelo de plug-in permite que você use plug-ins em segundo plano para monitorar eventos, exibir o status das propriedades e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-124">This plug-in model enables you to use background plug-ins for monitoring events, displaying the status of properties, and so on.</span></span> <span data-ttu-id="5f6d7-125">O guia de programação nesta seção descreve como criar um plug-in de interface do usuário em segundo plano para o Windows Media Player 10 Mobile usando o assistente de plug-in do Windows Media Player para desktop.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-125">The programming guide in this section describes how to create a background UI plug-in for Windows Media Player 10 Mobile by using the desktop Windows Media Player Plug-in Wizard.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5f6d7-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f6d7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f6d7-127">**Plug-ins do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="5f6d7-127">**Windows Media Player Plug-ins**</span></span>](windows-media-player-plug-ins.md)
</dt> </dl>

 

 




