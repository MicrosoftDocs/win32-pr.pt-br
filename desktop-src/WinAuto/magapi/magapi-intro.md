---
title: Visão geral da API de ampliação
description: Este tópico descreve a API de ampliação e explica como usá-la em um aplicativo.
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- Amplia
- aplicativos de ampliação de tela
- Amplia
- processamento de imagem personalizada
- Magnification.dll
- criando controles de lupa
- ampliação seletiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d66595cc2f5fdd8402ecd9d525e6deb1d07078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105812428"
---
# <a name="magnification-api-overview"></a><span data-ttu-id="8a79b-110">Visão geral da API de ampliação</span><span class="sxs-lookup"><span data-stu-id="8a79b-110">Magnification API Overview</span></span>

<span data-ttu-id="8a79b-111">A API de ampliação permite que fornecedores de tecnologia assistencial desenvolvam aplicativos de ampliação de tela que são executados no Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8a79b-111">The Magnification API enables assistive technology vendors to develop screen magnification applications that run on Microsoft Windows.</span></span> <span data-ttu-id="8a79b-112">Este tópico descreve a API de ampliação e explica como usá-la em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8a79b-112">This topic describes the Magnification API and explains how to use it in an application.</span></span> <span data-ttu-id="8a79b-113">Ele contém as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="8a79b-113">It contains the following sections:</span></span>

- [<span data-ttu-id="8a79b-114">Introdução</span><span class="sxs-lookup"><span data-stu-id="8a79b-114">Getting Started</span></span>](#getting-started)
- [<span data-ttu-id="8a79b-115">Conceitos básicos</span><span class="sxs-lookup"><span data-stu-id="8a79b-115">Basic Concepts</span></span>](#basic-concepts)
  - [<span data-ttu-id="8a79b-116">Tipos de lupas</span><span class="sxs-lookup"><span data-stu-id="8a79b-116">Types of Magnifiers</span></span>](#types-of-magnifiers)
  - [<span data-ttu-id="8a79b-117">Fator de ampliação</span><span class="sxs-lookup"><span data-stu-id="8a79b-117">Magnification Factor</span></span>](#magnification-factor)
  - [<span data-ttu-id="8a79b-118">Efeitos de cor</span><span class="sxs-lookup"><span data-stu-id="8a79b-118">Color Effects</span></span>](#color-effects)
  - [<span data-ttu-id="8a79b-119">Retângulo de origem</span><span class="sxs-lookup"><span data-stu-id="8a79b-119">Source Rectangle</span></span>](#source-rectangle)
  - [<span data-ttu-id="8a79b-120">Lista de filtros</span><span class="sxs-lookup"><span data-stu-id="8a79b-120">Filter List</span></span>](#filter-list)
  - [<span data-ttu-id="8a79b-121">Transformação de entrada</span><span class="sxs-lookup"><span data-stu-id="8a79b-121">Input Transform</span></span>](#input-transform)
  - [<span data-ttu-id="8a79b-122">Cursor do sistema</span><span class="sxs-lookup"><span data-stu-id="8a79b-122">System Cursor</span></span>](#system-cursor)
- [<span data-ttu-id="8a79b-123">Inicializando a biblioteca de tempo de execução da lupa</span><span class="sxs-lookup"><span data-stu-id="8a79b-123">Initializing the Magnifier Run-time Library</span></span>](#initializing-the-magnifier-run-time-library)
- [<span data-ttu-id="8a79b-124">Usando a Full-Screen lupa</span><span class="sxs-lookup"><span data-stu-id="8a79b-124">Using the Full-Screen Magnifier</span></span>](#using-the-full-screen-magnifier)
- [<span data-ttu-id="8a79b-125">Usando o controle lupa</span><span class="sxs-lookup"><span data-stu-id="8a79b-125">Using the Magnifier Control</span></span>](#using-the-magnifier-control)
  - [<span data-ttu-id="8a79b-126">Criando o controle lupa</span><span class="sxs-lookup"><span data-stu-id="8a79b-126">Creating the Magnifier Control</span></span>](#creating-the-magnifier-control)
  - [<span data-ttu-id="8a79b-127">Inicializando o controle</span><span class="sxs-lookup"><span data-stu-id="8a79b-127">Initializing the Control</span></span>](#initializing-the-control)
  - [<span data-ttu-id="8a79b-128">Configurando o retângulo de origem</span><span class="sxs-lookup"><span data-stu-id="8a79b-128">Setting the Source Rectangle</span></span>](#setting-the-source-rectangle)
  - [<span data-ttu-id="8a79b-129">Aplicando efeitos de cor</span><span class="sxs-lookup"><span data-stu-id="8a79b-129">Applying Color Effects</span></span>](#applying-color-effects)
  - [<span data-ttu-id="8a79b-130">Ampliação seletiva</span><span class="sxs-lookup"><span data-stu-id="8a79b-130">Selective Magnification</span></span>](#selective-magnification)
- [<span data-ttu-id="8a79b-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a79b-131">Related topics</span></span>](#related-topics)

## <a name="getting-started"></a><span data-ttu-id="8a79b-132">Introdução</span><span class="sxs-lookup"><span data-stu-id="8a79b-132">Getting Started</span></span>

<span data-ttu-id="8a79b-133">A versão original da API de ampliação tem suporte no Windows Vista e em sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="8a79b-133">The original release of the Magnification API is supported on Windows Vista and later operating systems.</span></span> <span data-ttu-id="8a79b-134">No Windows 8 e posterior, a API dá suporte a recursos adicionais, incluindo a ampliação de tela inteira e a definição da visibilidade do cursor do sistema ampliado.</span><span class="sxs-lookup"><span data-stu-id="8a79b-134">On Windows 8 and later, the API supports additional features, including full-screen magnification and setting the visibility of the magnified system cursor.</span></span>

<span data-ttu-id="8a79b-135">O suporte para a API de ampliação é fornecido pelo Magnification.dll.</span><span class="sxs-lookup"><span data-stu-id="8a79b-135">Support for the Magnification API is provided by Magnification.dll.</span></span> <span data-ttu-id="8a79b-136">Para compilar seu aplicativo, inclua ampliação. h e vincule a ampliação. lib.</span><span class="sxs-lookup"><span data-stu-id="8a79b-136">To compile your application, include Magnification.h and link to Magnification.lib.</span></span>

> [!Note]  
> <span data-ttu-id="8a79b-137">A API de ampliação não tem suporte no WOW64; ou seja, um aplicativo de lupa de 32 bits não será executado corretamente em janelas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8a79b-137">The Magnification API is not supported under WOW64; that is, a 32-bit magnifier application will not run correctly on 64-bit Windows.</span></span>

## <a name="basic-concepts"></a><span data-ttu-id="8a79b-138">Conceitos básicos</span><span class="sxs-lookup"><span data-stu-id="8a79b-138">Basic Concepts</span></span>

<span data-ttu-id="8a79b-139">Esta seção descreve os conceitos fundamentais em que a API de ampliação se baseia.</span><span class="sxs-lookup"><span data-stu-id="8a79b-139">This section describes the fundamental concepts that the magnification API is based on.</span></span> <span data-ttu-id="8a79b-140">Ele contém as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="8a79b-140">It contains the following parts:</span></span>

- [<span data-ttu-id="8a79b-141">Tipos de lupas</span><span class="sxs-lookup"><span data-stu-id="8a79b-141">Types of Magnifiers</span></span>](#types-of-magnifiers)
- [<span data-ttu-id="8a79b-142">Fator de ampliação</span><span class="sxs-lookup"><span data-stu-id="8a79b-142">Magnification Factor</span></span>](#magnification-factor)
- [<span data-ttu-id="8a79b-143">Efeitos de cor</span><span class="sxs-lookup"><span data-stu-id="8a79b-143">Color Effects</span></span>](#color-effects)
- [<span data-ttu-id="8a79b-144">Retângulo de origem</span><span class="sxs-lookup"><span data-stu-id="8a79b-144">Source Rectangle</span></span>](#source-rectangle)
- [<span data-ttu-id="8a79b-145">Lista de filtros</span><span class="sxs-lookup"><span data-stu-id="8a79b-145">Filter List</span></span>](#filter-list)
- [<span data-ttu-id="8a79b-146">Transformação de entrada</span><span class="sxs-lookup"><span data-stu-id="8a79b-146">Input Transform</span></span>](#input-transform)
- [<span data-ttu-id="8a79b-147">Cursor do sistema</span><span class="sxs-lookup"><span data-stu-id="8a79b-147">System Cursor</span></span>](#system-cursor)

### <a name="types-of-magnifiers"></a><span data-ttu-id="8a79b-148">Tipos de lupas</span><span class="sxs-lookup"><span data-stu-id="8a79b-148">Types of Magnifiers</span></span>

<span data-ttu-id="8a79b-149">A API dá suporte a dois tipos de ampliadores, à *lupa em tela inteira* e ao *controle de lupa*.</span><span class="sxs-lookup"><span data-stu-id="8a79b-149">The API supports two types of magnifiers, the *full-screen magnifier* and the *magnifier control*.</span></span> <span data-ttu-id="8a79b-150">A lupa de tela inteira aumenta o conteúdo da tela inteira, enquanto o controle de lupa aumenta o conteúdo de uma área específica da tela e exibe o conteúdo em uma janela.</span><span class="sxs-lookup"><span data-stu-id="8a79b-150">The full-screen magnifier magnifies the content of the entire screen, while the magnifier control magnifies the content of a particular area of the screen and displays the content in a window.</span></span> <span data-ttu-id="8a79b-151">Para Lupas, imagens e texto são ampliados e ambos permitem controlar a quantidade de ampliação.</span><span class="sxs-lookup"><span data-stu-id="8a79b-151">For both magnifiers, images and text are magnified, and both enable you to control the amount of magnification.</span></span> <span data-ttu-id="8a79b-152">Você também pode aplicar efeitos de cor ao conteúdo da tela ampliado, facilitando a visualização para pessoas que têm deficiências de cor ou precisam de cores com mais ou menos contraste.</span><span class="sxs-lookup"><span data-stu-id="8a79b-152">You can also apply color effects to the magnified screen content, making it easier to see for people who have color deficiencies or need colors that have more or less contrast.</span></span>

> [!Important]  
> <span data-ttu-id="8a79b-153">A API de controle de lupa está disponível no Windows Vista e em sistemas operacionais posteriores, enquanto a API de lupa de tela inteira está disponível apenas no Windows 8 e em sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="8a79b-153">The magnifier control API is available on Windows Vista and later operating systems, while the full-screen magnifier API is available only on Windows 8 and later operating systems.</span></span>

### <a name="magnification-factor"></a><span data-ttu-id="8a79b-154">Fator de ampliação</span><span class="sxs-lookup"><span data-stu-id="8a79b-154">Magnification Factor</span></span>

<span data-ttu-id="8a79b-155">Tanto a lupa em tela inteira quanto o controle lupa aplicam uma transformação Scale ao conteúdo da tela de ampliação.</span><span class="sxs-lookup"><span data-stu-id="8a79b-155">Both the full-screen magnifier and the magnifier control apply a scale transformation to magnify screen content.</span></span> <span data-ttu-id="8a79b-156">A quantidade de ampliação aplicada pela transformação de escala é chamada de *fator de ampliação*.</span><span class="sxs-lookup"><span data-stu-id="8a79b-156">The amount of magnification applied by the scale transformation is called the *magnification factor*.</span></span> <span data-ttu-id="8a79b-157">Ele é expresso como um valor de ponto flutuante em que 1,0 corresponde a sem ampliação e valores maiores resultam em uma quantidade correspondente de ampliação.</span><span class="sxs-lookup"><span data-stu-id="8a79b-157">It is expressed as a floating-point value where 1.0 corresponds to no magnification, and larger values result in a corresponding amount of magnification.</span></span> <span data-ttu-id="8a79b-158">Por exemplo, um valor de 1,5 torna o conteúdo da tela 50% maior.</span><span class="sxs-lookup"><span data-stu-id="8a79b-158">For example, a value of 1.5 makes the screen content 50 percent larger.</span></span> <span data-ttu-id="8a79b-159">Um fator de ampliação menor que 1,0 não é válido.</span><span class="sxs-lookup"><span data-stu-id="8a79b-159">A magnification factor less than 1.0 is not valid.</span></span>

### <a name="color-effects"></a><span data-ttu-id="8a79b-160">Efeitos de cor</span><span class="sxs-lookup"><span data-stu-id="8a79b-160">Color Effects</span></span>

<span data-ttu-id="8a79b-161">Os efeitos de cor são obtidos com a aplicação de uma matriz de transformação de cor 5 por 5 às cores do conteúdo da tela ampliado.</span><span class="sxs-lookup"><span data-stu-id="8a79b-161">Color effects are achieved by applying a 5-by-5 color transformation matrix to the colors of the magnified screen content.</span></span> <span data-ttu-id="8a79b-162">A matriz determina as intensidades dos componentes vermelho, azul, verde e alfa do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8a79b-162">The matrix determines the intensities of the red, blue, green, and alpha components of the content.</span></span> <span data-ttu-id="8a79b-163">Para obter mais informações, consulte [usando uma matriz de cores para transformar uma única cor](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) na documentação do Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="8a79b-163">For more information, see [Using a Color Matrix to Transform a Single Color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in the Windows GDI+ documentation.</span></span>

### <a name="source-rectangle"></a><span data-ttu-id="8a79b-164">Retângulo de origem</span><span class="sxs-lookup"><span data-stu-id="8a79b-164">Source Rectangle</span></span>

<span data-ttu-id="8a79b-165">A lupa de tela inteira aplica a transformação de escala e a transformação de cores à tela inteira.</span><span class="sxs-lookup"><span data-stu-id="8a79b-165">The full-screen magnifier applies the scale transformation and color transformation to the entire screen.</span></span> <span data-ttu-id="8a79b-166">O controle lupa, por outro lado, copia uma área da tela, chamada de *retângulo de origem*, para um bitmap fora da tela.</span><span class="sxs-lookup"><span data-stu-id="8a79b-166">The magnifier control, on the other hand, copies an area of the screen, called the *source rectangle*, to an off-screen bitmap.</span></span> <span data-ttu-id="8a79b-167">Em seguida, o controle aplica a transformação escala e a transformação cor, se houver, ao bitmap fora da tela.</span><span class="sxs-lookup"><span data-stu-id="8a79b-167">Next, the control applies the scale transformation and the color transformation, if any, to the off-screen bitmap.</span></span> <span data-ttu-id="8a79b-168">Por fim, o controle exibe o bitmap escalado e transformado por cor na janela de controle da lupa.</span><span class="sxs-lookup"><span data-stu-id="8a79b-168">Finally, the control displays the scaled and color-transformed bitmap in the magnifier control window.</span></span>

### <a name="filter-list"></a><span data-ttu-id="8a79b-169">Lista de filtros</span><span class="sxs-lookup"><span data-stu-id="8a79b-169">Filter List</span></span>

<span data-ttu-id="8a79b-170">Por padrão, o controle lupa amplia todas as janelas no retângulo de origem especificado.</span><span class="sxs-lookup"><span data-stu-id="8a79b-170">By default, the magnifier control magnifies all windows in the specified source rectangle.</span></span> <span data-ttu-id="8a79b-171">No entanto, ao fornecer uma *lista de filtros* de identificadores de janela, você pode controlar quais janelas estão incluídas no conteúdo ampliado e quais não são.</span><span class="sxs-lookup"><span data-stu-id="8a79b-171">However, by providing a *filter list* of window handles, you can control which windows are included in the magnified content, and which are not.</span></span> <span data-ttu-id="8a79b-172">Para obter mais informações, consulte [ampliação seletiva](#selective-magnification).</span><span class="sxs-lookup"><span data-stu-id="8a79b-172">For more information, see [Selective Magnification](#selective-magnification).</span></span>

<span data-ttu-id="8a79b-173">A lupa de tela inteira não dá suporte a uma lista de filtros; sempre aumenta todas as janelas na tela.</span><span class="sxs-lookup"><span data-stu-id="8a79b-173">The full-screen magnifier does not support a filter list; it always magnifies all windows on the screen.</span></span>

### <a name="input-transform"></a><span data-ttu-id="8a79b-174">Transformação de entrada</span><span class="sxs-lookup"><span data-stu-id="8a79b-174">Input Transform</span></span>

<span data-ttu-id="8a79b-175">Normalmente, o conteúdo da tela ampliado é "invisível" à caneta do usuário ou à entrada por toque.</span><span class="sxs-lookup"><span data-stu-id="8a79b-175">Normally, magnified screen content is "invisible" to user pen or touch input.</span></span> <span data-ttu-id="8a79b-176">Por exemplo, se o usuário tocar na imagem ampliada de um controle, o sistema não passará necessariamente a entrada para o controle.</span><span class="sxs-lookup"><span data-stu-id="8a79b-176">For example, if the user taps the magnified image of a control, the system does not necessarily pass the input to the control.</span></span> <span data-ttu-id="8a79b-177">Em vez disso, o sistema passa a entrada para qualquer item (se houver) que resida nas coordenadas de tela tocadas na área de trabalho não ampliada.</span><span class="sxs-lookup"><span data-stu-id="8a79b-177">Instead, the system passes the input to whatever item (if any) resides at the tapped screen coordinates on the unmagnified desktop.</span></span> <span data-ttu-id="8a79b-178">A função [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) permite que você especifique uma *transformação de entrada* que mapeia o espaço de coordenadas do conteúdo da tela ampliado para o espaço de coordenadas de tela real (não ampliado).</span><span class="sxs-lookup"><span data-stu-id="8a79b-178">The [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) function enables you to specify an *input transformation* that maps the coordinate space of the magnified screen content to the actual (unmagnified) screen coordinate space.</span></span> <span data-ttu-id="8a79b-179">Isso permite que o sistema passe a entrada de caneta ou toque que é inserida no conteúdo da tela ampliado, para o elemento da interface do usuário correto na tela.</span><span class="sxs-lookup"><span data-stu-id="8a79b-179">This enables the system to pass pen or touch input that is entered in magnified screen content, to the correct UI element on the screen.</span></span>

> [!Note]  
> <span data-ttu-id="8a79b-180">O processo de chamada deve ter privilégios de UIAccess para definir a transformação de entrada.</span><span class="sxs-lookup"><span data-stu-id="8a79b-180">The calling process must have UIAccess privileges to set the input transform.</span></span> <span data-ttu-id="8a79b-181">Para obter mais informações, consulte [considerações de segurança de automação da interface do usuário](../uiauto-securityoverview.md) e [/MANIFESTUAC (incorpora informações do UAC no manifesto)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).</span><span class="sxs-lookup"><span data-stu-id="8a79b-181">For more information, see [UI Automation Security Considerations](../uiauto-securityoverview.md) and [/MANIFESTUAC (Embeds UAC information in manifest)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).</span></span>

### <a name="system-cursor"></a><span data-ttu-id="8a79b-182">Cursor do sistema</span><span class="sxs-lookup"><span data-stu-id="8a79b-182">System Cursor</span></span>

<span data-ttu-id="8a79b-183">A função [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) permite mostrar ou ocultar o cursor do sistema.</span><span class="sxs-lookup"><span data-stu-id="8a79b-183">The [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) function enables you to show or hide the system cursor.</span></span> <span data-ttu-id="8a79b-184">Se você mostrar o cursor do sistema quando a lupa de tela inteira estiver ativa, o cursor do sistema sempre será ampliado junto com o restante do conteúdo da tela.</span><span class="sxs-lookup"><span data-stu-id="8a79b-184">If you show the system cursor when the full-screen magnifier is active, the system cursor is always magnified along with the rest of the screen content.</span></span> <span data-ttu-id="8a79b-185">Se você ocultar o cursor do sistema quando a lupa de tela inteira estiver ativa, o cursor do sistema não estará visível.</span><span class="sxs-lookup"><span data-stu-id="8a79b-185">If you hide the system cursor when the full-screen magnifier is active, the system cursor is not visible at all.</span></span>

<span data-ttu-id="8a79b-186">Com o controle lupa, a função [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) mostra ou oculta o cursor do sistema não ampliado, mas não tem efeito sobre o cursor do sistema ampliado.</span><span class="sxs-lookup"><span data-stu-id="8a79b-186">With the magnifier control, the [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) function shows or hides the unmagnified system cursor, but has no effect on the magnified system cursor.</span></span> <span data-ttu-id="8a79b-187">A visibilidade do cursor do sistema ampliado depende se o controle de lupa tem o estilo de [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8a79b-187">The visibility of the magnified system cursor depends on whether the magnifier control has the [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) style.</span></span> <span data-ttu-id="8a79b-188">Se ele tiver esse estilo, o controle lupa exibirá o cursor do sistema ampliado, juntamente com o conteúdo da tela ampliada, sempre que o cursor do sistema entrar no retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="8a79b-188">If it has this style, the magnifier control displays the magnified system cursor, along with the magnified screen content, whenever the system cursor enters the source rectangle.</span></span>

## <a name="initializing-the-magnifier-run-time-library"></a><span data-ttu-id="8a79b-189">Inicializando a biblioteca de tempo de execução da lupa</span><span class="sxs-lookup"><span data-stu-id="8a79b-189">Initializing the Magnifier Run-time Library</span></span>

<span data-ttu-id="8a79b-190">Antes de poder chamar qualquer outra função de API de lupa, você deve criar e inicializar os objetos de tempo de execução da lupa chamando a função [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) .</span><span class="sxs-lookup"><span data-stu-id="8a79b-190">Before you can call any other magnifier API functions, you must create and initialize the magnifier run-time objects by calling the [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) function.</span></span> <span data-ttu-id="8a79b-191">Da mesma forma, depois de terminar de usar a API de lupa, chame a função [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) para destruir os objetos de tempo de execução da lupa e liberar os recursos do sistema associados.</span><span class="sxs-lookup"><span data-stu-id="8a79b-191">Similarly, after you finish using the magnifier API, call the [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) function to destroy the magnifier run-time objects and free the associated system resources.</span></span>

## <a name="using-the-full-screen-magnifier"></a><span data-ttu-id="8a79b-192">Usando a Full-Screen lupa</span><span class="sxs-lookup"><span data-stu-id="8a79b-192">Using the Full-Screen Magnifier</span></span>

<span data-ttu-id="8a79b-193">Para usar a lupa de tela inteira, chame a função [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) .</span><span class="sxs-lookup"><span data-stu-id="8a79b-193">To use the full-screen magnifier, call the [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) function.</span></span> <span data-ttu-id="8a79b-194">O parâmetro *magLevel* especifica o fator de ampliação.</span><span class="sxs-lookup"><span data-stu-id="8a79b-194">The *magLevel* parameter specifies the magnification factor.</span></span> <span data-ttu-id="8a79b-195">Os parâmetros *xOffset* e *yOffset* especificam como o conteúdo da tela ampliada é posicionado em relação à tela.</span><span class="sxs-lookup"><span data-stu-id="8a79b-195">The *xOffset* and *yOffset* parameters specify how the magnified screen content is positioned relative to the screen.</span></span>

<span data-ttu-id="8a79b-196">Quando o conteúdo da tela é ampliado, ele se torna maior do que a própria tela.</span><span class="sxs-lookup"><span data-stu-id="8a79b-196">When the screen content is magnified, it becomes larger than the screen itself.</span></span> <span data-ttu-id="8a79b-197">Parte do conteúdo ultrapassa as bordas da tela e torna-se invisível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="8a79b-197">Some portion of the content extends beyond the edges of the screen and becomes invisible to the user.</span></span> <span data-ttu-id="8a79b-198">Os parâmetros *xOffset* e *YOffset* da função [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) determinam qual parte do conteúdo da tela ampliada aparece na tela.</span><span class="sxs-lookup"><span data-stu-id="8a79b-198">The *xOffset* and *yOffset* parameters of the [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) function determine which portion of the magnified screen content appears on the screen.</span></span> <span data-ttu-id="8a79b-199">Juntos, os parâmetros especificam as coordenadas de um ponto no conteúdo da tela não ampliada.</span><span class="sxs-lookup"><span data-stu-id="8a79b-199">Together, the parameters specify the coordinates of a point in the unmagnified screen content.</span></span> <span data-ttu-id="8a79b-200">Quando o conteúdo é ampliado, ele é posicionado com o ponto especificado no canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="8a79b-200">When the content is magnified, it is positioned with the specified point at the upper-left corner of the screen.</span></span>

<span data-ttu-id="8a79b-201">O exemplo a seguir define o fator de ampliação para a lupa de tela inteira e coloca o centro do conteúdo da tela ampliado no centro da tela.</span><span class="sxs-lookup"><span data-stu-id="8a79b-201">The following example sets the magnification factor for the full-screen magnifier and places the center of the magnified screen content at the center of the screen.</span></span>

```C++
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}
```

<span data-ttu-id="8a79b-202">Use a função [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) para aplicar efeitos de cor ao conteúdo de tela inteira definindo uma matriz de transformação de cor definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8a79b-202">Use the [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) function to apply color effects to the full-screen content by setting an application-defined color transformation matrix.</span></span> <span data-ttu-id="8a79b-203">Por exemplo, o exemplo a seguir define uma matriz de transformação de cor que converte cores em escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="8a79b-203">For example, the following example sets a color transformation matrix that converts colors to grayscale.</span></span>

```C++
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &amp;g_MagEffectGrayscale : &amp;g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}
```

<span data-ttu-id="8a79b-204">Você pode recuperar o fator de ampliação e os valores de deslocamento atuais chamando a função [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) .</span><span class="sxs-lookup"><span data-stu-id="8a79b-204">You can retrieve the current magnification factor and offset values by calling the [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) function.</span></span> <span data-ttu-id="8a79b-205">Você pode recuperar a matriz de transformação de cor atual chamando a função [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) .</span><span class="sxs-lookup"><span data-stu-id="8a79b-205">You can retrieve the current color transformation matrix by calling the [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) function.</span></span>

## <a name="using-the-magnifier-control"></a><span data-ttu-id="8a79b-206">Usando o controle lupa</span><span class="sxs-lookup"><span data-stu-id="8a79b-206">Using the Magnifier Control</span></span>

<span data-ttu-id="8a79b-207">O controle lupa amplia o conteúdo de uma área específica da tela e exibe o conteúdo em uma janela.</span><span class="sxs-lookup"><span data-stu-id="8a79b-207">The magnifier control magnifies the content of a particular area of the screen and displays the content in a window.</span></span> <span data-ttu-id="8a79b-208">Esta seção descreve como usar o controle lupa.</span><span class="sxs-lookup"><span data-stu-id="8a79b-208">This section describes how to use the magnifier control.</span></span> <span data-ttu-id="8a79b-209">Ele contém as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="8a79b-209">It contains the following parts:</span></span>

- [<span data-ttu-id="8a79b-210">Criando o controle lupa</span><span class="sxs-lookup"><span data-stu-id="8a79b-210">Creating the Magnifier Control</span></span>](#creating-the-magnifier-control)
- [<span data-ttu-id="8a79b-211">Inicializando o controle</span><span class="sxs-lookup"><span data-stu-id="8a79b-211">Initializing the Control</span></span>](#initializing-the-control)
- [<span data-ttu-id="8a79b-212">Configurando o retângulo de origem</span><span class="sxs-lookup"><span data-stu-id="8a79b-212">Setting the Source Rectangle</span></span>](#setting-the-source-rectangle)
- [<span data-ttu-id="8a79b-213">Aplicando efeitos de cor</span><span class="sxs-lookup"><span data-stu-id="8a79b-213">Applying Color Effects</span></span>](#applying-color-effects)
- [<span data-ttu-id="8a79b-214">Ampliação seletiva</span><span class="sxs-lookup"><span data-stu-id="8a79b-214">Selective Magnification</span></span>](#selective-magnification)

### <a name="creating-the-magnifier-control"></a><span data-ttu-id="8a79b-215">Criando o controle lupa</span><span class="sxs-lookup"><span data-stu-id="8a79b-215">Creating the Magnifier Control</span></span>

<span data-ttu-id="8a79b-216">O controle lupa deve ser hospedado em uma janela criada com o estilo estendido [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8a79b-216">The magnifier control must be hosted in a window created with the [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) extended style.</span></span> <span data-ttu-id="8a79b-217">Depois de criar a janela do host, chame [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) para definir a opacidade da janela do host.</span><span class="sxs-lookup"><span data-stu-id="8a79b-217">After creating the host window, call [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) to set the opacity of the host window.</span></span> <span data-ttu-id="8a79b-218">A janela do host é normalmente definida como opacidade total para evitar que o conteúdo da tela subjacente seja mostrado no entanto.</span><span class="sxs-lookup"><span data-stu-id="8a79b-218">The host window is typically set to full opacity to prevent the underlying screen content from showing though.</span></span> <span data-ttu-id="8a79b-219">O exemplo a seguir mostra como definir a janela do host para opacidade total:</span><span class="sxs-lookup"><span data-stu-id="8a79b-219">The following example shows how to set the host window to full opacity:</span></span>

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

<span data-ttu-id="8a79b-220">Se você aplicar o estilo de [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) à janela do host, os cliques do mouse serão passados para qualquer objeto que esteja atrás da janela do host no local do cursor do mouse.</span><span class="sxs-lookup"><span data-stu-id="8a79b-220">If you apply the [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) style to the host window, mouse clicks are passed to whatever object is behind the host window at the location of the mouse cursor.</span></span> <span data-ttu-id="8a79b-221">Lembre-se de que, como a janela do host não processa cliques do mouse, o usuário não poderá mover ou redimensionar a janela de ampliação usando o mouse.</span><span class="sxs-lookup"><span data-stu-id="8a79b-221">Be aware that, because the host window does not process mouse clicks, the user will not be able to move or resize the magnification window by using the mouse.</span></span>

<span data-ttu-id="8a79b-222">A classe Window da janela de controle lupa deve ser **WC_MAGNIFIER**.</span><span class="sxs-lookup"><span data-stu-id="8a79b-222">The window class of the magnifier control window must be **WC_MAGNIFIER**.</span></span> <span data-ttu-id="8a79b-223">Se você aplicar o estilo de [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) , o controle lupa incluirá o cursor do sistema no conteúdo da tela ampliada e o cursor será ampliado junto com o conteúdo da tela.</span><span class="sxs-lookup"><span data-stu-id="8a79b-223">If you apply the [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) style, the magnifier control includes the system cursor in the magnified screen contents, and the cursor is magnified along with the screen contents.</span></span>

<span data-ttu-id="8a79b-224">Depois de criar o controle de lupa, mantenha o identificador de janela para que você possa passá-lo para outras funções.</span><span class="sxs-lookup"><span data-stu-id="8a79b-224">After you create the magnifier control, keep the window handle so that you can pass it to other functions.</span></span>

<span data-ttu-id="8a79b-225">O exemplo a seguir mostra como criar o controle lupa.</span><span class="sxs-lookup"><span data-stu-id="8a79b-225">The following example shows how to create the magnifier control.</span></span>

```C++
// Description: 
//   Registers the host window class, creates the host window, sets the layered
//   window attributes, and creates the magnifier control. 
// Parameters:
//   hInstance - Instance handle of the application.
// Variables:
//   HostWndProc - Window procedure of the host window.
//   WindowClassName - Name of the window class.
//   WindowTitle - Title of the host window.
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
// 
BOOL CreateMagnifier(HINSTANCE hInstance)
{
   // Register the host window class.
    WNDCLASSEX wcex = {};
    wcex.cbSize = sizeof(WNDCLASSEX); 
    wcex.style          = 0;
    wcex.lpfnWndProc    = HostWndProc;
    wcex.hInstance      = hInstance;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(1 + COLOR_BTNFACE);
    wcex.lpszClassName  = WindowClassName;
    
    if (RegisterClassEx(&amp;wcex) == 0)
        return FALSE;

    // Create the host window. 
    hwndHost = CreateWindowEx(WS_EX_TOPMOST | WS_EX_LAYERED | WS_EX_TRANSPARENT, 
        WindowClassName, WindowTitle, 
        WS_CLIPCHILDREN,
        0, 0, 0, 0,
        NULL, NULL, hInstance, NULL);
    if (!hwndHost)
    {
        return FALSE;
    }

    // Make the window opaque.
    SetLayeredWindowAttributes(hwndHost, 0, 255, LWA_ALPHA);

    // Create a magnifier control that fills the client area.
    hwndMag = CreateWindow(WC_MAGNIFIER, TEXT("MagnifierWindow"), 
        WS_CHILD | MS_SHOWMAGNIFIEDCURSOR | WS_VISIBLE,
        0, 0, 
        LENS_WIDTH, 
        LENS_HEIGHT, 
        hwndHost, NULL, hInstance, NULL );
    if (!hwndMag)
    {
        return FALSE;
    }

    return TRUE;
}
```

### <a name="initializing-the-control"></a><span data-ttu-id="8a79b-226">Inicializando o controle</span><span class="sxs-lookup"><span data-stu-id="8a79b-226">Initializing the Control</span></span>

<span data-ttu-id="8a79b-227">Depois de criar o controle lupa, você deve chamar a função [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) para especificar o fator de ampliação.</span><span class="sxs-lookup"><span data-stu-id="8a79b-227">After creating the magnifier control, you must call the [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) function to specify the magnification factor.</span></span> <span data-ttu-id="8a79b-228">Isso é simplesmente uma questão de especificar uma matriz de</span><span class="sxs-lookup"><span data-stu-id="8a79b-228">This is simply a matter of specifying a matrix of</span></span>

<span data-ttu-id="8a79b-229">(*n*, 0,0, 0,0)</span><span class="sxs-lookup"><span data-stu-id="8a79b-229">(*n*, 0.0, 0.0)</span></span>

<span data-ttu-id="8a79b-230">(0,0, *n*, 0,0)</span><span class="sxs-lookup"><span data-stu-id="8a79b-230">(0.0, *n*, 0.0)</span></span>

<span data-ttu-id="8a79b-231">(0,0, 0,0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="8a79b-231">(0.0, 0.0, 1.0)</span></span>

<span data-ttu-id="8a79b-232">onde *n* é o fator de ampliação.</span><span class="sxs-lookup"><span data-stu-id="8a79b-232">where *n* is the magnification factor.</span></span>

<span data-ttu-id="8a79b-233">O exemplo a seguir mostra como definir o fator de ampliação para o controle lupa.</span><span class="sxs-lookup"><span data-stu-id="8a79b-233">The following example shows how to set the magnification factor for the magnifier control.</span></span>

```C++
// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
```

### <a name="setting-the-source-rectangle"></a><span data-ttu-id="8a79b-234">Configurando o retângulo de origem</span><span class="sxs-lookup"><span data-stu-id="8a79b-234">Setting the Source Rectangle</span></span>

<span data-ttu-id="8a79b-235">À medida que o usuário move o cursor do mouse pela tela, seu aplicativo chama a função [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) para especificar a parte da tela subjacente que será ampliada.</span><span class="sxs-lookup"><span data-stu-id="8a79b-235">As the user moves the mouse cursor around the screen, your application calls the [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) function to specify the part of the underlying screen that is to be magnified.</span></span>

<span data-ttu-id="8a79b-236">A função de exemplo a seguir calcula a posição e as dimensões do retângulo de origem (com base na posição do mouse e as dimensões da janela da lupa dividida pelo fator de ampliação) e define o retângulo de origem de acordo.</span><span class="sxs-lookup"><span data-stu-id="8a79b-236">The following example function calculates the position and dimensions of the source rectangle (based on the mouse position and the dimensions of the magnifier window divided by the magnification factor) and sets the source rectangle accordingly.</span></span> <span data-ttu-id="8a79b-237">A função também centraliza a área cliente da janela host na posição do mouse.</span><span class="sxs-lookup"><span data-stu-id="8a79b-237">The function also centers the client area of the host window at the mouse position.</span></span> <span data-ttu-id="8a79b-238">Essa função seria chamada em intervalos para atualizar a janela de ampliação.</span><span class="sxs-lookup"><span data-stu-id="8a79b-238">This function would be called at intervals to update the magnification window.</span></span>

```C++
// Description: 
//   Called by a timer to update the contents of the magnifier window and to set
//   the position of the host window. 
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
//   MAGFACTOR - The magnification factor.
//
void CALLBACK UpdateMagWindow(HWND /*hwnd*/, UINT /*uMsg*/, 
        UINT_PTR /*idEvent*/, DWORD /*dwTime*/)
{
    // Get the mouse coordinates.
    POINT mousePoint;
    GetCursorPos(&amp;mousePoint);

    // Calculate a source rectangle that is centered at the mouse coordinates. 
    // Size the rectangle so that it fits into the magnifier window (the lens).
    RECT sourceRect;
    int borderWidth = GetSystemMetrics(SM_CXFIXEDFRAME);
    int captionHeight = GetSystemMetrics(SM_CYCAPTION);
    sourceRect.left = (mousePoint.x - (int)((LENS_WIDTH / 2) / MAGFACTOR)) + 
             (int)(borderWidth / MAGFACTOR);
    sourceRect.top = (mousePoint.y - (int)((LENS_HEIGHT / 2) / MAGFACTOR)) + 
             (int)(captionHeight / MAGFACTOR) + (int)(borderWidth / MAGFACTOR); 
    sourceRect.right = LENS_WIDTH;
    sourceRect.bottom = LENS_HEIGHT;

    // Pass the source rectangle to the magnifier control.
    MagSetWindowSource(hwndMag, sourceRect);

    // Move the host window so that the origin of the client area lines up
    // with the origin of the magnified source rectangle.
    MoveWindow(hwndHost, 
        (mousePoint.x - LENS_WIDTH / 2), 
        (mousePoint.y - LENS_HEIGHT / 2), 
        LENS_WIDTH, 
        LENS_HEIGHT,
        FALSE);

    // Force the magnifier control to redraw itself.
    InvalidateRect(hwndMag, NULL, TRUE);

    return;
}
```

### <a name="applying-color-effects"></a><span data-ttu-id="8a79b-239">Aplicando efeitos de cor</span><span class="sxs-lookup"><span data-stu-id="8a79b-239">Applying Color Effects</span></span>

<span data-ttu-id="8a79b-240">Um controle de lupa com o estilo [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) aplica uma matriz de transformação de cor interna que inverte as cores do conteúdo da tela ampliada.</span><span class="sxs-lookup"><span data-stu-id="8a79b-240">A magnifier control that has the [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) style applies a built-in color transformation matrix that inverts the colors of the magnified screen content.</span></span> <span data-ttu-id="8a79b-241">A ilustração a seguir mostra o conteúdo de tela em um controle de lupa que tem o estilo de **MS_INVERTCOLORS** .</span><span class="sxs-lookup"><span data-stu-id="8a79b-241">The following illustration shows screen content in a magnifier control that has the **MS_INVERTCOLORS** style.</span></span>

![captura de tela do conteúdo ampliado com cores invertidas](images/color-inversion.png)

<span data-ttu-id="8a79b-243">A função [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) permite que você aplique outros efeitos de cor configurando uma matriz de transformação de cor definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8a79b-243">The [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) function enables you to apply other color effects by setting an application-defined color transformation matrix.</span></span> <span data-ttu-id="8a79b-244">Por exemplo, a função a seguir define uma matriz de transformação de cor que converte cores em escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="8a79b-244">For example, the following function sets a color transformation matrix that converts colors to grayscale.</span></span>


```C++
// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
```

<span data-ttu-id="8a79b-245">Para obter mais informações sobre como funcionam as transformações de cores, consulte [usando uma matriz de cores para transformar uma única cor](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) na documentação do GDI+.</span><span class="sxs-lookup"><span data-stu-id="8a79b-245">For more information about how color transformations work, see [Using a Color Matrix to Transform a Single Color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in the GDI+ documentation.</span></span>

### <a name="selective-magnification"></a><span data-ttu-id="8a79b-246">Ampliação seletiva</span><span class="sxs-lookup"><span data-stu-id="8a79b-246">Selective Magnification</span></span>

<span data-ttu-id="8a79b-247">Por padrão, a ampliação é aplicada a todas as janelas que não sejam a própria janela de ampliação.</span><span class="sxs-lookup"><span data-stu-id="8a79b-247">By default, magnification is applied to all windows other than the magnification window itself.</span></span> <span data-ttu-id="8a79b-248">Para especificar quais janelas devem ser ampliadas, chame a função [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) .</span><span class="sxs-lookup"><span data-stu-id="8a79b-248">To specify which windows are to be magnified, call the [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) function.</span></span> <span data-ttu-id="8a79b-249">Esse método usa uma lista do Windows para ampliar ou uma lista de janelas a serem excluídas da ampliação.</span><span class="sxs-lookup"><span data-stu-id="8a79b-249">This method takes either a list of windows to magnify, or a list of windows to exclude from magnification.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a79b-250">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a79b-250">Related topics</span></span>

[<span data-ttu-id="8a79b-251">API de ampliação</span><span class="sxs-lookup"><span data-stu-id="8a79b-251">Magnification API</span></span>](entry-magapi-sdk.md)