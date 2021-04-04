---
title: Estrutura do arquivo de definição de capa
description: Estrutura do arquivo de definição de capa
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Capas do Windows Media Player, arquivos de definição de capa
- capas, arquivos de definição de capa
- arquivos para capas, definição de capa
- arquivos de definição de capa, estrutura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64226fb918bcbf93c95ece52075e2c8e7ed13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005785"
---
# <a name="skin-definition-file-structure"></a><span data-ttu-id="6fc2b-107">Estrutura do arquivo de definição de capa</span><span class="sxs-lookup"><span data-stu-id="6fc2b-107">Skin Definition File Structure</span></span>

<span data-ttu-id="6fc2b-108">O arquivo de definição de capa deve seguir uma estrutura específica.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-108">The skin definition file must follow a specific structure.</span></span> <span data-ttu-id="6fc2b-109">Você começa com um elemento **Theme** , cria um ou mais elementos **View** e, em seguida, define cada elemento **View** com os elementos da interface do usuário apropriados para o tipo de exibição que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-109">You start with a **THEME** element, create one or more **VIEW** elements, and then define each **VIEW** element with the user interface elements appropriate for the type of view you want to use.</span></span>

## <a name="theme-elements"></a><span data-ttu-id="6fc2b-110">Elementos de tema</span><span class="sxs-lookup"><span data-stu-id="6fc2b-110">THEME Elements</span></span>

<span data-ttu-id="6fc2b-111">No nível superior, você deve iniciar o arquivo de definição de capa com o elemento **Theme** e fechá-lo.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-111">At the top level, you must start the skin definition file with the **THEME** element and close with it.</span></span>


```C++
<THEME>
    ...
</THEME>

```



<span data-ttu-id="6fc2b-112">O elemento **Theme** é o elemento raiz da sua capa.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-112">The **THEME** element is the root element for your skin.</span></span> <span data-ttu-id="6fc2b-113">Pode haver apenas um elemento **Theme** em um arquivo de definição de capa e deve estar no nível superior.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-113">There can be only one **THEME** element in a skin definition file, and it must be at the top level.</span></span> <span data-ttu-id="6fc2b-114">Os elementos de **tema** têm atributos específicos e de ambiente, embora a maioria das vezes não seja necessário usá-los.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-114">**THEME** elements have specific and ambient attributes, though most of the time you will not need to use them.</span></span> <span data-ttu-id="6fc2b-115">Para obter mais informações sobre esses atributos, consulte a [referência de programação de capa](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="6fc2b-115">For more information about these attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="view-elements"></a><span data-ttu-id="6fc2b-116">EXIBIR elementos</span><span class="sxs-lookup"><span data-stu-id="6fc2b-116">VIEW Elements</span></span>

<span data-ttu-id="6fc2b-117">Cada **tema** deve ter pelo menos um elemento de **exibição** .</span><span class="sxs-lookup"><span data-stu-id="6fc2b-117">Each **THEME** must have at least one **VIEW** element.</span></span> <span data-ttu-id="6fc2b-118">O elemento **View** governa a imagem específica que você vê na tela.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-118">The **VIEW** element governs the particular image you see on the screen.</span></span> <span data-ttu-id="6fc2b-119">Talvez você queira ter mais de uma exibição, para que você possa alternar para frente e para trás.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-119">You may want to have more than one view, so you can switch back and forth.</span></span> <span data-ttu-id="6fc2b-120">Por exemplo, talvez você queira ter uma exibição grande para trabalhar com listas de reprodução, uma exibição média para assistir a visualizações e uma pequena exibição que se encaixa em um canto da tela.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-120">For example, you might want to have a large view for working with playlists, a medium view for watching visualizations, and a tiny view that fits in a corner of the screen.</span></span>

<span data-ttu-id="6fc2b-121">Se você estiver criando várias exibições, convém garantir que cada exibição tenha um valor de atributo de **ID** exclusivo que será usado para identificar a exibição.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-121">If you are creating multiple views, you will want to make sure that each view has a unique **ID** attribute value that will be used to identify the view.</span></span> <span data-ttu-id="6fc2b-122">Você deve definir o atributo **backgroundImage** ou sua exibição não terá nenhuma imagem inicial.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-122">You must define the **backgroundImage** attribute or your view will have no starting image.</span></span> <span data-ttu-id="6fc2b-123">Se você não quiser exibir uma imagem retangular, provavelmente desejará usar o atributo **clippingColor** para definir as áreas da sua capa que não serão exibidas e provavelmente desejará definir o atributo **TitleBar** do elemento **View** .</span><span class="sxs-lookup"><span data-stu-id="6fc2b-123">If you do not want to display a rectangular image, you will probably want to use the **clippingColor** attribute to define the areas of your skin that will not display, and you will probably want to set the **titleBar** attribute of the **VIEW** element.</span></span>

<span data-ttu-id="6fc2b-124">Cada elemento **View** também pode ter um ou mais elementos **subview** .</span><span class="sxs-lookup"><span data-stu-id="6fc2b-124">Each **VIEW** element can also have one or more **SUBVIEW** elements.</span></span> <span data-ttu-id="6fc2b-125">Um elemento de **subexibição** é semelhante a uma **exibição** e pode ser usado para partes da sua capa que você deseja mover, ocultar ou mostrar.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-125">A **SUBVIEW** element is similar to a **VIEW** and can be used for parts of your skin that you want to move around, hide, or show.</span></span> <span data-ttu-id="6fc2b-126">Por exemplo, um elemento de **subexibição** pode ser usado para criar uma bandeja deslizante que se desprenda da sua capa para exibir um equalizador gráfico.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-126">For example, a **SUBVIEW** element might be used to create a sliding tray that pops out of your skin to display a graphic equalizer.</span></span> <span data-ttu-id="6fc2b-127">Os elementos de **subexibição** podem ser alinhados com a **exibição** e ter outras relações especiais com a **exibição**.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-127">**SUBVIEW** elements can be aligned with the **VIEW** and have other special relationships to the **VIEW**.</span></span>

## <a name="initializing-windows-media-player"></a><span data-ttu-id="6fc2b-128">Inicializando o Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="6fc2b-128">Initializing Windows Media Player</span></span>

<span data-ttu-id="6fc2b-129">Você pode definir determinadas propriedades iniciais do Windows Media Player usando os elementos **Player**, **configurações** e **controles** .</span><span class="sxs-lookup"><span data-stu-id="6fc2b-129">You can set certain initial properties of Windows Media Player by using the **PLAYER**, **SETTINGS**, and **CONTROLS** elements.</span></span> <span data-ttu-id="6fc2b-130">Por exemplo, você pode definir o volume para um nível inicial ou dar um valor padrão para um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-130">For example, you could set the volume to an initial level or give a default value for a file name.</span></span>

<span data-ttu-id="6fc2b-131">O código a seguir mostra como definir o valor da **URL** em uma capa:</span><span class="sxs-lookup"><span data-stu-id="6fc2b-131">The following code shows how to set the **URL** value in a skin:</span></span>


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



<span data-ttu-id="6fc2b-132">Se você quisesse definir o atributo **AutoStart** de **configurações** como false, usaria o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="6fc2b-132">If you wanted to set the **autoStart** attribute of **SETTINGS** to False, you would use the following code:</span></span>


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



<span data-ttu-id="6fc2b-133">Observe que o elemento **Settings** está aninhado dentro do elemento **Player** .</span><span class="sxs-lookup"><span data-stu-id="6fc2b-133">Note that the **SETTINGS** element is nested inside the **PLAYER** element.</span></span>

<span data-ttu-id="6fc2b-134">Usando esses elementos, os seguintes atributos e eventos podem ser especificados em tempo de design:</span><span class="sxs-lookup"><span data-stu-id="6fc2b-134">Using these elements, the following attributes and events can be specified at design time:</span></span>

<span data-ttu-id="6fc2b-135">**Atributos do elemento PLAYER**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-135">**PLAYER Element Attributes**</span></span>

-   <span data-ttu-id="6fc2b-136">**url**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-136">**url**</span></span>
-   <span data-ttu-id="6fc2b-137">**de resposta**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-137">**Buffering**</span></span>
-   <span data-ttu-id="6fc2b-138">**Currentitemchange**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-138">**Currentitemchange**</span></span>
-   <span data-ttu-id="6fc2b-139">**Currentplaylistchange**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-139">**Currentplaylistchange**</span></span>
-   <span data-ttu-id="6fc2b-140">**Erro**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-140">**Error**</span></span>
-   <span data-ttu-id="6fc2b-141">**Markerhit**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-141">**Markerhit**</span></span>
-   <span data-ttu-id="6fc2b-142">**Mediachange**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-142">**Mediachange**</span></span>
-   <span data-ttu-id="6fc2b-143">**Mediacollectionchange**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-143">**Mediacollectionchange**</span></span>
-   <span data-ttu-id="6fc2b-144">**Modechange**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-144">**Modechange**</span></span>
-   <span data-ttu-id="6fc2b-145">**Mpenstatechange**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-145">**Mpenstatechange**</span></span>
-   <span data-ttu-id="6fc2b-146">**Mlaylistchange**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-146">**Mlaylistchange**</span></span>
-   <span data-ttu-id="6fc2b-147">**Mlaystatechange**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-147">**Mlaystatechange**</span></span>
-   <span data-ttu-id="6fc2b-148">**Mositionchange**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-148">**Mositionchange**</span></span>
-   <span data-ttu-id="6fc2b-149">**Mcriptcommand**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-149">**Mcriptcommand**</span></span>
-   <span data-ttu-id="6fc2b-150">**Mtatuschange**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-150">**Mtatuschange**</span></span>

<span data-ttu-id="6fc2b-151">**Atributos do elemento SETTINGS**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-151">**SETTINGS Element Attributes**</span></span>

-   <span data-ttu-id="6fc2b-152">**Inicialização automática**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-152">**autoStart**</span></span>
-   <span data-ttu-id="6fc2b-153">**Lance**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-153">**balance**</span></span>
-   <span data-ttu-id="6fc2b-154">**baseURL**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-154">**baseURL**</span></span>
-   <span data-ttu-id="6fc2b-155">**DefaultFrame**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-155">**defaultFrame**</span></span>
-   <span data-ttu-id="6fc2b-156">**enableErrorDialogs**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-156">**enableErrorDialogs**</span></span>
-   <span data-ttu-id="6fc2b-157">**invokeURLs**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-157">**invokeURLs**</span></span>
-   <span data-ttu-id="6fc2b-158">**Muta**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-158">**mute**</span></span>
-   <span data-ttu-id="6fc2b-159">**playCount**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-159">**playCount**</span></span>
-   <span data-ttu-id="6fc2b-160">**frequência**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-160">**rate**</span></span>
-   <span data-ttu-id="6fc2b-161">**volume**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-161">**volume**</span></span>

## <a name="controls-element-attributes"></a><span data-ttu-id="6fc2b-162">Atributos do elemento CONTROLS</span><span class="sxs-lookup"><span data-stu-id="6fc2b-162">CONTROLS Element Attributes</span></span>

-   <span data-ttu-id="6fc2b-163">**currentMarker**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-163">**currentMarker**</span></span>
-   <span data-ttu-id="6fc2b-164">**currentPosition**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-164">**currentPosition**</span></span>

## <a name="other-user-interface-elements"></a><span data-ttu-id="6fc2b-165">Outros elementos da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="6fc2b-165">Other User Interface Elements</span></span>

<span data-ttu-id="6fc2b-166">Depois de definir seus elementos **Theme** e **View** , você deve preencher sua **exibição** com elementos específicos da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-166">Once you have defined your **THEME** and **VIEW** elements, you must populate your **VIEW** with specific user interface elements.</span></span> <span data-ttu-id="6fc2b-167">Você não precisa usar todos os elementos disponíveis em uma capa, apenas aqueles que você precisa.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-167">You do not have to use all the available elements in a skin, just the ones you need.</span></span>

<span data-ttu-id="6fc2b-168">Se um elemento puder ser visto pelo usuário, ele será chamado de controle.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-168">If an element can be seen by the user, it is called a control.</span></span> <span data-ttu-id="6fc2b-169">Os seguintes controles estão disponíveis para capas:</span><span class="sxs-lookup"><span data-stu-id="6fc2b-169">The following controls are available for skins:</span></span>

-   <span data-ttu-id="6fc2b-170">Botões</span><span class="sxs-lookup"><span data-stu-id="6fc2b-170">Buttons</span></span>
-   <span data-ttu-id="6fc2b-171">Controles deslizantes, controles deslizantes personalizados e barras de progresso</span><span class="sxs-lookup"><span data-stu-id="6fc2b-171">Sliders, custom sliders, and progress bars</span></span>
-   <span data-ttu-id="6fc2b-172">Caixas de texto</span><span class="sxs-lookup"><span data-stu-id="6fc2b-172">Text boxes</span></span>
-   <span data-ttu-id="6fc2b-173">Janelas de vídeo</span><span class="sxs-lookup"><span data-stu-id="6fc2b-173">Video windows</span></span>
-   <span data-ttu-id="6fc2b-174">Janelas de visualização</span><span class="sxs-lookup"><span data-stu-id="6fc2b-174">Visualization windows</span></span>
-   <span data-ttu-id="6fc2b-175">Janelas de lista de reprodução</span><span class="sxs-lookup"><span data-stu-id="6fc2b-175">Playlist windows</span></span>
-   <span data-ttu-id="6fc2b-176">Janelas de subexibição</span><span class="sxs-lookup"><span data-stu-id="6fc2b-176">Subview windows</span></span>

<span data-ttu-id="6fc2b-177">Além disso, vários elementos podem ser usados para definir ainda mais as ações do Windows Media Player, mas exigem elementos visuais, como botões ou controles deslizantes:</span><span class="sxs-lookup"><span data-stu-id="6fc2b-177">In addition, several elements can be used to further define Windows Media Player actions, but they require visual elements such as buttons or sliders:</span></span>

-   <span data-ttu-id="6fc2b-178">Configurações de vídeo</span><span class="sxs-lookup"><span data-stu-id="6fc2b-178">Video settings</span></span>
-   <span data-ttu-id="6fc2b-179">Configurações do equalizador</span><span class="sxs-lookup"><span data-stu-id="6fc2b-179">Equalizer Settings</span></span>
-   <span data-ttu-id="6fc2b-180">Configurações de visualização</span><span class="sxs-lookup"><span data-stu-id="6fc2b-180">Visualization settings</span></span>

## <a name="buttons"></a><span data-ttu-id="6fc2b-181">Botões</span><span class="sxs-lookup"><span data-stu-id="6fc2b-181">Buttons</span></span>

<span data-ttu-id="6fc2b-182">Os botões são a parte mais popular de uma capa.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-182">Buttons are the most popular part of a skin.</span></span> <span data-ttu-id="6fc2b-183">Você pode usar botões para disparar ações como reproduzir, parar, encerrar, minimizar e alternar para modo de exibição diferente.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-183">You can use buttons to trigger actions such as play, stop, quit, minimize, and switch to different view.</span></span> <span data-ttu-id="6fc2b-184">O Windows Media Player fornece o criador da capa com dois tipos de elementos Button: o elemento **Button** e o elemento **Button** .</span><span class="sxs-lookup"><span data-stu-id="6fc2b-184">Windows Media Player provides the skin creator with two types of button elements: the **BUTTON** element and the **BUTTONGROUP** element.</span></span> <span data-ttu-id="6fc2b-185">Além disso, há vários tipos predefinidos de botões.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-185">In addition, there are several predefined types of buttons.</span></span>

-   <span data-ttu-id="6fc2b-186">**Elemento BUTTON.**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-186">**BUTTON element.**</span></span> <span data-ttu-id="6fc2b-187">O elemento **Button** é usado para botões individuais.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-187">The **BUTTON** element is used for individual buttons.</span></span> <span data-ttu-id="6fc2b-188">Se você usar o elemento **Button** , deverá fornecer uma imagem para cada botão e definir o local exato onde você deseja que o botão apareça em relação à imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-188">If you use the **BUTTON** element, you must supply an image for each button and define the exact location where you want the button to appear relative to the background image.</span></span> <span data-ttu-id="6fc2b-189">Uma das vantagens do elemento **Button** é que você pode alterar a imagem do botão dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-189">One of the advantages of the **BUTTON** element is that you can change the button image dynamically.</span></span>
-   <span data-ttu-id="6fc2b-190">**Elemento de botão.**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-190">**BUTTONGROUP element.**</span></span> <span data-ttu-id="6fc2b-191">O elemento do grupo **de botões é** usado para grupos de botões.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-191">The **BUTTONGROUP** element is used for groups of buttons.</span></span> <span data-ttu-id="6fc2b-192">Na verdade, você deve colocar cada elemento de um dos **botões** com um par de marcas de **botão** .</span><span class="sxs-lookup"><span data-stu-id="6fc2b-192">In fact, you must enclose each **BUTTONGROUP** element with a pair of **BUTTONGROUP** tags.</span></span> <span data-ttu-id="6fc2b-193">O uso de grupos de botões é mais fácil do que usar botões individuais, pois você não precisa especificar o local exato para cada botão.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-193">Using button groups is easier than using individual buttons because you do not have to specify the exact location for each button.</span></span> <span data-ttu-id="6fc2b-194">Em vez disso, você fornece um mapa de imagem separado que define as ações que ocorrerão quando o mouse passar sobre ou clicar em uma área em seu plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-194">Instead, you supply a separate image map that defines the actions that will take place when the mouse hovers over or clicks an area on your background.</span></span> <span data-ttu-id="6fc2b-195">Usar mapas de imagem é fácil porque você pode pegar a arte criada para seu plano de fundo e copiá-la para uma camada de mapeamento em seu programa de edição de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-195">Using image maps is easy because you can take the art you created for your background and copy it to a mapping layer in your graphics editing program.</span></span> <span data-ttu-id="6fc2b-196">Usar o programa de edição de elementos gráficos é mais rápido e preciso do que tentar definir exatamente onde um botão individual deve ser colocado em seu plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-196">Using your graphics editing program is faster and more precise than trying to define exactly where an individual button should be placed on your background.</span></span>
-   <span data-ttu-id="6fc2b-197">**Botões predefinidos.**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-197">**Predefined buttons.**</span></span> <span data-ttu-id="6fc2b-198">Há vários botões predefinidos.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-198">There are several predefined buttons.</span></span> <span data-ttu-id="6fc2b-199">Por exemplo, você pode usar um botão PLAYelement para reproduzir arquivos de mídia digital e um STOPelement para parar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-199">For example, you can use a PLAYELEMENT button to play digital media files, and a STOPELEMENT to stop playback.</span></span> <span data-ttu-id="6fc2b-200">Consulte [elemento de botão](buttongroup-element.md) e [elemento Button](button-element.md) na referência de programação de capa.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-200">See [BUTTONGROUP](buttongroup-element.md) Element and [BUTTON Element](button-element.md) in the Skin Programming Reference.</span></span> <span data-ttu-id="6fc2b-201">O [IMAGEBUTTON](imagebutton.md) pode ser usado para exibir imagens que podem ser alteradas em resposta a eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-201">The [IMAGEBUTTON](imagebutton.md) can be used to display images that can change in response to specific events.</span></span>

## <a name="sliders"></a><span data-ttu-id="6fc2b-202">Controles deslizantes</span><span class="sxs-lookup"><span data-stu-id="6fc2b-202">Sliders</span></span>

<span data-ttu-id="6fc2b-203">Os controles deslizantes são úteis para trabalhar com informações que mudam ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-203">Sliders are useful for working with information that changes over time.</span></span> <span data-ttu-id="6fc2b-204">Por exemplo, você pode usar um controle deslizante para indicar a quantidade de músicas que já foram reproduzidas para um arquivo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-204">For example, you might use a slider to indicate the amount of music that has already played for a particular media file.</span></span> <span data-ttu-id="6fc2b-205">Os controles deslizantes podem ser horizontais, verticais, lineares ou circulares ou qualquer forma que você possa imaginar.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-205">Sliders can be horizontal or vertical, linear or circular, or any shape you can think of.</span></span> <span data-ttu-id="6fc2b-206">Os controles deslizantes são fornecidos em três variedades: controles deslizantes, barras de progresso e controles deslizantes personalizados.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-206">Sliders come in three varieties: sliders, progress bars, and custom sliders.</span></span>

-   <span data-ttu-id="6fc2b-207">**Controles deslizantes.**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-207">**Sliders.**</span></span> <span data-ttu-id="6fc2b-208">Você pode usar o elemento **Slider** para controles de volume ou para permitir que o usuário se mova para uma parte diferente do conteúdo de mídia.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-208">You can use the **SLIDER** element for volume controls or to allow the user to move to a different part of the media content.</span></span>
-   <span data-ttu-id="6fc2b-209">**Barras de progresso.**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-209">**Progress bars.**</span></span> <span data-ttu-id="6fc2b-210">As barras de progresso são semelhantes aos controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-210">Progress bars are similar to sliders.</span></span> <span data-ttu-id="6fc2b-211">As barras de progresso são projetadas para exibir graficamente a porcentagem de um processo específico que foi concluído, mas não para um processo com o qual o usuário desejará interagir.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-211">Progress bars are designed for graphically displaying the percentage of a particular process that has been completed, but not for a process that the user will want to interact with.</span></span> <span data-ttu-id="6fc2b-212">Por exemplo, talvez você queira usar uma barra de progresso para indicar o progresso do buffer.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-212">For example, you might want to use a progress bar to indicate buffering progress.</span></span>
-   <span data-ttu-id="6fc2b-213">**Controles deslizantes personalizados.**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-213">**Custom sliders.**</span></span> <span data-ttu-id="6fc2b-214">A funcionalidade de controle deslizante personalizado é fornecida para que você possa criar controles como botões ou criar mecanismos de controle incomuns.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-214">Custom slider functionality is provided so you can create controls such as knobs, or make unusual control mechanisms.</span></span> <span data-ttu-id="6fc2b-215">Por exemplo, se você quiser criar um controle de volume que encapsula em sua capa, poderá fazê-lo com um controle deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-215">For example, if you want to create a volume control that wraps around your skin, you can do it with a custom slider.</span></span> <span data-ttu-id="6fc2b-216">Para configurar o controle deslizante personalizado, você deve criar um mapa de imagem que contenha imagens em escala de cinza para definir os locais dos valores no controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-216">To set up the custom slider, you must create an image map that contains grayscale images to define the locations of the values on the slider.</span></span> <span data-ttu-id="6fc2b-217">Isso é relativamente fácil de fazer com um programa de edição de gráficos que dá suporte a camadas.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-217">This is relatively easy to do with a graphics editing program that supports layers.</span></span>

## <a name="text"></a><span data-ttu-id="6fc2b-218">Texto</span><span class="sxs-lookup"><span data-stu-id="6fc2b-218">Text</span></span>

<span data-ttu-id="6fc2b-219">Você pode usar o elemento de **texto** para exibir o texto em sua capa, como títulos de música.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-219">You can use the **TEXT** element to display text on your skin, such as song titles.</span></span>

## <a name="video"></a><span data-ttu-id="6fc2b-220">Vídeo</span><span class="sxs-lookup"><span data-stu-id="6fc2b-220">Video</span></span>

<span data-ttu-id="6fc2b-221">Você pode exibir o vídeo em sua capa.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-221">You can display video in your skin.</span></span> <span data-ttu-id="6fc2b-222">O elemento **Video** permite que você defina o tamanho e a posição da janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-222">The **VIDEO** element allows you to set the size and position of the video window.</span></span>

<span data-ttu-id="6fc2b-223">Você também pode permitir que o usuário altere as configurações de vídeo com o elemento **VIDEOSETTINGS** .</span><span class="sxs-lookup"><span data-stu-id="6fc2b-223">You can also allow the user to change the video settings with the **VIDEOSETTINGS** element.</span></span> <span data-ttu-id="6fc2b-224">Por exemplo, você pode criar controles para ajustar o brilho do vídeo.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-224">For example, you can create controls to adjust the brightness of the video.</span></span>

<span data-ttu-id="6fc2b-225">Se você não fornecer um elemento de vídeo e o conteúdo contiver vídeo, o Windows Media Player retornará ao modo completo e sua capa não será exibida.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-225">If you do not supply a video element and the content contains video, Windows Media Player will return to full mode and your skin will not be displayed.</span></span>

## <a name="equalizer-settings"></a><span data-ttu-id="6fc2b-226">Configurações do equalizador</span><span class="sxs-lookup"><span data-stu-id="6fc2b-226">Equalizer Settings</span></span>

<span data-ttu-id="6fc2b-227">Você pode definir a filtragem para faixas de frequência de áudio específicas usando o elemento **EQUALIZERSETTINGS** .</span><span class="sxs-lookup"><span data-stu-id="6fc2b-227">You can set the filtering for specific audio frequency bands by using the **EQUALIZERSETTINGS** element.</span></span> <span data-ttu-id="6fc2b-228">Você pode aumentar os graves, ajustar os agudos e configurar seus sons para que correspondam aos ouvidos ou à sala de vida.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-228">You can boost the bass, tweak the treble, and set up your sounds to match your ears or your living room.</span></span>

## <a name="visualizations"></a><span data-ttu-id="6fc2b-229">Visualizações</span><span class="sxs-lookup"><span data-stu-id="6fc2b-229">Visualizations</span></span>

<span data-ttu-id="6fc2b-230">Você pode exibir visualizações em sua capa.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-230">You can display visualizations in your skin.</span></span> <span data-ttu-id="6fc2b-231">As visualizações são efeitos visuais que mudam com o passar do tempo conforme o áudio é executado pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-231">Visualizations are visual effects that change over time as audio is playing through Windows Media Player.</span></span> <span data-ttu-id="6fc2b-232">O elemento **Effects** determina onde as visualizações serão reproduzidas, qual será o tamanho da janela e quais visualizações serão reproduzidas.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-232">The **EFFECTS** element determines where the visualizations will play, what size the window will be, and which visualizations will be played.</span></span>

## <a name="playlists"></a><span data-ttu-id="6fc2b-233">Playlists</span><span class="sxs-lookup"><span data-stu-id="6fc2b-233">Playlists</span></span>

<span data-ttu-id="6fc2b-234">Você pode usar o elemento **playlist** para permitir que o usuário selecione um item de uma lista de reprodução específica.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-234">You can use the **PLAYLIST** element to let the user select an item from a specific playlist.</span></span>

## <a name="subviews"></a><span data-ttu-id="6fc2b-235">Subexibições</span><span class="sxs-lookup"><span data-stu-id="6fc2b-235">Subviews</span></span>

<span data-ttu-id="6fc2b-236">Você pode usar o elemento **subview** para exibir conjuntos secundários de controles de interface, como uma playlist ou controles de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6fc2b-236">You can use the **SUBVIEW** element to display secondary sets of interface controls, such as a playlist or video controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fc2b-237">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6fc2b-237">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fc2b-238">**Arquivos de capa**</span><span class="sxs-lookup"><span data-stu-id="6fc2b-238">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




