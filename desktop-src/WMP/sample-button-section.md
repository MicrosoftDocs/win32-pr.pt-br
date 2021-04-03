---
title: Seção de botão de exemplo
description: Seção de botão de exemplo
ms.assetid: 52358f83-8c74-4957-87c4-ca1ed7f667fc
keywords:
- Aparências móveis do Windows Media Player, seção de botão
- capas, seção de botão
- referência para capas, seção de botão
- botões em capas, seção de botão
- arquivos de definição de capa, seção de botão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c35a4efd0e52dd7f5fd0cf87fc269eb4a9f4c27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005761"
---
# <a name="sample-button-section"></a><span data-ttu-id="6a5bd-108">Seção de botão de exemplo</span><span class="sxs-lookup"><span data-stu-id="6a5bd-108">Sample Button Section</span></span>

<span data-ttu-id="6a5bd-109">As linhas a seguir mostram uma seção de botões típicos de um arquivo de definição de capa:</span><span class="sxs-lookup"><span data-stu-id="6a5bd-109">The following lines show a typical Buttons section of a skin definition file:</span></span>


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98
    Info       PushHit    97,49,43,43    Pushed @ 57,0     Disabled @ 57,0      0,  0,  0
    Stop       PushHit    97,173,43,43   Pushed @ 57,124   Disabled @ 57,124  255,255,  0
    Prev       PushHit    40,83,43,43    Pushed @ 0,34     Disabled @ 0,34      0,  0,255
    Next       PushHit    153,83,43,43   Pushed @ 113,34   Disabled @ 113,34  255,  0,  0
    Shuffle    ToggleHit  40,136,43,43   Pushed @ 0,87     Disabled @ 0,87      0,255,  0
    Repeat     ToggleHit  153,136,43,43  Pushed @ 113,87   Disabled @ 113,87  255,  0,255
    Mute       Toggle     5,220,24,23    Super @ 247,29    Super @ 4,28         0,  0,  0

```



<span data-ttu-id="6a5bd-110">Esse código define oito botões que são usados para fornecer todas as seguintes funções em uma capa:</span><span class="sxs-lookup"><span data-stu-id="6a5bd-110">This code defines eight buttons that are used to provide all of the following functions in a skin:</span></span>

-   <span data-ttu-id="6a5bd-111">Reproduzir, pausar e parar itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="6a5bd-111">Play, pause, and stop media items.</span></span>
-   <span data-ttu-id="6a5bd-112">Embaralhar, repetir e percorrer a lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="6a5bd-112">Shuffle, repeat, and move through the playlist.</span></span>
-   <span data-ttu-id="6a5bd-113">Ativar mudo do volume.</span><span class="sxs-lookup"><span data-stu-id="6a5bd-113">Mute the volume.</span></span>

<span data-ttu-id="6a5bd-114">Todos os botões, exceto o botão sem som, são botões de região.</span><span class="sxs-lookup"><span data-stu-id="6a5bd-114">All the buttons except the mute button are region buttons.</span></span> <span data-ttu-id="6a5bd-115">O botão mudo obtém suas imagens enviadas por push e desabilitadas do super bitmap para sua conveniência.</span><span class="sxs-lookup"><span data-stu-id="6a5bd-115">The mute button gets its Pushed and Disabled images from the Super bitmap for convenience.</span></span>

> [!Note]  
> <span data-ttu-id="6a5bd-116">Os tipos de botões são preteridos em capas para Windows Media Player 10 Mobile ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6a5bd-116">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span> <span data-ttu-id="6a5bd-117">Em vez de um tipo de botão declarado em seu arquivo de capa, digite "NA" para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="6a5bd-117">Instead of a button type declared in your skin file, enter "NA" for each type.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6a5bd-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a5bd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a5bd-119">**Botões**</span><span class="sxs-lookup"><span data-stu-id="6a5bd-119">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




