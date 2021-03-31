---
title: Criando um arquivo de definição de capa
description: Criando um arquivo de definição de capa
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Capas móveis do Windows Media Player, arquivos de definição de capa
- capas, arquivos de definição de capa
- arquivos para capas, definição de capa
- arquivos de definição de capa, criando
- Criando capas, sobre
- Criando capas, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8a2920a08a3f57f740ff5ed3ca6e291ffd1bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636309"
---
# <a name="creating-a-skin-definition-file"></a><span data-ttu-id="8aca3-109">Criando um arquivo de definição de capa</span><span class="sxs-lookup"><span data-stu-id="8aca3-109">Creating a Skin Definition File</span></span>

<span data-ttu-id="8aca3-110">Um arquivo de definição de capa é um arquivo de texto que define uma capa e todas as suas partes de composição.</span><span class="sxs-lookup"><span data-stu-id="8aca3-110">A skin definition file is a text file that defines a skin and all its composite parts.</span></span> <span data-ttu-id="8aca3-111">A extensão de nome de arquivo deve ser. skn.</span><span class="sxs-lookup"><span data-stu-id="8aca3-111">The file name extension must be .skn.</span></span>

<span data-ttu-id="8aca3-112">Todo arquivo de definição de capa deve começar com a linha a seguir, que especifica o número de versão do arquivo de capa.</span><span class="sxs-lookup"><span data-stu-id="8aca3-112">Every skin definition file must start with the following line, which specifies the skin file version number.</span></span> <span data-ttu-id="8aca3-113">A tabela a seguir mostra as versões do Windows Media Player e a linha de código que devem ser usadas para identificar cada uma em um arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="8aca3-113">The following table shows Windows Media Player versions and the code line that should be used to identify each in a skin definition file.</span></span> <span data-ttu-id="8aca3-114">Embora alguns dos números nas linhas de código não sejam o que você espera, eles estão corretos, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8aca3-114">Although some of the numbers in the code lines are not what you would expect, they are correct as shown in the following table.</span></span>



| <span data-ttu-id="8aca3-115">Versão do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="8aca3-115">Windows Media Player version</span></span> | <span data-ttu-id="8aca3-116">Primeira linha do arquivo de definição de capa</span><span class="sxs-lookup"><span data-stu-id="8aca3-116">First line of skin definition file</span></span> |
|------------------------------|------------------------------------|
| <span data-ttu-id="8aca3-117">1.01.1</span><span class="sxs-lookup"><span data-stu-id="8aca3-117">1.01.1</span></span><br/>            | <span data-ttu-id="8aca3-118">\[Arquivo de capa do Pocket WMP v 1.0\]</span><span class="sxs-lookup"><span data-stu-id="8aca3-118">\[Pocket WMP Skin File v1.0\]</span></span>      |
| <span data-ttu-id="8aca3-119">1.2</span><span class="sxs-lookup"><span data-stu-id="8aca3-119">1.2</span></span>                          | <span data-ttu-id="8aca3-120">\[Arquivo de capa do Pocket WMP v 1.2\]</span><span class="sxs-lookup"><span data-stu-id="8aca3-120">\[Pocket WMP Skin File v1.2\]</span></span>      |
| <span data-ttu-id="8aca3-121">7.0</span><span class="sxs-lookup"><span data-stu-id="8aca3-121">7.0</span></span>                          | <span data-ttu-id="8aca3-122">\[Arquivo de capa do Pocket WMP v 2.0\]</span><span class="sxs-lookup"><span data-stu-id="8aca3-122">\[Pocket WMP Skin File v2.0\]</span></span>      |
| <span data-ttu-id="8aca3-123">7.1</span><span class="sxs-lookup"><span data-stu-id="8aca3-123">7.1</span></span>                          | <span data-ttu-id="8aca3-124">\[Arquivo de capa do Pocket WMP v 8.0\]</span><span class="sxs-lookup"><span data-stu-id="8aca3-124">\[Pocket WMP Skin File v8.0\]</span></span>      |
| <span data-ttu-id="8aca3-125">9 Series</span><span class="sxs-lookup"><span data-stu-id="8aca3-125">9 Series</span></span>                     | <span data-ttu-id="8aca3-126">\[Arquivo de capa 9.0.1 do Pocket WMP v\]</span><span class="sxs-lookup"><span data-stu-id="8aca3-126">\[Pocket WMP Skin File v9.0.1\]</span></span>    |
| <span data-ttu-id="8aca3-127">10 Mobile</span><span class="sxs-lookup"><span data-stu-id="8aca3-127">10 Mobile</span></span>                    | <span data-ttu-id="8aca3-128">\[Arquivo de capa 9.0.1 do Pocket WMP v\]</span><span class="sxs-lookup"><span data-stu-id="8aca3-128">\[Pocket WMP Skin File v9.0.1\]</span></span>    |
| <span data-ttu-id="8aca3-129">10,1 móvel</span><span class="sxs-lookup"><span data-stu-id="8aca3-129">10.1 Mobile</span></span>                  | <span data-ttu-id="8aca3-130">\[Arquivo de capa 9.0.1 do Pocket WMP v\]</span><span class="sxs-lookup"><span data-stu-id="8aca3-130">\[Pocket WMP Skin File v9.0.1\]</span></span>    |



 

<span data-ttu-id="8aca3-131">O número de versão 9.0.1 é para capas criadas especificamente para o Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8aca3-131">The version number 9.0.1 is for skins created specifically for Windows Media Player 9 Series or later.</span></span> <span data-ttu-id="8aca3-132">As capas com um número de versão anterior são abertas pelo Windows Media Player 9 Series ou posterior como modo retrato, 96 pontos por polegada (DPI).</span><span class="sxs-lookup"><span data-stu-id="8aca3-132">Skins having an earlier version number are opened by Windows Media Player 9 Series or later as portrait mode, 96 dots per inch (DPI) skins.</span></span>

<span data-ttu-id="8aca3-133">O arquivo de definição de capa consiste em várias seções.</span><span class="sxs-lookup"><span data-stu-id="8aca3-133">The skin definition file consists of several sections.</span></span> <span data-ttu-id="8aca3-134">Cada seção define uma área específica da capa.</span><span class="sxs-lookup"><span data-stu-id="8aca3-134">Each section defines a particular area of the skin.</span></span> <span data-ttu-id="8aca3-135">As seções devem ser colocadas na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="8aca3-135">The sections must be placed in the following order:</span></span>

1.  <span data-ttu-id="8aca3-136">Description</span><span class="sxs-lookup"><span data-stu-id="8aca3-136">Description</span></span>
2.  <span data-ttu-id="8aca3-137">Bitmaps</span><span class="sxs-lookup"><span data-stu-id="8aca3-137">Bitmaps</span></span>
3.  <span data-ttu-id="8aca3-138">Vídeo</span><span class="sxs-lookup"><span data-stu-id="8aca3-138">Video</span></span>
4.  <span data-ttu-id="8aca3-139">Botões</span><span class="sxs-lookup"><span data-stu-id="8aca3-139">Buttons</span></span>
5.  <span data-ttu-id="8aca3-140">Status</span><span class="sxs-lookup"><span data-stu-id="8aca3-140">Status</span></span>
6.  <span data-ttu-id="8aca3-141">Texto</span><span class="sxs-lookup"><span data-stu-id="8aca3-141">Text</span></span>
7.  <span data-ttu-id="8aca3-142">Marquee</span><span class="sxs-lookup"><span data-stu-id="8aca3-142">Marquee</span></span>
8.  <span data-ttu-id="8aca3-143">Trackbars</span><span class="sxs-lookup"><span data-stu-id="8aca3-143">Trackbars</span></span>

<span data-ttu-id="8aca3-144">Cada seção começa com o nome da seção entre colchetes, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8aca3-144">Each section starts with the name of the section in square brackets, for example:</span></span>


```C++
[ Bitmaps ]

```



> [!Note]  
> <span data-ttu-id="8aca3-145">O arquivo de definição de capa não será analisado corretamente, a menos que você inclua espaços entre colchetes e o nome da seção.</span><span class="sxs-lookup"><span data-stu-id="8aca3-145">Your skin definition file will not be parsed correctly unless you include spaces between the brackets and the name of the section.</span></span>

 

<span data-ttu-id="8aca3-146">Em seguida, uma ou mais linhas definem imagens individuais, botões e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8aca3-146">Then, one or more lines define individual images, buttons, and so on.</span></span> <span data-ttu-id="8aca3-147">Por exemplo, uma seção bitmaps pode incluir o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8aca3-147">For example, a Bitmaps section might include the following:</span></span>


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



<span data-ttu-id="8aca3-148">Não é necessário alinhar os valores em colunas, mas isso ajudará o seu código a ser mais legível.</span><span class="sxs-lookup"><span data-stu-id="8aca3-148">It is not necessary to line up the values in columns, but it will help your code to be more readable.</span></span> <span data-ttu-id="8aca3-149">Para obter mais detalhes sobre cada seção do arquivo de definição de capa, consulte a [referência de capa](skin-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8aca3-149">For more details about each section of the skin definition file, see the [Skin Reference](skin-reference.md).</span></span>

> [!Note]  
> <span data-ttu-id="8aca3-150">Não use guias em qualquer lugar do arquivo; em vez disso, use espaços extras.</span><span class="sxs-lookup"><span data-stu-id="8aca3-150">Do not use tabs anywhere in the file; use extra spaces instead.</span></span> <span data-ttu-id="8aca3-151">Isso é muito importante, pois pressionar a tecla TAB durante a gravação ou edição do arquivo de definição de capa fará com que toda a capa falhe.</span><span class="sxs-lookup"><span data-stu-id="8aca3-151">This is very important, because pressing the TAB key while writing or editing your skin definition file will cause the entire skin to fail.</span></span> <span data-ttu-id="8aca3-152">Cada linha deve ser concluída e não pode continuar em uma segunda linha.</span><span class="sxs-lookup"><span data-stu-id="8aca3-152">Each line must be complete and cannot continue onto a second line.</span></span> <span data-ttu-id="8aca3-153">Além disso, a região e os super valores são preteridos para capas usadas com o Windows Media Player 10 Mobile ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8aca3-153">Also, the Region and Super values are deprecated for skins used with Windows Media Player 10 Mobile or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8aca3-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8aca3-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8aca3-155">**Arquivo de definição de capa**</span><span class="sxs-lookup"><span data-stu-id="8aca3-155">**Skin Definition File**</span></span>](skin-definition-file-mobile.md)
</dt> </dl>

 

 





