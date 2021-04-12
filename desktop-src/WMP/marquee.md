---
title: Marquee
description: Marquee
ms.assetid: 2715732a-25cc-4ba9-9aa6-181ebb9e1d1c
keywords:
- Aparências móveis do Windows Media Player, letreiros
- capas, letreiros
- referência para capas, letreiros
- marcas de aparência em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efa2db2c6079d47d207240b18a57ebbf7e41ae1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364232"
---
# <a name="marquee"></a><span data-ttu-id="bf1a4-107">Marquee</span><span class="sxs-lookup"><span data-stu-id="bf1a4-107">Marquee</span></span>

<span data-ttu-id="bf1a4-108">Um letreiro é uma caixa de exibição de texto de rolagem que exibe informações de uma ou mais caixas de exibição de texto.</span><span class="sxs-lookup"><span data-stu-id="bf1a4-108">A marquee is a scrolling text display box that displays information from one or more text display boxes.</span></span> <span data-ttu-id="bf1a4-109">Você não precisa adicionar um letreiro, mas ele pode ser muito útil quando você tem informações detalhadas que deseja exibir para o usuário em um espaço limitado.</span><span class="sxs-lookup"><span data-stu-id="bf1a4-109">You do not need to add a marquee, but it can be very useful when you have detailed information you want to display to the user in a limited space.</span></span>

<span data-ttu-id="bf1a4-110">O texto no letreiro será rolado somente se ambas as condições a seguir forem atendidas:</span><span class="sxs-lookup"><span data-stu-id="bf1a4-110">The text in the marquee will scroll only if both of the following conditions are met:</span></span>

-   <span data-ttu-id="bf1a4-111">Você tem mais texto a ser exibido no letreiro do que a largura da caixa de exibição do letreiro digital.</span><span class="sxs-lookup"><span data-stu-id="bf1a4-111">You have more text to display in the marquee than the width of the marquee display box.</span></span>
-   <span data-ttu-id="bf1a4-112">O item de mídia foi interrompido ou pausado.</span><span class="sxs-lookup"><span data-stu-id="bf1a4-112">The media item is either stopped or paused.</span></span>

<span data-ttu-id="bf1a4-113">A seção de letreiro do arquivo de definição de capa deve começar com esta linha:</span><span class="sxs-lookup"><span data-stu-id="bf1a4-113">The Marquee section of the skin definition file must begin with this line:</span></span>


```C++
[ Marquee ]

```



> [!Note]  
> <span data-ttu-id="bf1a4-114">Para manter a compatibilidade com versões do Windows Media Player Mobile anteriores ao Windows Media Player 10 Mobile, o uso de "Marquis" em um arquivo de definição de capa ainda é considerado válido.</span><span class="sxs-lookup"><span data-stu-id="bf1a4-114">To maintain compatibility with versions of Windows Media Player Mobile older than Windows Media Player 10 Mobile, using "Marquis" in a skin definition file is still considered valid.</span></span>

 

<span data-ttu-id="bf1a4-115">Em seguida, você deve adicionar uma ou mais linhas que contêm informações sobre cada uma das caixas de exibição do letreiro em sua capa.</span><span class="sxs-lookup"><span data-stu-id="bf1a4-115">You then must add one or more lines that contain information about each of the marquee display boxes in your skin.</span></span>


```C++
    3,2,234,20   Tahoma,12,N  255,0,0    Playlist, Time, Filename

```



<span data-ttu-id="bf1a4-116">Você pode usar o modelo a seguir para a seção de letreiro de seu arquivo de definição de capa:</span><span class="sxs-lookup"><span data-stu-id="bf1a4-116">You can use the following template for the Marquee section of your skin definition file:</span></span>


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------

```



<span data-ttu-id="bf1a4-117">Você deve usar a seguinte ordem para obter informações em cada linha da seção de letreiro (cada parte da linha é necessária):</span><span class="sxs-lookup"><span data-stu-id="bf1a4-117">You must use the following order for information in each line of the Marquee section (each part of the line is required):</span></span>

1.  [<span data-ttu-id="bf1a4-118">Local do letreiro</span><span class="sxs-lookup"><span data-stu-id="bf1a4-118">Marquee Location</span></span>](marquee-location.md)
2.  [<span data-ttu-id="bf1a4-119">Fonte do letreiro</span><span class="sxs-lookup"><span data-stu-id="bf1a4-119">Marquee Font</span></span>](marquee-font.md)
3.  [<span data-ttu-id="bf1a4-120">Cor do letreiro</span><span class="sxs-lookup"><span data-stu-id="bf1a4-120">Marquee Color</span></span>](marquee-color.md)
4.  [<span data-ttu-id="bf1a4-121">Combinações de texto</span><span class="sxs-lookup"><span data-stu-id="bf1a4-121">Text Combinations</span></span>](text-combinations.md)

<span data-ttu-id="bf1a4-122">Para obter um exemplo de código de letreiro, consulte a [seção letreiro de exemplo](sample-marquee-section.md).</span><span class="sxs-lookup"><span data-stu-id="bf1a4-122">For an example of Marquee code, see [Sample Marquee Section](sample-marquee-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf1a4-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf1a4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf1a4-124">**Referência de capa**</span><span class="sxs-lookup"><span data-stu-id="bf1a4-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




