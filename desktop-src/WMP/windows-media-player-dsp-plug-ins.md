---
title: Plug-ins de DSP do Windows Media Player
description: Plug-ins de DSP do Windows Media Player
ms.assetid: 1c7202c4-ca66-491d-9a5f-26032cad1dcc
keywords:
- Windows Media Player, plug-ins
- Windows Media Player, plug-ins do DSP
- Plug-ins do Windows Media Player, processamento de sinal digital (DSP)
- plug-ins, processamento de sinal digital (DSP)
- plug-ins de processamento de sinal digital, sobre
- Plug-ins do DSP, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755088bce89530350997d2f543e30872f630e882
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453647"
---
# <a name="windows-media-player-dsp-plug-ins"></a><span data-ttu-id="85b95-109">Plug-ins de DSP do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="85b95-109">Windows Media Player DSP Plug-ins</span></span>

<span data-ttu-id="85b95-110">O Microsoft Windows Media Player fornece uma arquitetura que permite ao usuário instalar e ativar programas de plug-in que adicionam funcionalidade de DSP (processamento de sinal digital).</span><span class="sxs-lookup"><span data-stu-id="85b95-110">Microsoft Windows Media Player provides an architecture that enables the user to install and activate plug-in programs that add digital signal processing (DSP) functionality.</span></span> <span data-ttu-id="85b95-111">Um plug-in do DSP é um Microsoft DirectX Media Object (DMO) ou uma Media Foundation Transform (MFT) que se conecta ao Player usando interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="85b95-111">A DSP plug-in is a Microsoft DirectX Media Object (DMO) or a Media Foundation Transform (MFT) that connects to the Player by using COM interfaces.</span></span> <span data-ttu-id="85b95-112">Um plug-in típico do DSP pode ser um equalizador de áudio ou um controle de tonalidade de vídeo.</span><span class="sxs-lookup"><span data-stu-id="85b95-112">A typical DSP plug-in might be an audio equalizer or a video tint control.</span></span> <span data-ttu-id="85b95-113">Esta seção do SDK fornece as informações de programação necessárias para criar seu próprio plug-in do DSP.</span><span class="sxs-lookup"><span data-stu-id="85b95-113">This section of the SDK provides the programming information you need to create your own DSP plug-in.</span></span>

<span data-ttu-id="85b95-114">A documentação de plug-in do DSP é dividida nas três seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="85b95-114">The DSP plug-in documentation is divided into the following three sections.</span></span>



| <span data-ttu-id="85b95-115">Seção</span><span class="sxs-lookup"><span data-stu-id="85b95-115">Section</span></span>                                                                      | <span data-ttu-id="85b95-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="85b95-116">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85b95-117">Sobre plug-ins do DSP</span><span class="sxs-lookup"><span data-stu-id="85b95-117">About DSP Plug-ins</span></span>](about-dsp-plug-ins.md)                                 | <span data-ttu-id="85b95-118">Fornece uma visão geral da arquitetura usada para plug-ins do DSP. Leia esta seção para aprender os conceitos gerais envolvidos nessa tecnologia.</span><span class="sxs-lookup"><span data-stu-id="85b95-118">Provides an overview of the architecture used for DSP plug-ins. Read this section to learn the general concepts involved with this technology.</span></span>  |
| [<span data-ttu-id="85b95-119">Guia de programação de plug-ins do DSP</span><span class="sxs-lookup"><span data-stu-id="85b95-119">DSP Plug-ins Programming Guide</span></span>](dsp-plug-ins-programming-guide.md)         | <span data-ttu-id="85b95-120">Explica o que você precisa fazer para criar um plug-in do DSP.</span><span class="sxs-lookup"><span data-stu-id="85b95-120">Explains what you need to do to create a DSP plug-in.</span></span> <span data-ttu-id="85b95-121">Esta seção contém código de exemplo e procedimentos passo a passo.</span><span class="sxs-lookup"><span data-stu-id="85b95-121">This section contains example code and step-by-step procedures.</span></span>                           |
| [<span data-ttu-id="85b95-122">Referência de programação de plug-ins do DSP</span><span class="sxs-lookup"><span data-stu-id="85b95-122">DSP Plug-ins Programming Reference</span></span>](dsp-plug-ins-programming-reference.md) | <span data-ttu-id="85b95-123">Fornece uma referência detalhada para as interfaces COM, os métodos e os tipos enumerados suportados pelo SDK do Windows Media Player para plug-ins do DSP.</span><span class="sxs-lookup"><span data-stu-id="85b95-123">Provides a detailed reference for the COM interfaces, methods, and enumerated types supported by the Windows Media Player SDK for DSP plug-ins.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="85b95-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="85b95-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85b95-125">**Plug-ins do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="85b95-125">**Windows Media Player Plug-ins**</span></span>](windows-media-player-plug-ins.md)
</dt> </dl>

 

 




