---
title: Código completo para aparência simples
description: Código completo para aparência simples
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- Criando capas, exemplos de código
- Capas do Windows Media Player, exemplos de código
- capas, exemplos de código
- arquivos de definição de capa, exemplos de código
- Criando capas, exemplos
- Capas do Windows Media Player, exemplos
- capas, exemplos
- arquivos de definição de capa, exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682e6143c751d1c72cd8799f849fef7c9c27adb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822781"
---
# <a name="complete-code-for-simple-skin"></a><span data-ttu-id="33e15-111">Código completo para aparência simples</span><span class="sxs-lookup"><span data-stu-id="33e15-111">Complete Code for Simple Skin</span></span>

<span data-ttu-id="33e15-112">Este é o código completo da primeira capa de exemplo:</span><span class="sxs-lookup"><span data-stu-id="33e15-112">Here is the complete code for the first sample skin:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick="JScript: player.URL='https://proseware.com/laure.wma';" />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick = "JScript: view.close(); " />
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



<span data-ttu-id="33e15-113">Agora você tem todas as peças reunidas.</span><span class="sxs-lookup"><span data-stu-id="33e15-113">Now you have all the pieces put together.</span></span>

<span data-ttu-id="33e15-114">Crie um arquivo compactado com uma extensão de nome de arquivo. zip.</span><span class="sxs-lookup"><span data-stu-id="33e15-114">Create a compressed file with a .zip file name extension.</span></span> <span data-ttu-id="33e15-115">Esse arquivo compactado contém o arquivo de definição de capa, bitmaps e todos os arquivos de mídia digital que você deseja incluir.</span><span class="sxs-lookup"><span data-stu-id="33e15-115">This compressed file contains your skin definition file, bitmaps, and any digital media files you want to include.</span></span> <span data-ttu-id="33e15-116">Renomeie o arquivo para que ele tenha uma extensão de nome de arquivo. wmz.</span><span class="sxs-lookup"><span data-stu-id="33e15-116">Rename the file so that it has a .wmz file name extension.</span></span> <span data-ttu-id="33e15-117">Em seguida, clicar duas vezes em sua capa compactada a iniciará.</span><span class="sxs-lookup"><span data-stu-id="33e15-117">Then double-clicking your compressed skin will start it playing.</span></span>

<span data-ttu-id="33e15-118">Você pode ver uma aparência semelhante de trabalho simples na seção de exemplos do SDK.</span><span class="sxs-lookup"><span data-stu-id="33e15-118">You can see a similar working simple skin in the samples section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33e15-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33e15-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33e15-120">**Criando o arquivo de definição de capa**</span><span class="sxs-lookup"><span data-stu-id="33e15-120">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




