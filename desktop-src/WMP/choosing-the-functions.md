---
title: Escolhendo as funções
description: Escolhendo as funções
ms.assetid: ded3c578-5087-4e4f-bf21-2149cf72719d
keywords:
- Capas móveis do Windows Media Player, funções para áudio
- capas, funções de áudio
- Criando capas, funções para áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a139dc21a7d10847a7920955988ec2b02fced0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364353"
---
# <a name="choosing-the-functions"></a><span data-ttu-id="2c6db-106">Escolhendo as funções</span><span class="sxs-lookup"><span data-stu-id="2c6db-106">Choosing the Functions</span></span>

<span data-ttu-id="2c6db-107">A finalidade dessa capa é fornecer a funcionalidade básica para a reprodução de áudio.</span><span class="sxs-lookup"><span data-stu-id="2c6db-107">The purpose of this skin is to provide basic functionality for playing audio.</span></span> <span data-ttu-id="2c6db-108">As seguintes funções serão usadas:</span><span class="sxs-lookup"><span data-stu-id="2c6db-108">The following functions will be used:</span></span>



| <span data-ttu-id="2c6db-109">Função</span><span class="sxs-lookup"><span data-stu-id="2c6db-109">Function</span></span>                     | <span data-ttu-id="2c6db-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c6db-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6db-111">PlayPause ou PlayPauseStop\*</span><span class="sxs-lookup"><span data-stu-id="2c6db-111">PlayPause or PlayPauseStop\*</span></span> | <span data-ttu-id="2c6db-112">Iniciar o item de mídia é de importância principal.</span><span class="sxs-lookup"><span data-stu-id="2c6db-112">Starting the media item is of prime importance.</span></span> <span data-ttu-id="2c6db-113">Se você estiver criando uma capa para o Windows Media Player 10 Mobile ou posterior, use PlayPauseStop.</span><span class="sxs-lookup"><span data-stu-id="2c6db-113">If you are creating a skin for Windows Media Player 10 Mobile or later, then you should use PlayPauseStop.</span></span> <span data-ttu-id="2c6db-114">Se você estiver trabalhando com uma versão anterior do Windows Media Player Mobile, deverá usar PlayPause.</span><span class="sxs-lookup"><span data-stu-id="2c6db-114">If you are working with an earlier version of Windows Media Player Mobile, then you must use PlayPause.</span></span> <span data-ttu-id="2c6db-115">Ambas as funções oferecem a funcionalidade adicional de pausar, mas somente PlayPauseStop permite que você interrompa uma transmissão ao vivo quando a funcionalidade de pausa não está disponível.</span><span class="sxs-lookup"><span data-stu-id="2c6db-115">Both functions give you the added functionality of pausing, but only PlayPauseStop allows you to stop a live broadcast when pause functionality is not available.</span></span> |
| <span data-ttu-id="2c6db-116">Stop</span><span class="sxs-lookup"><span data-stu-id="2c6db-116">Stop</span></span>                         | <span data-ttu-id="2c6db-117">Você desejará adicionar parar para parar de executar o item.</span><span class="sxs-lookup"><span data-stu-id="2c6db-117">You will want to add Stop to stop playing the item.</span></span> <span data-ttu-id="2c6db-118">Se você estiver criando uma capa para o Windows Media Player 10 Mobile ou posterior, a função PlayPauseStop já fornecerá essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="2c6db-118">If you are creating a skin for Windows Media Player 10 Mobile or later, the PlayPauseStop function already provides this functionality.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="2c6db-119">Avançar</span><span class="sxs-lookup"><span data-stu-id="2c6db-119">Next</span></span>                         | <span data-ttu-id="2c6db-120">Se você tiver uma lista de reprodução, será conveniente poder escolher o próximo item.</span><span class="sxs-lookup"><span data-stu-id="2c6db-120">If you have a playlist, you will want to be able to choose the next item.</span></span> <span data-ttu-id="2c6db-121">Você precisa disso para a navegação básica de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="2c6db-121">You need this for basic navigation of digital media.</span></span>                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2c6db-122">Prev</span><span class="sxs-lookup"><span data-stu-id="2c6db-122">Prev</span></span>                         | <span data-ttu-id="2c6db-123">Embora você possa usar avançar para percorrer a lista de reprodução até chegar ao início, adicionar anterior tornará mais fácil para o usuário voltar e para frente ao navegar na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="2c6db-123">While you could use Next to cycle through the playlist until you came to the beginning, adding Prev will make it easy for the user to go backward as well as forward when navigating the playlist.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="2c6db-124">VolumeUp ou VolumeDown\*</span><span class="sxs-lookup"><span data-stu-id="2c6db-124">VolumeUp or VolumeDown\*</span></span>     | <span data-ttu-id="2c6db-125">Você deverá fornecer ao usuário a capacidade de ativar ou desativar o volume.</span><span class="sxs-lookup"><span data-stu-id="2c6db-125">You will want to provide the user with the ability to turn the volume up or down.</span></span>                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="2c6db-126">\*Disponível para Windows Media Player 10 Mobile ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2c6db-126">\*Available for Windows Media Player 10 Mobile or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c6db-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c6db-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c6db-128">**Guia de aparência**</span><span class="sxs-lookup"><span data-stu-id="2c6db-128">**Skin Guide**</span></span>](skin-guide.md)
</dt> </dl>

 

 




