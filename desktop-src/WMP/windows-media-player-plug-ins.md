---
title: Plug-ins do Windows Media Player
description: Plug-ins do Windows Media Player
ms.assetid: 6265084b-e1ff-455b-aca8-dc008d94ed43
keywords:
- Windows Media Player, plug-ins
- Plug-ins do Windows Media Player, sobre
- plug-ins, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7d666874590f380e6f3828031b297d483ffff7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105785198"
---
# <a name="windows-media-player-plug-ins"></a><span data-ttu-id="bcb27-106">Plug-ins do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="bcb27-106">Windows Media Player Plug-ins</span></span>

<span data-ttu-id="bcb27-107">O Microsoft Windows Media Player expõe interfaces que permitem estender a funcionalidade de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="bcb27-107">Microsoft Windows Media Player exposes interfaces that allow you to extend functionality in several ways.</span></span> <span data-ttu-id="bcb27-108">As seções a seguir descrevem as arquiteturas de plug-ins com suporte e o processo de criação de um plug-in:</span><span class="sxs-lookup"><span data-stu-id="bcb27-108">The following sections describe the supported plug-in architectures and the process of building a plug-in:</span></span>



| <span data-ttu-id="bcb27-109">Seção</span><span class="sxs-lookup"><span data-stu-id="bcb27-109">Section</span></span>                                                                                                         | <span data-ttu-id="bcb27-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="bcb27-110">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bcb27-111">Criando um plug-in</span><span class="sxs-lookup"><span data-stu-id="bcb27-111">Building a Plug-in</span></span>](building-a-plug-in.md)                                                                    | <span data-ttu-id="bcb27-112">Você pode criar vários tipos de plug-ins usando o Visual Studio e o assistente de plug-in do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bcb27-112">You can build several types of plug-ins by using Visual Studio and the Windows Media Player plug-in wizard.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="bcb27-113">Visualizações personalizadas do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="bcb27-113">Windows Media Player Custom Visualizations</span></span>](windows-media-player-custom-visualizations.md)                    | <span data-ttu-id="bcb27-114">As visualizações do Windows Media Player são objetos Component Object Model (COM) usados para exibir imagens visuais que são sincronizadas com a parte de áudio da reprodução de mídia do Player.</span><span class="sxs-lookup"><span data-stu-id="bcb27-114">Windows Media Player visualizations are Component Object Model (COM) objects used to display visual imagery that is synchronized to the audio portion of the media playback of the player.</span></span> <span data-ttu-id="bcb27-115">As visualizações personalizadas podem ser criadas usando Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="bcb27-115">Custom visualizations can be created using Microsoft Visual C++.</span></span>                                             |
| [<span data-ttu-id="bcb27-116">Plug-ins de interface do usuário do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="bcb27-116">Windows Media Player User Interface Plug-ins</span></span>](windows-media-player-user-interface-plug-ins.md)                | <span data-ttu-id="bcb27-117">Os plug-ins de interface de usuário do Windows Media Player adicionam nova funcionalidade ao painel em **execução** do player de modo completo.</span><span class="sxs-lookup"><span data-stu-id="bcb27-117">Windows Media Player user interface plug-ins add new functionality to the **Now Playing** pane of the full mode Player.</span></span> <span data-ttu-id="bcb27-118">Você pode criar plug-ins que usam a área de visualização, uma janela separada, a área de configurações, a área de metadados ou plug-ins de segundo plano que não expõem nenhuma interface de usuário visível.</span><span class="sxs-lookup"><span data-stu-id="bcb27-118">You can create plug-ins that use the visualization area, a separate window, the settings area, the metadata area, or background plug-ins that expose no visible user interface.</span></span> |
| [<span data-ttu-id="bcb27-119">Plug-ins de DSP do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="bcb27-119">Windows Media Player DSP Plug-ins</span></span>](windows-media-player-dsp-plug-ins.md)                                      | <span data-ttu-id="bcb27-120">Os plug-ins do DSP do Windows Media Player modificam ou processam dados de áudio e vídeo antes de serem renderizados pelo Player.</span><span class="sxs-lookup"><span data-stu-id="bcb27-120">Windows Media Player DSP plug-ins modify or process audio and video data before it is rendered by the Player.</span></span> <span data-ttu-id="bcb27-121">Plug-ins do DSP são objetos de mídia do DirectX (DMO) que se conectam ao Player por meio de interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="bcb27-121">DSP plug-ins are DirectX Media Objects (DMO) that connect to the Player through COM interfaces.</span></span>                                                                                           |
| <span data-ttu-id="bcb27-122">[Plug-ins de renderização do Windows Media Player (preterido)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bcb27-122">[Windows Media Player Rendering Plug-ins (deprecated)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85))</span></span> | <span data-ttu-id="bcb27-123">Decodificação de plug-ins de renderização do Windows Media Player (se necessário) e renderização de dados personalizados contidos em um fluxo de formato de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="bcb27-123">Windows Media Player rendering plug-ins decode (if necessary) and render custom data contained in a Windows Media format stream.</span></span> <span data-ttu-id="bcb27-124">Os plug-ins de renderização são os objetos de mídia do DirectX (DMO) que se conectam ao Player por meio de interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="bcb27-124">Rendering plug-ins are DirectX Media Objects (DMO) that connect to the Player through COM interfaces.</span></span>                                                                  |
| [<span data-ttu-id="bcb27-125">Plug-ins de conversão do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="bcb27-125">Windows Media Player Conversion Plug-ins</span></span>](windows-media-player-conversion-plug-ins.md)                        | <span data-ttu-id="bcb27-126">Os plug-ins de conversão do Windows Media Player convertem arquivos de mídia digital criados usando tecnologias não fornecidas pela Microsoft no formato ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="bcb27-126">Windows Media Player conversion plug-ins convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).</span></span>                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="bcb27-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bcb27-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcb27-128">**SDK do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="bcb27-128">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 