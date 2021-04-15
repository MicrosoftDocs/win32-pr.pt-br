---
title: Elemento VIEW
description: Elemento VIEW
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Capas do Windows Media Player, elemento VIEW
- aparência, elemento VIEW
- Elemento VIEW
- referência para capas, elemento VIEW
- elementos, exibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e907cced22b4d1cd498054df06ac8677a7488b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364126"
---
# <a name="view-element"></a><span data-ttu-id="912db-108">Elemento VIEW</span><span class="sxs-lookup"><span data-stu-id="912db-108">VIEW Element</span></span>

<span data-ttu-id="912db-109">O elemento **View** contém os detalhes da interface do usuário de uma capa e usa os atributos, métodos e manipuladores de eventos mostrados nas tabelas a seguir.</span><span class="sxs-lookup"><span data-stu-id="912db-109">The **VIEW** element contains the user interface details of a skin, and uses the attributes, methods, and event handlers shown in the following tables.</span></span>

<span data-ttu-id="912db-110">Vários elementos **View** podem ser definidos como filhos do elemento **Theme** de uma capa para fornecer interfaces diferentes para situações diferentes.</span><span class="sxs-lookup"><span data-stu-id="912db-110">Multiple **VIEW** elements can be defined as children of the **THEME** element of a skin to provide different interfaces for different situations.</span></span> <span data-ttu-id="912db-111">Os elementos de **exibição** não podem ser especificados como filhos de qualquer outro elemento e contêm todos os outros elementos de capa.</span><span class="sxs-lookup"><span data-stu-id="912db-111">**VIEW** elements cannot be specified as children of any other element, and they contain all other skin elements.</span></span> <span data-ttu-id="912db-112">Observe que cada exibição tem seu próprio escopo de variável, o que significa que não é possível compartilhar valores de atributo com outras exibições.</span><span class="sxs-lookup"><span data-stu-id="912db-112">Note that each view has its own variable scope, which means it cannot share attribute values with other views.</span></span>

<span data-ttu-id="912db-113">O atributo global **View** pode ser usado para fazer referência a um elemento **View** específico de qualquer lugar dentro dele.</span><span class="sxs-lookup"><span data-stu-id="912db-113">The **view** global attribute can be used to reference a specific **VIEW** element from anywhere within it.</span></span> <span data-ttu-id="912db-114">Essa é uma alternativa ao uso de seu atributo de **ID** , que deve ser usado de dentro de outros elementos de **exibição** ou de dentro do elemento **Theme** .</span><span class="sxs-lookup"><span data-stu-id="912db-114">This is an alternative to using its **id** attribute, which must be used from within other **VIEW** elements or from within the **THEME** element.</span></span>

<span data-ttu-id="912db-115">O elemento **View** oferece suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="912db-115">The **VIEW** element supports the following attributes.</span></span> <span data-ttu-id="912db-116">Os atributos marcados com um asterisco ( \* ) também têm suporte no elemento **subview** .</span><span class="sxs-lookup"><span data-stu-id="912db-116">Attributes marked with an asterisk (\*) are also supported by the **SUBVIEW** element.</span></span>



| <span data-ttu-id="912db-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="912db-117">Attribute</span></span>                                                       | <span data-ttu-id="912db-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="912db-118">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="912db-119">[backgroundColor](view-backgroundcolor.md)\*</span><span class="sxs-lookup"><span data-stu-id="912db-119">[backgroundColor](view-backgroundcolor.md) \*</span></span>                  | <span data-ttu-id="912db-120">Especifica ou recupera a cor da tela de fundo da **exibição** ou da **subexibição**.</span><span class="sxs-lookup"><span data-stu-id="912db-120">Specifies or retrieves the background color of the **VIEW** or **SUBVIEW**.</span></span>                                             |
| <span data-ttu-id="912db-121">[backgroundImage](view-backgroundimage.md) \*</span><span class="sxs-lookup"><span data-stu-id="912db-121">[backgroundImage](view-backgroundimage.md) \*</span></span>                  | <span data-ttu-id="912db-122">Especifica ou recupera a imagem de plano de fundo da **exibição** ou da **subexibição**.</span><span class="sxs-lookup"><span data-stu-id="912db-122">Specifies or retrieves the background image of the **VIEW** or **SUBVIEW**.</span></span>                                             |
| [<span data-ttu-id="912db-123">backgroundImageHueShift</span><span class="sxs-lookup"><span data-stu-id="912db-123">backgroundImageHueShift</span></span>](view-backgroundimagehueshift.md)     | <span data-ttu-id="912db-124">Especifica ou recupera a quantidade pela qual o matiz da imagem de plano de fundo é deslocado.</span><span class="sxs-lookup"><span data-stu-id="912db-124">Specifies or retrieves the amount by which the hue of the background image is shifted.</span></span>                                  |
| [<span data-ttu-id="912db-125">backgroundImageSaturation</span><span class="sxs-lookup"><span data-stu-id="912db-125">backgroundImageSaturation</span></span>](view-backgroundimagesaturation.md) | <span data-ttu-id="912db-126">Especifica ou recupera o valor de saturação da imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="912db-126">Specifies or retrieves the saturation value of the background image.</span></span>                                                    |
| <span data-ttu-id="912db-127">[backgroundTiled](view-backgroundtiled.md)\*</span><span class="sxs-lookup"><span data-stu-id="912db-127">[backgroundTiled](view-backgroundtiled.md) \*</span></span>                  | <span data-ttu-id="912db-128">Especifica ou recupera um valor que indica se a imagem de plano de fundo do **modo de exibição** ou da **subexibição** é colocada em ladrilho.</span><span class="sxs-lookup"><span data-stu-id="912db-128">Specifies or retrieves a value indicating whether the background image of the **VIEW** or **SUBVIEW** is tiled.</span></span>         |
| [<span data-ttu-id="912db-129">category</span><span class="sxs-lookup"><span data-stu-id="912db-129">category</span></span>](view-category.md)                                   | <span data-ttu-id="912db-130">Especifica ou recupera a categoria para a qual a interface do usuário será exibida.</span><span class="sxs-lookup"><span data-stu-id="912db-130">Specifies or retrieves the category for which the user interface will appear.</span></span>                                           |
| [<span data-ttu-id="912db-131">focusObjectID</span><span class="sxs-lookup"><span data-stu-id="912db-131">focusObjectID</span></span>](view-focusobjectid.md)                         | <span data-ttu-id="912db-132">Especifica ou recupera um valor que indica qual elemento tem o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="912db-132">Specifies or retrieves a value indicating which element has keyboard focus.</span></span>                                             |
| [<span data-ttu-id="912db-133">maxHeight</span><span class="sxs-lookup"><span data-stu-id="912db-133">maxHeight</span></span>](view-maxheight.md)                                 | <span data-ttu-id="912db-134">Especifica ou recupera a altura máxima da **exibição** durante o redimensionamento.</span><span class="sxs-lookup"><span data-stu-id="912db-134">Specifies or retrieves the maximum height of the **VIEW** when resizing.</span></span>                                                |
| [<span data-ttu-id="912db-135">maxWidth</span><span class="sxs-lookup"><span data-stu-id="912db-135">maxWidth</span></span>](view-maxwidth.md)                                   | <span data-ttu-id="912db-136">Especifica ou recupera a largura máxima da **exibição** ao redimensionar.</span><span class="sxs-lookup"><span data-stu-id="912db-136">Specifies or retrieves the maximum width of the **VIEW** when resizing.</span></span>                                                 |
| [<span data-ttu-id="912db-137">minHeight</span><span class="sxs-lookup"><span data-stu-id="912db-137">minHeight</span></span>](view-minheight.md)                                 | <span data-ttu-id="912db-138">Especifica ou recupera a altura mínima da **exibição** ao redimensionar.</span><span class="sxs-lookup"><span data-stu-id="912db-138">Specifies or retrieves the minimum height of the **VIEW** when resizing.</span></span>                                                |
| [<span data-ttu-id="912db-139">minWidth</span><span class="sxs-lookup"><span data-stu-id="912db-139">minWidth</span></span>](view-minwidth.md)                                   | <span data-ttu-id="912db-140">Especifica ou recupera a largura mínima da **exibição** ao redimensionar.</span><span class="sxs-lookup"><span data-stu-id="912db-140">Specifies or retrieves the minimum width of the **VIEW** when resizing.</span></span>                                                 |
| [<span data-ttu-id="912db-141">redimensionável</span><span class="sxs-lookup"><span data-stu-id="912db-141">resizable</span></span>](view-resizable.md)                                 | <span data-ttu-id="912db-142">Especifica ou recupera um valor que indica se a **exibição** pode ser redimensionada.</span><span class="sxs-lookup"><span data-stu-id="912db-142">Specifies or retrieves a value indicating whether the **VIEW** can be resized.</span></span>                                          |
| [<span data-ttu-id="912db-143">resizeBackgroundImage</span><span class="sxs-lookup"><span data-stu-id="912db-143">resizeBackgroundImage</span></span>](view-resizebackgroundimage.md)         | <span data-ttu-id="912db-144">Especifica ou recupera um valor que indica se a imagem de plano de fundo pode ser redimensionada.</span><span class="sxs-lookup"><span data-stu-id="912db-144">Specifies or retrieves a value indicating whether the background image can be resized.</span></span>                                  |
| [<span data-ttu-id="912db-145">scriptFile</span><span class="sxs-lookup"><span data-stu-id="912db-145">scriptFile</span></span>](view-scriptfile.md)                               | <span data-ttu-id="912db-146">Especifica os nomes de arquivo do que acompanham arquivos JScript.</span><span class="sxs-lookup"><span data-stu-id="912db-146">Specifies the file names of accompanying JScript files.</span></span>                                                                 |
| [<span data-ttu-id="912db-147">IntervaloDoCronômetro</span><span class="sxs-lookup"><span data-stu-id="912db-147">timerInterval</span></span>](view-timerinterval.md)                         | <span data-ttu-id="912db-148">Especifica ou recupera o intervalo, em milissegundos, no qual o temporizador dispara eventos para o manipulador de eventos **OnTimer** .</span><span class="sxs-lookup"><span data-stu-id="912db-148">Specifies or retrieves the interval, in milliseconds, at which the timer fires events to the **ontimer** event handler.</span></span> |
| [<span data-ttu-id="912db-149">title</span><span class="sxs-lookup"><span data-stu-id="912db-149">title</span></span>](view-title.md)                                         | <span data-ttu-id="912db-150">Especifica ou recupera o título da **exibição**.</span><span class="sxs-lookup"><span data-stu-id="912db-150">Specifies or retrieves the title of the **VIEW**.</span></span> <span data-ttu-id="912db-151">Só pode ser definido em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="912db-151">Can only be set at design time.</span></span>                                       |
| [<span data-ttu-id="912db-152">titleBar</span><span class="sxs-lookup"><span data-stu-id="912db-152">titleBar</span></span>](view-titlebar.md)                                   | <span data-ttu-id="912db-153">Especifica ou recupera um valor que indica se a barra de título da janela é mostrada.</span><span class="sxs-lookup"><span data-stu-id="912db-153">Specifies or retrieves a value indicating whether the window title bar is shown.</span></span>                                        |
| <span data-ttu-id="912db-154">[transparencyColor](view-transparencycolor.md)\*</span><span class="sxs-lookup"><span data-stu-id="912db-154">[transparencyColor](view-transparencycolor.md) \*</span></span>              | <span data-ttu-id="912db-155">Especifica ou recupera a cor de transparência da imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="912db-155">Specifies or retrieves the transparency color of the background image.</span></span>                                                  |



 

<span data-ttu-id="912db-156">O elemento **View** oferece suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="912db-156">The **VIEW** element supports the following methods.</span></span>



| <span data-ttu-id="912db-157">Método</span><span class="sxs-lookup"><span data-stu-id="912db-157">Method</span></span>                                              | <span data-ttu-id="912db-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="912db-158">Description</span></span>                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="912db-159">close</span><span class="sxs-lookup"><span data-stu-id="912db-159">close</span></span>](view-close.md)                             | <span data-ttu-id="912db-160">Fecha a **exibição**.</span><span class="sxs-lookup"><span data-stu-id="912db-160">Closes the **VIEW**.</span></span>                                       |
| [<span data-ttu-id="912db-161">tirar</span><span class="sxs-lookup"><span data-stu-id="912db-161">maximize</span></span>](view-maximize.md)                       | <span data-ttu-id="912db-162">Maximiza a **exibição**.</span><span class="sxs-lookup"><span data-stu-id="912db-162">Maximizes the **VIEW**.</span></span>                                    |
| [<span data-ttu-id="912db-163">maximiza</span><span class="sxs-lookup"><span data-stu-id="912db-163">minimize</span></span>](view-minimize.md)                       | <span data-ttu-id="912db-164">Minimiza a **exibição**.</span><span class="sxs-lookup"><span data-stu-id="912db-164">Minimizes the **VIEW**.</span></span>                                    |
| [<span data-ttu-id="912db-165">restore</span><span class="sxs-lookup"><span data-stu-id="912db-165">restore</span></span>](view-restore.md)                         | <span data-ttu-id="912db-166">Restaura a **exibição**.</span><span class="sxs-lookup"><span data-stu-id="912db-166">Restores the **VIEW**.</span></span>                                     |
| [<span data-ttu-id="912db-167">returnToMediaCenter</span><span class="sxs-lookup"><span data-stu-id="912db-167">returnToMediaCenter</span></span>](view-returntomediacenter.md) | <span data-ttu-id="912db-168">Retorna o usuário para o modo completo do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="912db-168">Returns the user to the full mode of Windows Media Player.</span></span> |
| [<span data-ttu-id="912db-169">size</span><span class="sxs-lookup"><span data-stu-id="912db-169">size</span></span>](view-size.md)                               | <span data-ttu-id="912db-170">Redimensiona a **exibição** em uma borda especificada.</span><span class="sxs-lookup"><span data-stu-id="912db-170">Resizes the **VIEW** on a specified edge.</span></span>                  |



 

<span data-ttu-id="912db-171">O elemento **View** pode implementar os manipuladores de eventos a seguir.</span><span class="sxs-lookup"><span data-stu-id="912db-171">The **VIEW** element can implement the following event handlers.</span></span>



| <span data-ttu-id="912db-172">Manipulador de eventos</span><span class="sxs-lookup"><span data-stu-id="912db-172">Event handler</span></span>               | <span data-ttu-id="912db-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="912db-173">Description</span></span>                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="912db-174">fechamento</span><span class="sxs-lookup"><span data-stu-id="912db-174">onclose</span></span>](view-onclose.md) | <span data-ttu-id="912db-175">Manipula um evento que ocorre quando a **exibição** está prestes a ser fechada.</span><span class="sxs-lookup"><span data-stu-id="912db-175">Handles an event that occurs when the **VIEW** is about to be closed.</span></span>      |
| [<span data-ttu-id="912db-176">OnError</span><span class="sxs-lookup"><span data-stu-id="912db-176">onerror</span></span>](view-onerror.md) | <span data-ttu-id="912db-177">Manipulará um evento de erro se **Settings. enableErrorDialogs** for definido como false.</span><span class="sxs-lookup"><span data-stu-id="912db-177">Handles an error event if **Settings.enableErrorDialogs** is set to false.</span></span> |
| [<span data-ttu-id="912db-178">carregamento</span><span class="sxs-lookup"><span data-stu-id="912db-178">onload</span></span>](view-onload.md)   | <span data-ttu-id="912db-179">Manipula um evento que ocorre quando a **exibição** é exibida pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="912db-179">Handles an event that occurs when the **VIEW** is first displayed.</span></span>         |
| [<span data-ttu-id="912db-180">OnTimer</span><span class="sxs-lookup"><span data-stu-id="912db-180">ontimer</span></span>](view-ontimer.md) | <span data-ttu-id="912db-181">Manipula eventos de temporizador.</span><span class="sxs-lookup"><span data-stu-id="912db-181">Handles timer events.</span></span>                                                      |



 

<span data-ttu-id="912db-182">O elemento **View** oferece suporte aos atributos de ambiente e pode implementar os manipuladores de eventos de ambiente, exceto quando indicado.</span><span class="sxs-lookup"><span data-stu-id="912db-182">The **VIEW** element supports the ambient attributes and can implement the ambient event handlers, except where noted.</span></span> <span data-ttu-id="912db-183">Para obter mais informações, consulte [atributos de ambiente](ambient-attributes.md) e [manipuladores de eventos de ambiente](ambient-event-handlers.md),</span><span class="sxs-lookup"><span data-stu-id="912db-183">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md),</span></span>

## <a name="related-topics"></a><span data-ttu-id="912db-184">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="912db-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="912db-185">**Referência de programação de capa**</span><span class="sxs-lookup"><span data-stu-id="912db-185">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




