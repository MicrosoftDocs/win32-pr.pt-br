---
title: Criando o arquivo de arte principal
description: Criando o arquivo de arte principal
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- Criando capas, arquivos de arte principais
- Capas do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, imagens primárias
- Capas do Windows Media Player, imagens primárias
- capas, imagens primárias
- imagens primárias em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ceb92a5a87c1fc03ec7336a7ca5dd7814e4a1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104570562"
---
# <a name="creating-the-primary-art-file"></a><span data-ttu-id="95e5c-111">Criando o arquivo de arte principal</span><span class="sxs-lookup"><span data-stu-id="95e5c-111">Creating the Primary Art File</span></span>

<span data-ttu-id="95e5c-112">O arquivo de arte principal conterá a arte que o usuário da sua capa vê primeiro.</span><span class="sxs-lookup"><span data-stu-id="95e5c-112">The primary art file will contain the art that the user of your skin first sees.</span></span> <span data-ttu-id="95e5c-113">Nesse caso, você criará imagens em camadas diferentes do seu programa de arte.</span><span class="sxs-lookup"><span data-stu-id="95e5c-113">In this case, you will be creating images in different layers of your art program.</span></span> <span data-ttu-id="95e5c-114">O motivo para usar camadas é que você copiará camadas específicas posteriormente para criar arquivos de mapa e arquivos de arte alternativos.</span><span class="sxs-lookup"><span data-stu-id="95e5c-114">The reason for using layers is that you will copy specific layers later to create map files and alternate art files.</span></span>

<span data-ttu-id="95e5c-115">Para criar o arquivo de arte principal, você criará as seguintes camadas na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="95e5c-115">To create the primary art file, you will create the following layers in the following order:</span></span>

<span data-ttu-id="95e5c-116">Camada de fundo de capa</span><span class="sxs-lookup"><span data-stu-id="95e5c-116">Skin background layer</span></span>

<span data-ttu-id="95e5c-117">Essa é a cor que será transparente quando a capa for exibida.</span><span class="sxs-lookup"><span data-stu-id="95e5c-117">This is the color that will be transparent when the skin is displayed.</span></span> <span data-ttu-id="95e5c-118">Crie uma camada para isso primeiro, mas escolha a cor final dessa camada depois de escolher uma cor para a camada de contêiner de capa.</span><span class="sxs-lookup"><span data-stu-id="95e5c-118">Create a layer for this first, but choose the final color of this layer after you chose a color for the skin container layer.</span></span> <span data-ttu-id="95e5c-119">Essa cor deve ser semelhante a, mas não a mesma que a camada de contêiner de capa, para ocultar quaisquer efeitos de suavização de alias.</span><span class="sxs-lookup"><span data-stu-id="95e5c-119">This color should be similar to, but not the same as, the skin container layer, to hide any anti-aliasing effects.</span></span>

<span data-ttu-id="95e5c-120">Camada de contêiner de capa</span><span class="sxs-lookup"><span data-stu-id="95e5c-120">Skin container layer</span></span>

<span data-ttu-id="95e5c-121">Essa é a imagem que formará o contorno da sua capa e será o que o usuário vê.</span><span class="sxs-lookup"><span data-stu-id="95e5c-121">This is the image that will form the outline of your skin and will be what the user sees.</span></span> <span data-ttu-id="95e5c-122">Ele também será o contêiner para os dois botões neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="95e5c-122">It also will be the container for the two buttons in this example.</span></span> <span data-ttu-id="95e5c-123">Imagine sua capa como um contêiner para controles de interface do usuário, como botões, controles deslizantes e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="95e5c-123">Think of your skin as a container for user interface controls such as buttons, sliders, and so on.</span></span> <span data-ttu-id="95e5c-124">Neste exemplo, o contêiner é uma elipse amarela.</span><span class="sxs-lookup"><span data-stu-id="95e5c-124">In this example, the container is a yellow oval.</span></span>

<span data-ttu-id="95e5c-125">Reproduzir e fechar camadas de botão</span><span class="sxs-lookup"><span data-stu-id="95e5c-125">Play and Close button layers</span></span>

<span data-ttu-id="95e5c-126">Esses são os dois controles de interface do usuário que este exemplo usa.</span><span class="sxs-lookup"><span data-stu-id="95e5c-126">These are the two user interface controls that this example uses.</span></span> <span data-ttu-id="95e5c-127">Você os colocará em camadas separadas para que possa ajustá-las facilmente ou copiá-las mais tarde.</span><span class="sxs-lookup"><span data-stu-id="95e5c-127">You will put them in separate layers so that you can easily adjust them or copy them later.</span></span>

<span data-ttu-id="95e5c-128">Antes de criar suas camadas, você deve criar o arquivo que manterá suas camadas.</span><span class="sxs-lookup"><span data-stu-id="95e5c-128">Before you create your layers, you must create the file that will hold your layers.</span></span> <span data-ttu-id="95e5c-129">Inicie o Photoshop e crie um novo arquivo com 100 pixels de altura e 200 pixels de largura.</span><span class="sxs-lookup"><span data-stu-id="95e5c-129">Start up Photoshop and create a new file that is 100 pixels high and 200 pixels wide.</span></span> <span data-ttu-id="95e5c-130">O arquivo usado para criar a arte para este exemplo é chamado de tiny.psd e está incluído no SDK.</span><span class="sxs-lookup"><span data-stu-id="95e5c-130">The file used to create the art for this sample is called tiny.psd and is included with the SDK.</span></span>

<span data-ttu-id="95e5c-131">Todas as instruções são fornecidas em termos do Photoshop, mas qualquer outro programa de arte pode ser usado para criar capas, desde que você possa salvar em um dos formatos de arquivo com suporte no Windows Media Player (BMP, GIF, JPG e PNG).</span><span class="sxs-lookup"><span data-stu-id="95e5c-131">All instructions are given in terms of Photoshop, but any other art program can be used to create skins as long as you can save to one of the file formats supported by the Windows Media Player (BMP, GIF, JPG, and PNG).</span></span> <span data-ttu-id="95e5c-132">Você encontrará uma criação de capa mais fácil se usar um programa de arte que tenha camadas, como Adobe Photoshop, Jasc Paint Shop Pro ou Jedor viscosity.</span><span class="sxs-lookup"><span data-stu-id="95e5c-132">You will find skin creation easier if you use an art program that has layers, such as Adobe Photoshop, Jasc Paint Shop Pro, or Jedor Viscosity.</span></span> <span data-ttu-id="95e5c-133">As camadas são extremamente úteis porque as imagens devem estar alinhadas corretamente para o mapeamento de imagem e a exibição de imagens alternativas.</span><span class="sxs-lookup"><span data-stu-id="95e5c-133">Layers are extremely useful because images must be properly aligned for image mapping and display of alternative images.</span></span>

## <a name="skin-background-layer"></a><span data-ttu-id="95e5c-134">Camada de fundo de capa</span><span class="sxs-lookup"><span data-stu-id="95e5c-134">Skin Background Layer</span></span>

<span data-ttu-id="95e5c-135">Crie uma nova camada e nomeie-a como "fundo da capa".</span><span class="sxs-lookup"><span data-stu-id="95e5c-135">Create a new layer and name it "Skin background".</span></span> <span data-ttu-id="95e5c-136">Isso se tornará a cor de transparência que você definirá no arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="95e5c-136">This will become the transparency color you will define in the skin definition file.</span></span> <span data-ttu-id="95e5c-137">Aguarde até que a cor do contêiner de capa seja escolhida antes de preencher a camada de plano de fundo da capa com uma cor específica.</span><span class="sxs-lookup"><span data-stu-id="95e5c-137">Wait until the color for the skin container is chosen before filling the skin background layer with a specific color.</span></span>

## <a name="skin-container-layer"></a><span data-ttu-id="95e5c-138">Camada de contêiner de capa</span><span class="sxs-lookup"><span data-stu-id="95e5c-138">Skin Container Layer</span></span>

<span data-ttu-id="95e5c-139">Em seguida, crie uma nova camada e chame-a de "contêiner de capa".</span><span class="sxs-lookup"><span data-stu-id="95e5c-139">Next create a new layer and call it "Skin container".</span></span> <span data-ttu-id="95e5c-140">Isso definirá as bordas da sua capa e será o contêiner para os botões.</span><span class="sxs-lookup"><span data-stu-id="95e5c-140">This will define the edges of your skin and will be the container for the buttons.</span></span>

<span data-ttu-id="95e5c-141">Escolha uma cor de primeiro plano para a forma, usando os controles deslizantes de cores da Web.</span><span class="sxs-lookup"><span data-stu-id="95e5c-141">Choose a foreground color for the shape, using the Web color sliders.</span></span> <span data-ttu-id="95e5c-142">Neste exemplo, a cor " \# DBDD11" foi escolhida.</span><span class="sxs-lookup"><span data-stu-id="95e5c-142">In this example, the color "\#DBDD11" was chosen.</span></span>

<span data-ttu-id="95e5c-143">Em seguida, crie uma forma oval.</span><span class="sxs-lookup"><span data-stu-id="95e5c-143">Next create an oval shape.</span></span> <span data-ttu-id="95e5c-144">A maneira mais fácil é usar a ferramenta Eliptical Marquee e criar uma seleção de oval.</span><span class="sxs-lookup"><span data-stu-id="95e5c-144">The easiest way is to use the Eliptical Marquee tool and create an oval selection.</span></span> <span data-ttu-id="95e5c-145">Quando você tiver criado uma seleção de oval que é o tamanho e a forma desejados, preencha a seleção com a cor de primeiro plano e cancele a seleção.</span><span class="sxs-lookup"><span data-stu-id="95e5c-145">When you have created an oval selection that is the size and shape you want, fill the selection with the foreground color and cancel the selection.</span></span>

<span data-ttu-id="95e5c-146">Por fim, para tornar essa aparência um pouco mais interessante, aplique o efeito de camada de bisel e entalhe com os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="95e5c-146">Finally, to make this look a bit more interesting, apply the layer effect of Bevel and Emboss with the default values.</span></span>

<span data-ttu-id="95e5c-147">Sua camada de contêiner de capa deve ser parecida com a ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="95e5c-147">Your skin container layer should look like the following illustration.</span></span>

![camada de contêiner de capa](images/g01cont.png)

## <a name="background-skin-color"></a><span data-ttu-id="95e5c-149">Cor da capa em segundo plano</span><span class="sxs-lookup"><span data-stu-id="95e5c-149">Background Skin Color</span></span>

<span data-ttu-id="95e5c-150">Agora que você escolheu uma cor de primeiro plano para sua forma de contêiner de capa, você pode escolher uma cor semelhante para sua camada de plano de fundo de capa.</span><span class="sxs-lookup"><span data-stu-id="95e5c-150">Now that you have chosen a foreground color for your skin container shape, you can choose a similar color for your skin background layer.</span></span> <span data-ttu-id="95e5c-151">Você não quer exatamente a mesma cor ou seu contêiner de capa também será transparente.</span><span class="sxs-lookup"><span data-stu-id="95e5c-151">You do not want the exact same color, or your skin container will be transparent also.</span></span> <span data-ttu-id="95e5c-152">Na verdade, certifique-se de não usar essa cor exata em qualquer outro lugar na sua capa, mesmo em fotografias, porque sempre que essa cor é exibida, a imagem da área de trabalho será exibida em vez disso.</span><span class="sxs-lookup"><span data-stu-id="95e5c-152">In fact, be sure you do not use this exact color anywhere else in your skin, even in photographs, because wherever this color appears, the desktop image will appear instead.</span></span>

<span data-ttu-id="95e5c-153">Você deseja uma cor próxima à cor do contêiner da capa para evitar efeitos de suavização de alias.</span><span class="sxs-lookup"><span data-stu-id="95e5c-153">You want a color close to the skin container color to avoid anti-aliasing effects.</span></span> <span data-ttu-id="95e5c-154">Por exemplo, se você tiver um plano de fundo preto, alguns bits de preto poderão aparecer em toda a borda da sua capa.</span><span class="sxs-lookup"><span data-stu-id="95e5c-154">For example, if you have a black background, some bits of black may show up around the edge of your skin.</span></span> <span data-ttu-id="95e5c-155">Ao escolher uma cor perto da cor do contêiner de capa, todos os pixels isolados que aparecem no processo de suavização de serrilhado serão despercebidos.</span><span class="sxs-lookup"><span data-stu-id="95e5c-155">By choosing a color close to the color of the skin container, any stray pixels that show up in the anti-aliasing process will be unnoticed.</span></span>

<span data-ttu-id="95e5c-156">A suavização de serrilhado é o processo de suavização das bordas de formas inclinadas ou curvas.</span><span class="sxs-lookup"><span data-stu-id="95e5c-156">Anti-aliasing is the process of smoothing the edges of slanted or curved shapes.</span></span> <span data-ttu-id="95e5c-157">A suavização de serrilhado cria novas cores, para pixels ao longo das bordas de uma forma, que são uma mistura da cor do primeiro plano e da cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="95e5c-157">Anti-aliasing creates new colors, for pixels along the edges of a shape, that are a blend of the foreground color and the background color.</span></span> <span data-ttu-id="95e5c-158">Algumas dessas cores podem fazer com que os pixels sejam perdidos quando a cor do plano de fundo se torna transparente.</span><span class="sxs-lookup"><span data-stu-id="95e5c-158">Some of these in-between colors can cause pixels to be missed when the background color is made transparent.</span></span>

<span data-ttu-id="95e5c-159">Sua camada de plano de fundo de capa deve ser parecida com a ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="95e5c-159">Your skin background layer should look like the following illustration.</span></span>

![camada de capa em segundo plano](images/g01backg.png)

## <a name="play-and-close-button-layers"></a><span data-ttu-id="95e5c-161">Reproduzir e fechar camadas de botão</span><span class="sxs-lookup"><span data-stu-id="95e5c-161">Play and Close Button Layers</span></span>

<span data-ttu-id="95e5c-162">Crie uma nova camada e nomeie-a como "Fechar botão".</span><span class="sxs-lookup"><span data-stu-id="95e5c-162">Create a new layer and name it "Close button".</span></span> <span data-ttu-id="95e5c-163">Usando a ferramenta de seleção de letreiro Eliptical novamente, crie um círculo e posicione-o no lado esquerdo da imagem geral.</span><span class="sxs-lookup"><span data-stu-id="95e5c-163">Using the Eliptical Marquee selection tool again, create a circle and position it on the left side of the overall image.</span></span> <span data-ttu-id="95e5c-164">Ative a visibilidade do arquivo de contêiner de capa para ajudar a colocar a seleção.</span><span class="sxs-lookup"><span data-stu-id="95e5c-164">Turn on the visibility of the skin container file to help place the selection.</span></span>

<span data-ttu-id="95e5c-165">Quando estiver satisfeito com o posicionamento, preencha a seleção com qualquer cor (exceto a cor do contêiner da capa ou do plano de fundo da capa).</span><span class="sxs-lookup"><span data-stu-id="95e5c-165">When you are satisfied with the placement, fill the selection with any color (except the color of the skin container or the skin background).</span></span> <span data-ttu-id="95e5c-166">Neste exemplo, foi escolhida uma cor roxa.</span><span class="sxs-lookup"><span data-stu-id="95e5c-166">In this example, a purple color was chosen.</span></span> <span data-ttu-id="95e5c-167">Você não precisa se lembrar do número da cor.</span><span class="sxs-lookup"><span data-stu-id="95e5c-167">You do not need to remember the number of the color.</span></span> <span data-ttu-id="95e5c-168">Em seguida, cancele a seleção e aplique outro efeito de camada de chanfro e entalhe padrão.</span><span class="sxs-lookup"><span data-stu-id="95e5c-168">Then cancel the selection and apply another default Bevel and Emboss layer effect.</span></span> <span data-ttu-id="95e5c-169">Se você quiser aplicar efeitos de não camada ao botão, faça uma cópia do original para uso posterior no mapeamento.</span><span class="sxs-lookup"><span data-stu-id="95e5c-169">If you want to apply non-layer effects to your button, make a copy of the original for later use in mapping.</span></span>

<span data-ttu-id="95e5c-170">O botão fechar deve ser semelhante à ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="95e5c-170">Your Close button should look like the following illustration.</span></span>

![botão de fechamento](images/g01qbut.png)

<span data-ttu-id="95e5c-172">Crie uma nova camada e nomeie-a como "botão reproduzir".</span><span class="sxs-lookup"><span data-stu-id="95e5c-172">Create a new layer and name it "Play button".</span></span> <span data-ttu-id="95e5c-173">Use as mesmas técnicas que você fez para o botão fechar, mas dê a ela uma cor diferente.</span><span class="sxs-lookup"><span data-stu-id="95e5c-173">Use the same techniques you did for the Close button, but give it a different color.</span></span> <span data-ttu-id="95e5c-174">Nesse caso, uma cor de botão rosa foi escolhida, mas qualquer cor pode ser usada desde que ela não seja a mesma cor que o contêiner de capa (porque ela se misturaria no contêiner) ou a cor de fundo da capa (porque ela se tornaria transparente).</span><span class="sxs-lookup"><span data-stu-id="95e5c-174">In this case, a pink button color was chosen, but any color can be used as long as it is not the same color as the skin container (because it would blend into the container) or the skin background color (because it would become transparent).</span></span>

<span data-ttu-id="95e5c-175">O botão de reprodução deve ser semelhante à ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="95e5c-175">Your Play button should look like the following illustration.</span></span>

![botão reproduzir](images/g01pbut.png)

## <a name="combine-layers-and-save"></a><span data-ttu-id="95e5c-177">Combinar camadas e salvar</span><span class="sxs-lookup"><span data-stu-id="95e5c-177">Combine Layers and Save</span></span>

<span data-ttu-id="95e5c-178">Agora você está pronto para criar o arquivo de arte primário.</span><span class="sxs-lookup"><span data-stu-id="95e5c-178">You are now ready to create the primary art file.</span></span> <span data-ttu-id="95e5c-179">Oculte todas as camadas e, em seguida, mostre apenas as camadas a seguir, nesta ordem (de cima para baixo):</span><span class="sxs-lookup"><span data-stu-id="95e5c-179">Hide all layers and then show only the following layers, in this order (top to bottom):</span></span>

<span data-ttu-id="95e5c-180">Botão reproduzir</span><span class="sxs-lookup"><span data-stu-id="95e5c-180">Play button</span></span>

<span data-ttu-id="95e5c-181">Botão Fechar</span><span class="sxs-lookup"><span data-stu-id="95e5c-181">Close button</span></span>

<span data-ttu-id="95e5c-182">Contêiner de capa</span><span class="sxs-lookup"><span data-stu-id="95e5c-182">Skin container</span></span>

<span data-ttu-id="95e5c-183">Plano de fundo da capa</span><span class="sxs-lookup"><span data-stu-id="95e5c-183">Skin background</span></span>

<span data-ttu-id="95e5c-184">Salve em um novo arquivo usando o comando salvar uma cópia no menu arquivo.</span><span class="sxs-lookup"><span data-stu-id="95e5c-184">Save to a new file using the Save a Copy command from the File menu.</span></span> <span data-ttu-id="95e5c-185">Selecione a opção BMP na parte salvar como da caixa de diálogo salvar uma cópia e digite um nome de arquivo que você irá referenciar posteriormente no arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="95e5c-185">Select the BMP option in the Save As portion of the Save a Copy dialog box and type a file name that you will refer to later in your skin definition file.</span></span> <span data-ttu-id="95e5c-186">O ideal é que você salve isso no mesmo diretório que o arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="95e5c-186">Ideally you should save this in the same directory as your skin definition file.</span></span> <span data-ttu-id="95e5c-187">Por exemplo, você pode chamar essa background.bmp.</span><span class="sxs-lookup"><span data-stu-id="95e5c-187">For example, you could call this background.bmp.</span></span> <span data-ttu-id="95e5c-188">Escolha as configurações padrão e salve o arquivo.</span><span class="sxs-lookup"><span data-stu-id="95e5c-188">Choose the default settings and save the file.</span></span>

<span data-ttu-id="95e5c-189">O arquivo de arte principal deve ter a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="95e5c-189">Your primary art file should look like this:</span></span>

![arquivo de arte principal](images/g01prime.png)

<span data-ttu-id="95e5c-191">Você usará esse nome de arquivo como o valor para o atributo **backgroundImage** do elemento **View** em seu arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="95e5c-191">You will use this file name as the value for the **backgroundImage** attribute of the **VIEW** element in your skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95e5c-192">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="95e5c-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95e5c-193">**Criando sua primeira capa**</span><span class="sxs-lookup"><span data-stu-id="95e5c-193">**Building Your First Skin**</span></span>](building-your-first-skin.md)
</dt> </dl>

 

 




