---
title: Exemplo de arte simples
description: Exemplo de arte simples
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Capas do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, exemplos
- Capas do Windows Media Player, exemplos
- capas, exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab7b25dc33da70a627f8b0e126d6797b1bcdd9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635738"
---
# <a name="simple-art-example"></a><span data-ttu-id="02c83-109">Exemplo de arte simples</span><span class="sxs-lookup"><span data-stu-id="02c83-109">Simple Art Example</span></span>

<span data-ttu-id="02c83-110">Três arquivos Art são necessários para criar uma aparência simples com dois botões.</span><span class="sxs-lookup"><span data-stu-id="02c83-110">Three art files are needed to create a simple skin with two buttons.</span></span> <span data-ttu-id="02c83-111">Uma imagem primária e uma imagem de mapeamento são necessárias e uma imagem alternativa fornece uma indicação visual para o usuário de que um botão é clicável.</span><span class="sxs-lookup"><span data-stu-id="02c83-111">A primary image and a mapping image are required, and an alternate image provides a visual cue to the user that a button is clickable.</span></span>

<span data-ttu-id="02c83-112">Esses arquivos de arte foram criados em um programa de arte que usa camadas.</span><span class="sxs-lookup"><span data-stu-id="02c83-112">These art files were created in an art program that uses layers.</span></span> <span data-ttu-id="02c83-113">O uso de camadas facilita a tarefa de garantir que suas imagens primárias, de mapeamento e alternativas tenham o mesmo tamanho e fiquem alinhadas umas com as outras.</span><span class="sxs-lookup"><span data-stu-id="02c83-113">Using layers makes it easier to make sure that your primary, mapping, and alternate images are all the same size and line up with each other.</span></span>

<span data-ttu-id="02c83-114">As instruções detalhadas sobre como criar a arte estão no [Guia de criação de capas](skin-creation-guide.md).</span><span class="sxs-lookup"><span data-stu-id="02c83-114">The detailed instructions on creating the art are in the [Skin Creation Guide](skin-creation-guide.md).</span></span>

## <a name="primary-image"></a><span data-ttu-id="02c83-115">Imagem primária</span><span class="sxs-lookup"><span data-stu-id="02c83-115">Primary Image</span></span>

<span data-ttu-id="02c83-116">A imagem primária é uma elipse amarela simples com dois botões, um rosa para iniciar o Windows Media Player e o botão roxo para interrompê-lo.</span><span class="sxs-lookup"><span data-stu-id="02c83-116">The primary image is a simple yellow oval with two buttons, a pink one to start Windows Media Player and purple button to stop it.</span></span> <span data-ttu-id="02c83-117">O plano de fundo é um pouco mais escuro amarelo do que o oval.</span><span class="sxs-lookup"><span data-stu-id="02c83-117">The background is a slightly darker yellow than the oval.</span></span> <span data-ttu-id="02c83-118">Essa imagem é mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="02c83-118">This image is shown in the following illustration.</span></span>

![imagem primária](images/absam01b.png)

<span data-ttu-id="02c83-120">A imagem primária era das imagens a seguir, cada uma em uma camada separada.</span><span class="sxs-lookup"><span data-stu-id="02c83-120">The primary image was from the following images, each in a separate layer.</span></span> <span data-ttu-id="02c83-121">Primeiro, uma oval foi criada com um efeito de bisel de camada e de entalhe.</span><span class="sxs-lookup"><span data-stu-id="02c83-121">First an oval was created with a layer bevel and emboss effect.</span></span> <span data-ttu-id="02c83-122">Essa imagem é mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="02c83-122">This image is shown in the following illustration.</span></span>

![imagem oval](images/absam01s.png)

<span data-ttu-id="02c83-124">Em seguida, os dois botões foram criados, também com efeitos de chanfro de camada e de entalhe.</span><span class="sxs-lookup"><span data-stu-id="02c83-124">Then the two buttons were created, also with layer bevel and emboss effects.</span></span> <span data-ttu-id="02c83-125">Isso é mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="02c83-125">This is shown in the following illustration.</span></span>

![dois botões](images/absam01p.png)

<span data-ttu-id="02c83-127">Em seguida, o plano de fundo da imagem foi criado.</span><span class="sxs-lookup"><span data-stu-id="02c83-127">Next the image background was created.</span></span> <span data-ttu-id="02c83-128">Um amarelo ligeiramente mais escuro foi escolhido para que qualquer suavização entre a oval e o plano de fundo não seja notado.</span><span class="sxs-lookup"><span data-stu-id="02c83-128">A slightly darker yellow was chosen so that any anti-aliasing between the oval and the background will not be noticed.</span></span> <span data-ttu-id="02c83-129">O valor de cor é \# CCCC00.</span><span class="sxs-lookup"><span data-stu-id="02c83-129">The color value is \#CCCC00.</span></span> <span data-ttu-id="02c83-130">Essa imagem é mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="02c83-130">This image is shown in the following illustration.</span></span>

![imagem de plano de fundo](images/absam01y.png)

<span data-ttu-id="02c83-132">As camadas que continham essas imagens foram tornadas visíveis e salvas como uma cópia no formato de bitmap, criando a imagem primária.</span><span class="sxs-lookup"><span data-stu-id="02c83-132">The layers that contained these images were made visible and saved as a copy in bitmap format, creating the primary image.</span></span> <span data-ttu-id="02c83-133">A imagem composta primária será usada pelo atributo **backgroundImage** do elemento **View** .</span><span class="sxs-lookup"><span data-stu-id="02c83-133">The primary composite image will be used by the **backgroundImage** attribute of the **VIEW** element.</span></span>

## <a name="mapping-image"></a><span data-ttu-id="02c83-134">Imagem de mapeamento</span><span class="sxs-lookup"><span data-stu-id="02c83-134">Mapping Image</span></span>

<span data-ttu-id="02c83-135">Uma imagem de mapeamento é necessária para especificar quando e onde uma capa é clicada.</span><span class="sxs-lookup"><span data-stu-id="02c83-135">A mapping image is needed to specify when and where a skin is clicked.</span></span> <span data-ttu-id="02c83-136">Uma imagem de mapeamento foi criada com uma área vermelha e uma área verde.</span><span class="sxs-lookup"><span data-stu-id="02c83-136">A mapping image was created with a red area and a green area.</span></span> <span data-ttu-id="02c83-137">Essa imagem é mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="02c83-137">This image is shown in the following illustration.</span></span>

![imagem de mapeamento](images/absam01m.png)

<span data-ttu-id="02c83-139">A área verde será usada para identificar a área na capa que iniciará o Windows Media Player e a área vermelha será usada para interrompê-la.</span><span class="sxs-lookup"><span data-stu-id="02c83-139">The green area will be used to identify the area on the skin that will start Windows Media Player and the red area will be used to stop it.</span></span> <span data-ttu-id="02c83-140">A imagem de mapeamento tem o mesmo tamanho da imagem primária.</span><span class="sxs-lookup"><span data-stu-id="02c83-140">The mapping image is the same size as the primary image.</span></span>

<span data-ttu-id="02c83-141">A imagem de mapeamento foi criada copiando a camada de botão para uma nova camada e desativando o efeito de bisel e entalhe.</span><span class="sxs-lookup"><span data-stu-id="02c83-141">The mapping image was created by copying the button layer to a new layer and turning off the bevel and emboss effect.</span></span> <span data-ttu-id="02c83-142">As imagens simples são necessárias para o mapeamento, pois o Windows Media Player procurará por valores de cor únicos em cada área.</span><span class="sxs-lookup"><span data-stu-id="02c83-142">Flat images are needed for mapping because Windows Media Player will be looking for single color values in each area.</span></span> <span data-ttu-id="02c83-143">Ele só pode pesquisar por uma cor que você definir, como vermelho ( \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="02c83-143">It can only search for a color you define, such as red (\#FF0000).</span></span> <span data-ttu-id="02c83-144">Se a imagem tiver um chanfro ou outro efeito, nem todos eles serão o vermelho exato de que você precisa.</span><span class="sxs-lookup"><span data-stu-id="02c83-144">If your image has a bevel or other effect, not all of it will be the exact red you need.</span></span>

<span data-ttu-id="02c83-145">Para tornar os botões de mapeamento uma cor fácil de se lembrar, as imagens foram preenchidas com vermelho puro e verde puro, mas qualquer cor pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="02c83-145">To make the mapping buttons an easy color to remember, the images were filled with pure red and pure green, but any color can be used.</span></span> <span data-ttu-id="02c83-146">Você precisará se lembrar dos números de cor em seu mapa para que eles possam ser inseridos no arquivo de definição de aparência XML.</span><span class="sxs-lookup"><span data-stu-id="02c83-146">You will need to remember the color numbers in your map so that they can be entered in the XML skin definition file.</span></span> <span data-ttu-id="02c83-147">Nesse caso, Red é \# FF0000 e Green é \# 00FF00.</span><span class="sxs-lookup"><span data-stu-id="02c83-147">In this case, red is \#FF0000 and green is \#00FF00.</span></span>

<span data-ttu-id="02c83-148">Em seguida, com apenas a nova camada visível, a imagem foi salva como uma cópia em um arquivo BMP.</span><span class="sxs-lookup"><span data-stu-id="02c83-148">Then, with only the new layer visible, the image was saved as a copy to a BMP file.</span></span> <span data-ttu-id="02c83-149">Ele será chamado pelo atributo **mappingImage** do elemento **Button** .</span><span class="sxs-lookup"><span data-stu-id="02c83-149">It will be called by the **mappingImage** attribute of the **BUTTONGROUP** element.</span></span>

## <a name="alternate-image"></a><span data-ttu-id="02c83-150">Imagem alternativa</span><span class="sxs-lookup"><span data-stu-id="02c83-150">Alternate Image</span></span>

<span data-ttu-id="02c83-151">Imagens alternativas não são necessárias, mas são muito úteis para dar indicações visuais ao usuário.</span><span class="sxs-lookup"><span data-stu-id="02c83-151">Alternate images are not required but are very useful to give visual cues to the user.</span></span> <span data-ttu-id="02c83-152">Nesse caso, uma imagem em foco é recomendada para que o usuário saiba em quais áreas podem ser clicadas.</span><span class="sxs-lookup"><span data-stu-id="02c83-152">In this case, a hover image is recommended so that the user knows what areas can be clicked on.</span></span>

<span data-ttu-id="02c83-153">Uma imagem alternativa foi criada com dois botões amarelos.</span><span class="sxs-lookup"><span data-stu-id="02c83-153">An alternate image was created with two yellow buttons.</span></span> <span data-ttu-id="02c83-154">Isso é mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="02c83-154">This is shown in the following illustration.</span></span>

![imagem em foco](images/absam01h.png)

<span data-ttu-id="02c83-156">A imagem alternativa foi criada copiando a camada do botão original para uma nova camada e, em seguida, alterando a cor de preenchimento para amarelo.</span><span class="sxs-lookup"><span data-stu-id="02c83-156">The alternate image was created by copying the original button layer to a new layer and then changing the fill color to yellow.</span></span> <span data-ttu-id="02c83-157">O efeito de bisel e entalhe foi mantido.</span><span class="sxs-lookup"><span data-stu-id="02c83-157">The bevel and emboss effect was kept.</span></span> <span data-ttu-id="02c83-158">Em seguida, uma nova camada foi criada e as imagens foram adicionadas: a seta indica "Play" e o quadrado indica "Stop".</span><span class="sxs-lookup"><span data-stu-id="02c83-158">Then a new layer was created and images were added: the arrow indicates "play" and the square indicates "stop".</span></span> <span data-ttu-id="02c83-159">Em seguida, com apenas o novo botão amarelo e as camadas de tipo visíveis, a imagem foi salva como uma cópia em um arquivo de bitmap.</span><span class="sxs-lookup"><span data-stu-id="02c83-159">Then, with only the new yellow button and type layers visible, the image was saved as a copy to a bitmap file.</span></span>

<span data-ttu-id="02c83-160">O resultado é que quando o mouse passa sobre uma área definida pela imagem de mapeamento, a imagem em foco será exibida, alertando o leitor de que, se clicarem nesse ponto, poderão reproduzir ou parar o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="02c83-160">The result is that when the mouse hovers over an area defined by the mapping image, the hover image will be displayed, alerting the reader that if they click on that spot, they can play or stop Windows Media Player.</span></span>

## <a name="final-image"></a><span data-ttu-id="02c83-161">Imagem final</span><span class="sxs-lookup"><span data-stu-id="02c83-161">Final Image</span></span>

<span data-ttu-id="02c83-162">Aqui está a imagem final da capa.</span><span class="sxs-lookup"><span data-stu-id="02c83-162">Here is the final image of the skin.</span></span>

![imagem final](images/absam01f.png)

<span data-ttu-id="02c83-164">Essa é a imagem que você verá se passar o mouse sobre o botão rosa à direita.</span><span class="sxs-lookup"><span data-stu-id="02c83-164">And this is the image you will see if you hover over the pink button on the right.</span></span>

![passar o mouse sobre o botão direito](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a><span data-ttu-id="02c83-166">Código XML para o exemplo de arte</span><span class="sxs-lookup"><span data-stu-id="02c83-166">XML Code for the Art Example</span></span>

<span data-ttu-id="02c83-167">Os detalhes de como escrever código XML são fornecidos no guia de [criação de capa](skin-creation-guide.md), mas para mostrar o quanto o código é necessário para criar uma aparência de trabalho, aqui está o código para o trabalho artístico neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="02c83-167">The details of how to write XML code are given in the [Skin Creation Guide](skin-creation-guide.md), but to show how little code is needed to create a working skin, here is the code for the artwork in this example.</span></span>

<span data-ttu-id="02c83-168">Botões predefinidos são usados para as funções Play e Stop.</span><span class="sxs-lookup"><span data-stu-id="02c83-168">Predefined buttons are used for the play and stop functions.</span></span> <span data-ttu-id="02c83-169">Você deve carregar um arquivo ou uma lista de reprodução da âncora do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="02c83-169">You must load a file or playlist from the Windows Media anchor.</span></span> <span data-ttu-id="02c83-170">Quando o Windows Media Player muda para o modo de capa, uma pequena caixa é exibida no canto inferior direito da tela.</span><span class="sxs-lookup"><span data-stu-id="02c83-170">When Windows Media Player changes to skin mode, a small box appears in the lower-right corner of the screen.</span></span> <span data-ttu-id="02c83-171">Essa caixa é chamada de "âncora".</span><span class="sxs-lookup"><span data-stu-id="02c83-171">This box is called the "anchor".</span></span> <span data-ttu-id="02c83-172">Clicar na âncora oferece a funcionalidade mínima necessária, caso uma capa não forneça uma maneira de retornar ao modo completo do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="02c83-172">Clicking the anchor gives you the minimum functionality needed, in case a skin does not provide a way to return to the full mode of Windows Media Player.</span></span> <span data-ttu-id="02c83-173">O usuário pode alternar entre os modos usando o menu **Exibir** se estiver em modo completo ou clicando na âncora se estiver no modo de capa.</span><span class="sxs-lookup"><span data-stu-id="02c83-173">The user can switch between modes by using the **View** menu if in full mode, or by clicking the anchor if in skin mode.</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">
                
        <PLAYELEMENT
            mappingColor = "#00FF00"/>

        <STOPELEMENT
            mappingColor = "#FF0000"/>
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



## <a name="related-topics"></a><span data-ttu-id="02c83-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02c83-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02c83-175">**Arquivos de arte**</span><span class="sxs-lookup"><span data-stu-id="02c83-175">**Art Files**</span></span>](art-files.md)
</dt> </dl>

 

 




