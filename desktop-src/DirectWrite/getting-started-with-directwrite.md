---
title: Tutorial Introdução com DirectWrite
description: Este documento mostra como usar DirectWrite e Direct2D para criar texto simples que contém um único formato e, em seguida, o texto que contém vários formatos.
ms.assetid: cc2758d7-3f47-452a-8d81-3f777fe490ec
keywords:
- DirectWrite, tutorial
- DirectWrite, tutorial de introdução
- DirectWrite, Direct2D
- Direct2D
- DirectWrite, interface IDWriteTextLayout
- Interface IDWriteTextLayout
- DirectWrite, interface IDWriteTypography
- Interface IDWriteTypography
- DirectWrite, interface IDWriteTextFormat
- Interface IDWriteTextFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb385ff78650a16599a32d76d7c51ba575de47
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294302"
---
# <a name="tutorial-getting-started-with-directwrite"></a><span data-ttu-id="46112-113">Tutorial: Introdução com DirectWrite</span><span class="sxs-lookup"><span data-stu-id="46112-113">Tutorial: Getting Started with DirectWrite</span></span>

<span data-ttu-id="46112-114">Este documento mostra como usar [DirectWrite](direct-write-portal.md) e [Direct2D](rendering-by-using-direct2d.md) para criar texto simples que contém um único formato e, em seguida, o texto que contém vários formatos.</span><span class="sxs-lookup"><span data-stu-id="46112-114">This document shows you how to use [DirectWrite](direct-write-portal.md) and [Direct2D](rendering-by-using-direct2d.md) to create simple text that contains a single format, and then text that contains multiple formats.</span></span>

<span data-ttu-id="46112-115">Este tutorial contém as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="46112-115">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="46112-116">Código-fonte</span><span class="sxs-lookup"><span data-stu-id="46112-116">Source Code</span></span>](#source-code)
-   [<span data-ttu-id="46112-117">Desenho de texto simples</span><span class="sxs-lookup"><span data-stu-id="46112-117">Drawing Simple Text</span></span>](#drawing-simple-text)
    -   [<span data-ttu-id="46112-118">Parte 1: declare os recursos DirectWrite e Direct2D.</span><span class="sxs-lookup"><span data-stu-id="46112-118">Part 1: Declare DirectWrite and Direct2D Resources.</span></span>](#part-1-declare-directwrite-and-direct2d-resources)
    -   [<span data-ttu-id="46112-119">Parte 2: criar recursos independentes de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46112-119">Part 2: Create Device Independent Resources.</span></span>](#part-2-create-device-independent-resources)
    -   [<span data-ttu-id="46112-120">Parte 3: criar Device-Dependent recursos.</span><span class="sxs-lookup"><span data-stu-id="46112-120">Part 3: Create Device-Dependent Resources.</span></span>](#part-3-create-device-dependent-resources)
    -   [<span data-ttu-id="46112-121">Parte 4: desenhar texto usando o método DrawText Direct2D.</span><span class="sxs-lookup"><span data-stu-id="46112-121">Part 4: Draw Text By Using the Direct2D DrawText Method.</span></span>](#part-4-draw-text-by-using-the-direct2d-drawtext-method)
    -   [<span data-ttu-id="46112-122">Parte 5: renderizar o conteúdo da janela usando Direct2D</span><span class="sxs-lookup"><span data-stu-id="46112-122">Part 5: Render the Window Contents Using Direct2D</span></span>](#part-5-render-the-window-contents-using-direct2d)
-   [<span data-ttu-id="46112-123">Desenhar texto com vários formatos.</span><span class="sxs-lookup"><span data-stu-id="46112-123">Drawing Text with Multiple Formats.</span></span>](#drawing-text-with-multiple-formats)
    -   [<span data-ttu-id="46112-124">Parte 1: criar uma interface IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="46112-124">Part 1: Create an IDWriteTextLayout Interface.</span></span>](#part-1-create-an-idwritetextlayout-interface)
    -   [<span data-ttu-id="46112-125">Parte 2: aplicando a formatação com IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="46112-125">Part 2: Applying Formatting with IDWriteTextLayout.</span></span>](#part-2-applying-formatting-with-idwritetextlayout)
    -   [<span data-ttu-id="46112-126">Parte 3: adicionando recursos tipográficos com IDWriteTypography.</span><span class="sxs-lookup"><span data-stu-id="46112-126">Part 3: Adding Typographic Features with IDWriteTypography.</span></span>](#part-3-adding-typographic-features-with-idwritetypography)
    -   [<span data-ttu-id="46112-127">Parte 4: desenhar texto usando o método Direct2D DrawTextLayout.</span><span class="sxs-lookup"><span data-stu-id="46112-127">Part 4: Draw Text Using the Direct2D DrawTextLayout Method.</span></span>](#part-4-draw-text-using-the-direct2d-drawtextlayout-method)

## <a name="source-code"></a><span data-ttu-id="46112-128">Código-fonte</span><span class="sxs-lookup"><span data-stu-id="46112-128">Source Code</span></span>

<span data-ttu-id="46112-129">O código-fonte mostrado nesta visão geral é obtido do [exemplo de Olá, mundo DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="46112-129">The source code shown in this overview is taken from the [DirectWrite Hello World sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span> <span data-ttu-id="46112-130">Cada parte é implementada em uma classe separada (SimpleText e multiformattedtext) e é exibida em uma janela filho separada.</span><span class="sxs-lookup"><span data-stu-id="46112-130">Each part is implemented in a separate class (SimpleText and MultiformattedText) and is displayed in a separate child window.</span></span> <span data-ttu-id="46112-131">Cada classe representa uma janela do Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="46112-131">Each class represents a Microsoft Win32 window.</span></span> <span data-ttu-id="46112-132">Além do método *WndProc* , cada classe contém os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="46112-132">In addition to the *WndProc* method, each class contains the following methods:</span></span>



| <span data-ttu-id="46112-133">Função</span><span class="sxs-lookup"><span data-stu-id="46112-133">Function</span></span>                              | <span data-ttu-id="46112-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="46112-134">Description</span></span>                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46112-135">**CreateDeviceIndependentResources**</span><span class="sxs-lookup"><span data-stu-id="46112-135">**CreateDeviceIndependentResources**</span></span>  | <span data-ttu-id="46112-136">Cria recursos independentes de dispositivo, para que eles possam ser reutilizados em qualquer lugar.</span><span class="sxs-lookup"><span data-stu-id="46112-136">Creates resources that are device independent, so they can be reused anywhere.</span></span>                      |
| <span data-ttu-id="46112-137">**DiscardDeviceIndependentResources**</span><span class="sxs-lookup"><span data-stu-id="46112-137">**DiscardDeviceIndependentResources**</span></span> | <span data-ttu-id="46112-138">Libera os recursos independentes do dispositivo depois que eles não são mais necessários.</span><span class="sxs-lookup"><span data-stu-id="46112-138">Releases the device-independent resources after they are no longer needed.</span></span>                          |
| <span data-ttu-id="46112-139">**CreateDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="46112-139">**CreateDeviceResources**</span></span>             | <span data-ttu-id="46112-140">Cria recursos, como pincéis e destinos de renderização, que estão vinculados a um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="46112-140">Creates resources, such as brushes and render targets, that are tied to a particular device.</span></span>        |
| <span data-ttu-id="46112-141">**DiscardDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="46112-141">**DiscardDeviceResources**</span></span>            | <span data-ttu-id="46112-142">Libera os recursos dependentes do dispositivo depois que eles não são mais necessários.</span><span class="sxs-lookup"><span data-stu-id="46112-142">Releases the device-dependent resources after they are no longer needed.</span></span>                            |
| <span data-ttu-id="46112-143">**DrawD2DContent**</span><span class="sxs-lookup"><span data-stu-id="46112-143">**DrawD2DContent**</span></span>                    | <span data-ttu-id="46112-144">Usa [Direct2D](../direct2d/direct2d-portal.md) para renderizar para a tela.</span><span class="sxs-lookup"><span data-stu-id="46112-144">Uses [Direct2D](../direct2d/direct2d-portal.md) to render to the screen.</span></span>                              |
| <span data-ttu-id="46112-145">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="46112-145">**DrawText**</span></span>                          | <span data-ttu-id="46112-146">Desenha a cadeia de texto usando [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="46112-146">Draws the text string by using [Direct2D](../direct2d/direct2d-portal.md).</span></span>                            |
| <span data-ttu-id="46112-147">**OnResize**</span><span class="sxs-lookup"><span data-stu-id="46112-147">**OnResize**</span></span>                          | <span data-ttu-id="46112-148">Redimensiona o destino de renderização [Direct2D](../direct2d/direct2d-portal.md) quando o tamanho da janela é alterado.</span><span class="sxs-lookup"><span data-stu-id="46112-148">Resizes the [Direct2D](../direct2d/direct2d-portal.md) render target when the window size is changed.</span></span> |



 

<span data-ttu-id="46112-149">Você pode usar o exemplo fornecido ou usar as instruções a seguir para adicionar [DirectWrite](direct-write-portal.md) e [Direct2D](rendering-by-using-direct2d.md) ao seu próprio aplicativo Win32.</span><span class="sxs-lookup"><span data-stu-id="46112-149">You can use the sample provided, or use the instructions that follow to add [DirectWrite](direct-write-portal.md) and [Direct2D](rendering-by-using-direct2d.md) to your own Win32 application.</span></span> <span data-ttu-id="46112-150">Para obter mais informações sobre o exemplo e os arquivos de projeto associados, consulte o [exemplo DirectWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="46112-150">For more information about the sample and the associated project files, see the [DirectWriteHelloWorld sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="drawing-simple-text"></a><span data-ttu-id="46112-151">Desenho de texto simples</span><span class="sxs-lookup"><span data-stu-id="46112-151">Drawing Simple Text</span></span>

<span data-ttu-id="46112-152">Esta seção mostra como usar [DirectWrite](direct-write-portal.md) e [Direct2D](../direct2d/direct2d-portal.md) para renderizar texto simples que tem um único formato, como mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="46112-152">This section shows how to use [DirectWrite](direct-write-portal.md) and [Direct2D](../direct2d/direct2d-portal.md) to render simple text that has a single format, as shown in the following screen shot.</span></span>

![captura de tela de "Olá, mundo usando DirectWrite!"](images/simplecropped.png)

<span data-ttu-id="46112-155">O desenho de texto simples na tela requer quatro componentes:</span><span class="sxs-lookup"><span data-stu-id="46112-155">Drawing simple text to the screen requires four components:</span></span>

-   <span data-ttu-id="46112-156">Uma cadeia de caracteres a ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="46112-156">A character string to render.</span></span>
-   <span data-ttu-id="46112-157">Uma instância de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span><span class="sxs-lookup"><span data-stu-id="46112-157">An instance of [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span></span>
-   <span data-ttu-id="46112-158">As dimensões da área para conter o texto.</span><span class="sxs-lookup"><span data-stu-id="46112-158">The dimensions of the area to contain the text.</span></span>
-   <span data-ttu-id="46112-159">Um objeto que pode renderizar o texto.</span><span class="sxs-lookup"><span data-stu-id="46112-159">An object that can render the text.</span></span> <span data-ttu-id="46112-160">Neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="46112-160">In this tutorial.</span></span> <span data-ttu-id="46112-161">Você usa um destino de renderização [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="46112-161">you use a [Direct2D](../direct2d/direct2d-portal.md) render target.</span></span>

<span data-ttu-id="46112-162">A interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) descreve o nome, o tamanho, o peso, o estilo e a ampliação da família de fontes usados para formatar o texto e descreve as informações de localidade.</span><span class="sxs-lookup"><span data-stu-id="46112-162">The [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface describes the font-family name, size, weight, style, and stretch used to format text, and it describes locale information.</span></span> <span data-ttu-id="46112-163">**IDWriteTextFormat** também define métodos para definir e obter as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="46112-163">**IDWriteTextFormat** also defines methods for setting and getting the following properties:</span></span>

-   <span data-ttu-id="46112-164">O espaçamento da linha.</span><span class="sxs-lookup"><span data-stu-id="46112-164">The line spacing.</span></span>
-   <span data-ttu-id="46112-165">O alinhamento do texto em relação às bordas esquerda e direita da caixa de layout.</span><span class="sxs-lookup"><span data-stu-id="46112-165">The text alignment relative to the left and right edges of the layout box.</span></span>
-   <span data-ttu-id="46112-166">O alinhamento de parágrafo em relação à parte superior e inferior da caixa de layout.</span><span class="sxs-lookup"><span data-stu-id="46112-166">The paragraph alignment relative to the top and bottom of the layout box.</span></span>
-   <span data-ttu-id="46112-167">A direção de leitura.</span><span class="sxs-lookup"><span data-stu-id="46112-167">The reading direction.</span></span>
-   <span data-ttu-id="46112-168">A granularidade de corte de texto para texto que estoura a caixa de layout.</span><span class="sxs-lookup"><span data-stu-id="46112-168">The text trimming granularity for text that overflows the layout box.</span></span>
-   <span data-ttu-id="46112-169">A parada de tabulação incremental.</span><span class="sxs-lookup"><span data-stu-id="46112-169">The incremental tab stop.</span></span>
-   <span data-ttu-id="46112-170">A direção do fluxo de parágrafo.</span><span class="sxs-lookup"><span data-stu-id="46112-170">The paragraph flow direction.</span></span>

<span data-ttu-id="46112-171">A interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) é necessária para o desenho de texto que usa os dois processos descritos neste documento.</span><span class="sxs-lookup"><span data-stu-id="46112-171">The [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is required for drawing text that uses both of the processes described in this document .</span></span>

<span data-ttu-id="46112-172">Antes de criar um objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) ou qualquer outro objeto [DirectWrite](direct-write-portal.md) , você precisa de uma instância [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="46112-172">Before you can create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, or any other [DirectWrite](direct-write-portal.md) object, you need an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) instance.</span></span> <span data-ttu-id="46112-173">Você usa um **IDWriteFactory** para criar instâncias **IDWriteTextFormat** e outros objetos DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="46112-173">You use an **IDWriteFactory** to create **IDWriteTextFormat** instances and other DirectWrite objects.</span></span> <span data-ttu-id="46112-174">Para obter uma instância de fábrica, use a função [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) .</span><span class="sxs-lookup"><span data-stu-id="46112-174">To obtain a factory instance, use the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function.</span></span>

### <a name="part-1-declare-directwrite-and-direct2d-resources"></a><span data-ttu-id="46112-175">Parte 1: declare os recursos DirectWrite e Direct2D.</span><span class="sxs-lookup"><span data-stu-id="46112-175">Part 1: Declare DirectWrite and Direct2D Resources.</span></span>

<span data-ttu-id="46112-176">Nesta parte, você declara os objetos que serão usados posteriormente para criar e exibir texto como membros de dados privados de sua classe.</span><span class="sxs-lookup"><span data-stu-id="46112-176">In this part, you declare the objects that you will use later for creating and displaying text as private data members of your class.</span></span> <span data-ttu-id="46112-177">Todas as interfaces, funções e tipos de datatipos para [DirectWrite](direct-write-portal.md) são declaradas no arquivo de cabeçalho *dwrite. h* e aquelas para [Direct2D](../direct2d/direct2d-portal.md) são declaradas no *d2d1. h*; Se você ainda não fez isso, inclua esses cabeçalhos em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="46112-177">All of the interfaces, functions, and datatypes for [DirectWrite](direct-write-portal.md) are declared in the *dwrite.h* header file, and those for [Direct2D](../direct2d/direct2d-portal.md) are declared in the *d2d1.h*; if you haven't already done this, include these headers in your project.</span></span>

1.  <span data-ttu-id="46112-178">Em seu arquivo de cabeçalho de classe (SimpleText. h), declare ponteiros para as interfaces [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) e [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) como membros privados.</span><span class="sxs-lookup"><span data-stu-id="46112-178">In your class header file (SimpleText.h), declare pointers to [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) and [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interfaces as private members.</span></span>
    ```C++
    IDWriteFactory* pDWriteFactory_;
    IDWriteTextFormat* pTextFormat_;
    
    ```

    

2.  <span data-ttu-id="46112-179">Declare membros para manter a cadeia de texto a ser renderizada e o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="46112-179">Declare members to hold the text string to render and the length of the string.</span></span>
    ```C++
    const wchar_t* wszText_;
    UINT32 cTextLength_;
    
    ```

    

3.  <span data-ttu-id="46112-180">Declare ponteiros para as interfaces [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)e [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) para renderizar o texto com [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="46112-180">Declare pointers to [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), and [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interfaces for rendering the text with [Direct2D](../direct2d/direct2d-portal.md).</span></span>
    ```C++
    ID2D1Factory* pD2DFactory_;
    ID2D1HwndRenderTarget* pRT_;
    ID2D1SolidColorBrush* pBlackBrush_;
    
    ```

    

### <a name="part-2-create-device-independent-resources"></a><span data-ttu-id="46112-181">Parte 2: criar recursos independentes de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46112-181">Part 2: Create Device Independent Resources.</span></span>

<span data-ttu-id="46112-182">O [Direct2D](rendering-by-using-direct2d.md) fornece dois tipos de recursos: recursos dependentes de dispositivo e recursos independentes de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46112-182">[Direct2D](rendering-by-using-direct2d.md) provides two types of resources: device-dependent resources and device-independent resources.</span></span> <span data-ttu-id="46112-183">Os recursos dependentes do dispositivo são associados a um dispositivo de renderização e não funcionam mais se esse dispositivo for removido.</span><span class="sxs-lookup"><span data-stu-id="46112-183">Device-dependent resources are associated with a rendering device and no longer function if that device is removed.</span></span> <span data-ttu-id="46112-184">Os recursos independentes de dispositivo, por outro lado, podem durar o escopo do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46112-184">Device-independent resources, on the other hand, can last for the scope of your application.</span></span>

<span data-ttu-id="46112-185">Os recursos do [DirectWrite](direct-write-portal.md) são independentes de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46112-185">[DirectWrite](direct-write-portal.md) resources are device-independent.</span></span>

<span data-ttu-id="46112-186">Nesta seção, você cria os recursos independentes do dispositivo que são usados pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46112-186">In this section, you create the device-independent resources that are used by your application.</span></span> <span data-ttu-id="46112-187">Esses recursos devem ser liberados com uma chamada para o método **Release** da interface.</span><span class="sxs-lookup"><span data-stu-id="46112-187">These resources must be freed with a call to the **Release** method of the interface.</span></span>

<span data-ttu-id="46112-188">Alguns dos recursos que são usados precisam ser criados apenas uma vez e não estão vinculados a um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46112-188">Some of the resources that are used have to be created only one time and are not tied to a device.</span></span> <span data-ttu-id="46112-189">A inicialização desses recursos é colocada no método *SimpleText:: CreateDeviceIndependentResources* , que é chamado ao inicializar a classe.</span><span class="sxs-lookup"><span data-stu-id="46112-189">The initialization for these resources is put in the *SimpleText::CreateDeviceIndependentResources* method, which is called when initializing the class.</span></span>

1.  <span data-ttu-id="46112-190">Dentro do método *SimpleText:: CreateDeviceIndependentResources* no arquivo de implementação de classe (SimpleText. cpp), chame a função [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) para criar uma interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , que é a interface de fábrica raiz para todos os objetos [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="46112-190">Inside the *SimpleText::CreateDeviceIndependentResources* method in the class implementation file (SimpleText.cpp), call the [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) function to create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface, which is the root factory interface for all [Direct2D](../direct2d/direct2d-portal.md) objects.</span></span> <span data-ttu-id="46112-191">Você usa a mesma fábrica para criar uma instância de outros recursos de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="46112-191">You use the same factory to instantiate other Direct2D resources.</span></span>
    ```C++
    hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &pD2DFactory_
        );
    
    ```

    

2.  <span data-ttu-id="46112-192">Chame a função [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) para criar uma interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) , que é a interface de fábrica raiz para todos os objetos [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="46112-192">Call the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function to create an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface, which is the root factory interface for all [DirectWrite](direct-write-portal.md) objects.</span></span> <span data-ttu-id="46112-193">Você usa a mesma fábrica para criar uma instância de outros recursos de DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="46112-193">You use the same factory to instantiate other DirectWrite resources.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory_)
            );
    }
    
    ```

    

3.  <span data-ttu-id="46112-194">Inicialize a cadeia de texto e armazene seu comprimento.</span><span class="sxs-lookup"><span data-stu-id="46112-194">Initialize the text string and store its length.</span></span>

    ```C++
    wszText_ = L"Hello World using  DirectWrite!";
    cTextLength_ = (UINT32) wcslen(wszText_);
    
    ```

    

4.  <span data-ttu-id="46112-195">Crie um objeto de interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) usando o método [**IDWriteFactory:: CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) .</span><span class="sxs-lookup"><span data-stu-id="46112-195">Create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface object by using the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method.</span></span> <span data-ttu-id="46112-196">O **IDWriteTextFormat** especifica a fonte, o peso, a ampliação, o estilo e a localidade que serão usados para renderizar a cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="46112-196">The **IDWriteTextFormat** specifies the font, weight, stretch, style, and locale that will be used to render the text string.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTextFormat(
            L"Gabriola",                // Font family name.
            NULL,                       // Font collection (NULL sets it to use the system font collection).
            DWRITE_FONT_WEIGHT_REGULAR,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            72.0f,
            L"en-us",
            &pTextFormat_
            );
    }
    
    ```

    

5.  <span data-ttu-id="46112-197">Centralize o texto horizontal e verticalmente chamando os métodos [**IDWriteTextFormat:: SetTextAlign**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) e [**IDWriteTextFormat:: SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) .</span><span class="sxs-lookup"><span data-stu-id="46112-197">Center the text horizontally and vertically by calling the [**IDWriteTextFormat::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) and [**IDWriteTextFormat::SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) methods.</span></span>
    ```C++
    // Center align (horizontally) the text.
    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }
    
    ```

    

<span data-ttu-id="46112-198">Nesta parte, você inicializou os recursos independentes do dispositivo que são usados pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46112-198">In this part, you initialized the device-independent resources that are used by your application.</span></span> <span data-ttu-id="46112-199">Na próxima parte, você inicializa os recursos dependentes do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46112-199">In the next part, you initialize the device-dependent resources.</span></span>

### <a name="part-3-create-device-dependent-resources"></a><span data-ttu-id="46112-200">Parte 3: criar Device-Dependent recursos.</span><span class="sxs-lookup"><span data-stu-id="46112-200">Part 3: Create Device-Dependent Resources.</span></span>

<span data-ttu-id="46112-201">Nesta parte, você cria um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) e um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) para renderizar seu texto.</span><span class="sxs-lookup"><span data-stu-id="46112-201">In this part, you create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) and an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) for rendering your text.</span></span>

<span data-ttu-id="46112-202">Um destino de renderização é um objeto Direct2D que cria recursos de desenho e renderiza comandos de desenho para um dispositivo de renderização.</span><span class="sxs-lookup"><span data-stu-id="46112-202">A render target is a Direct2D object that creates drawing resources and renders drawing commands to a rendering device.</span></span> <span data-ttu-id="46112-203">Um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) é um destino de renderização que é renderizado para um **HWND**.</span><span class="sxs-lookup"><span data-stu-id="46112-203">An [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) is a render target that renders to an **HWND**.</span></span>

<span data-ttu-id="46112-204">Um dos recursos de desenho que um destino de renderização pode criar é um pincel para contornos de pintura, preenchimentos e texto.</span><span class="sxs-lookup"><span data-stu-id="46112-204">One of the drawing resources that a render target can create is a brush for painting outlines, fills, and text.</span></span> <span data-ttu-id="46112-205">Um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pinta com uma cor sólida.</span><span class="sxs-lookup"><span data-stu-id="46112-205">An [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) paints with a solid color.</span></span>

<span data-ttu-id="46112-206">As interfaces [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) e [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) estão associadas a um dispositivo de renderização quando são criadas e devem ser liberadas e recriadas se o dispositivo se tornar inválido.</span><span class="sxs-lookup"><span data-stu-id="46112-206">Both the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) and the [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interfaces are bound to a rendering device when they are created and must be released and recreated if the device becomes invalid.</span></span>

1.  <span data-ttu-id="46112-207">Dentro do método SimpleText:: CreateDeviceResources, verifique se o ponteiro de destino de renderização é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="46112-207">Inside the SimpleText::CreateDeviceResources method, check whether the render target pointer is **NULL**.</span></span> <span data-ttu-id="46112-208">Se for, recupere o tamanho da área de renderização e crie um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) desse tamanho.</span><span class="sxs-lookup"><span data-stu-id="46112-208">If it is, retrieve the size of the render area and create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) of that size.</span></span> <span data-ttu-id="46112-209">Use o **ID2D1HwndRenderTarget** para criar um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="46112-209">Use the **ID2D1HwndRenderTarget** to create an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>
    ```C++
    RECT rc;
    GetClientRect(hwnd_, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

    if (!pRT_)
    {
        // Create a Direct2D render target.
        hr = pD2DFactory_->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(
                    hwnd_,
                    size
                    ),
                &pRT_
                );

        // Create a black brush.
        if (SUCCEEDED(hr))
        {
            hr = pRT_->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black),
                &pBlackBrush_
                );
        }
    }
    
    ```

    

2.  <span data-ttu-id="46112-210">No método SimpleText::D iscardDeviceResources, libere o pincel e o destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="46112-210">In the SimpleText::DiscardDeviceResources method, release both the brush and render target.</span></span>
    ```C++
    SafeRelease(&pRT_);
    SafeRelease(&pBlackBrush_);
    
    ```

    

<span data-ttu-id="46112-211">Agora que você criou um destino de renderização e um pincel, você pode usá-los para renderizar seu texto.</span><span class="sxs-lookup"><span data-stu-id="46112-211">Now that you have created a render target and a brush, you can use them to render your text.</span></span>

### <a name="part-4-draw-text-by-using-the-direct2d-drawtext-method"></a><span data-ttu-id="46112-212">Parte 4: desenhar texto usando o método DrawText Direct2D.</span><span class="sxs-lookup"><span data-stu-id="46112-212">Part 4: Draw Text By Using the Direct2D DrawText Method.</span></span>

1.  <span data-ttu-id="46112-213">No método SimpleText::D rawText da sua classe, defina a área para o layout de texto recuperando as dimensões da área de renderização e crie um retângulo de [Direct2D](../direct2d/direct2d-portal.md) que tenha as mesmas dimensões.</span><span class="sxs-lookup"><span data-stu-id="46112-213">In the SimpleText::DrawText method of your class, define the area for the text layout by retrieving the dimensions of the rendering area, and create a [Direct2D](../direct2d/direct2d-portal.md) rectangle that has the same dimensions.</span></span>
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  <span data-ttu-id="46112-214">Use o método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e o objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) para renderizar o texto na tela.</span><span class="sxs-lookup"><span data-stu-id="46112-214">Use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method and the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to render text to the screen.</span></span> <span data-ttu-id="46112-215">O método **ID2D1RenderTarget::D rawtext** usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="46112-215">The **ID2D1RenderTarget::DrawText** method takes the following parameters:</span></span>
    -   <span data-ttu-id="46112-216">Uma cadeia de caracteres a ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="46112-216">A string to render.</span></span>
    -   <span data-ttu-id="46112-217">Um ponteiro para uma interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) .</span><span class="sxs-lookup"><span data-stu-id="46112-217">A pointer to an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface.</span></span>
    -   <span data-ttu-id="46112-218">Um retângulo de layout [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="46112-218">A [Direct2D](../direct2d/direct2d-portal.md) layout rectangle.</span></span>
    -   <span data-ttu-id="46112-219">Um ponteiro para uma interface que expõe [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span><span class="sxs-lookup"><span data-stu-id="46112-219">A pointer to an interface that exposes [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span></span>

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

### <a name="part-5-render-the-window-contents-using-direct2d"></a><span data-ttu-id="46112-220">Parte 5: renderizar o conteúdo da janela usando Direct2D</span><span class="sxs-lookup"><span data-stu-id="46112-220">Part 5: Render the Window Contents Using Direct2D</span></span>

<span data-ttu-id="46112-221">Para renderizar o conteúdo da janela usando [Direct2D](../direct2d/direct2d-portal.md) quando uma mensagem de pintura for recebida, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="46112-221">To render the contents of the window by using [Direct2D](../direct2d/direct2d-portal.md) when a paint message is received, do the following:</span></span>

1.  <span data-ttu-id="46112-222">Crie os recursos dependentes do dispositivo chamando o método SimpleText:: CreateDeviceResources implementado na parte 3.</span><span class="sxs-lookup"><span data-stu-id="46112-222">Create the device dependent resources by calling the SimpleText::CreateDeviceResources method implemented in Part 3.</span></span>
2.  <span data-ttu-id="46112-223">Chame o método [**ID2D1HwndRenderTarget:: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) do destino render.</span><span class="sxs-lookup"><span data-stu-id="46112-223">Call the [**ID2D1HwndRenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method of the render target.</span></span>
3.  <span data-ttu-id="46112-224">Limpe o destino de renderização chamando o método [**ID2D1HwndRenderTarget:: Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) .</span><span class="sxs-lookup"><span data-stu-id="46112-224">Clear the render target by calling the [**ID2D1HwndRenderTarget::Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) method.</span></span>
4.  <span data-ttu-id="46112-225">Chame o método SimpleText::D rawText, implementado na parte 4.</span><span class="sxs-lookup"><span data-stu-id="46112-225">Call the SimpleText::DrawText method, implemented in Part 4.</span></span>
5.  <span data-ttu-id="46112-226">Chame o método [**ID2D1HwndRenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="46112-226">Call the [**ID2D1HwndRenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method of the render target.</span></span>
6.  <span data-ttu-id="46112-227">Se for necessário, descarte os recursos dependentes do dispositivo para que eles possam ser recriados quando a janela for redesenhada.</span><span class="sxs-lookup"><span data-stu-id="46112-227">If it is necessary, discard the device-dependent resources so that they can be recreated when the window is redrawn.</span></span>


```C++
hr = CreateDeviceResources();

if (SUCCEEDED(hr))
{
    pRT_->BeginDraw();

    pRT_->SetTransform(D2D1::IdentityMatrix());

    pRT_->Clear(D2D1::ColorF(D2D1::ColorF::White));

    // Call the DrawText method of this class.
    hr = DrawText();

    if (SUCCEEDED(hr))
    {
        hr = pRT_->EndDraw(
            );
    }
}

if (FAILED(hr))
{
    DiscardDeviceResources();
}

```



<span data-ttu-id="46112-228">A classe SimpleText é implementada em SimpleText. h e SimpleText. cpp.</span><span class="sxs-lookup"><span data-stu-id="46112-228">The SimpleText class is implemented in SimpleText.h and SimpleText.cpp.</span></span>

## <a name="drawing-text-with-multiple-formats"></a><span data-ttu-id="46112-229">Desenhar texto com vários formatos.</span><span class="sxs-lookup"><span data-stu-id="46112-229">Drawing Text with Multiple Formats.</span></span>

<span data-ttu-id="46112-230">Esta seção mostra como usar [DirectWrite](direct-write-portal.md) e [Direct2D](../direct2d/direct2d-portal.md) para renderizar texto com vários formatos, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="46112-230">This section shows how to use [DirectWrite](direct-write-portal.md) and [Direct2D](../direct2d/direct2d-portal.md) to render text with multiple formats, as shown in the following screen shot.</span></span>

![captura de tela de "Olá, mundo usando DirectWrite!", com algumas partes em diferentes estilos, tamanhos e formatos](images/multiformattedcropped.png)

<span data-ttu-id="46112-232">O código desta seção é implementado como a classe multiformattedtext no [exemplo DWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="46112-232">The code for this section is implemented as the MultiformattedText class in the [DWriteHelloWorld Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span> <span data-ttu-id="46112-233">Ele se baseia nas etapas da seção anterior.</span><span class="sxs-lookup"><span data-stu-id="46112-233">It is based on the steps from the previous section.</span></span>

<span data-ttu-id="46112-234">Para criar texto com vários formatos, use a interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) além da interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) introduzida na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="46112-234">To create multi-formatted text, you use the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface in addition to the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface introduced in the previous section.</span></span> <span data-ttu-id="46112-235">A interface **IDWriteTextLayout** descreve a formatação e o layout de um bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="46112-235">The **IDWriteTextLayout** interface describes the formatting and layout of a block of text.</span></span> <span data-ttu-id="46112-236">Além da formatação padrão especificada por um objeto **IDWriteTextFormat** , a formatação de intervalos específicos de texto pode ser alterada usando **IDWriteTextLayout**.</span><span class="sxs-lookup"><span data-stu-id="46112-236">In addition to default formatting specified by an **IDWriteTextFormat** object, the formatting for specific ranges of text can be changed by using **IDWriteTextLayout**.</span></span> <span data-ttu-id="46112-237">Isso inclui o nome, o tamanho, o peso, o estilo, a ampliação, o tachado e o sublinhado da família de fontes.</span><span class="sxs-lookup"><span data-stu-id="46112-237">This includes font family name, size, weight, style, stretch, strikethrough, and underlining.</span></span>

<span data-ttu-id="46112-238">O [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) também fornece métodos de teste de clique.</span><span class="sxs-lookup"><span data-stu-id="46112-238">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) also provides hit-testing methods.</span></span> <span data-ttu-id="46112-239">As métricas de teste de colisão retornadas por esses métodos são relativas à caixa de layout especificada quando o objeto de interface **IDWriteTextLayout** é criado usando o método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) da interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="46112-239">The hit-testing metrics returned by these methods are relative to the layout box specified when the **IDWriteTextLayout** interface object is created by using the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method of the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="46112-240">A interface [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) é usada para adicionar recursos de tipografia [OpenType](../intl/opentype-font-format.md) opcionais a um layout de texto, como traços violentos e conjuntos de texto estilísticos alternativos.</span><span class="sxs-lookup"><span data-stu-id="46112-240">The [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) interface is used to add optional [OpenType](../intl/opentype-font-format.md) typographic features to a text layout, such as swashes and alternative stylistic text sets.</span></span> <span data-ttu-id="46112-241">Recursos tipográficos podem ser adicionados a um intervalo específico de texto dentro de um layout de texto chamando o método [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) da interface **IDWriteTypography** .</span><span class="sxs-lookup"><span data-stu-id="46112-241">Typographic features can be added to a specific range of text within a text layout by calling the [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) method of the **IDWriteTypography** interface.</span></span> <span data-ttu-id="46112-242">Esse método recebe uma estrutura de [**\_ \_ recursos de fonte DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) como um parâmetro que contém uma constante de enumeração de **marca de \_ \_ recurso \_ de fonte DWRITE** e um parâmetro de execução **UINT32** .</span><span class="sxs-lookup"><span data-stu-id="46112-242">This method receives a [**DWRITE\_FONT\_FEATURE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) structure as a parameter that contains a **DWRITE\_FONT\_FEATURE\_TAG** enumeration constant and a **UINT32** execution parameter.</span></span> <span data-ttu-id="46112-243">Uma lista de recursos OpenType registrados pode ser encontrada no [registro de marca de layout OpenType](https://www.microsoft.com/typography/otspec/features_ae.htm) em Microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="46112-243">A list of registered OpenType features can be found at the [OpenType Layout Tag Registry](https://www.microsoft.com/typography/otspec/features_ae.htm) on microsoft.com.</span></span> <span data-ttu-id="46112-244">Para obter as constantes de enumeração DirectWrite equivalentes, consulte **\_ marca de \_ recurso \_ de fonte DWRITE**.</span><span class="sxs-lookup"><span data-stu-id="46112-244">For the equivalent DirectWrite enumeration constants, see **DWRITE\_FONT\_FEATURE\_TAG**.</span></span>

### <a name="part-1-create-an-idwritetextlayout-interface"></a><span data-ttu-id="46112-245">Parte 1: criar uma interface IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="46112-245">Part 1: Create an IDWriteTextLayout Interface.</span></span>

1.  <span data-ttu-id="46112-246">Declare um ponteiro para uma interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como membro da classe multiformattedtext.</span><span class="sxs-lookup"><span data-stu-id="46112-246">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the MultiformattedText class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="46112-247">No final do método multiformattedtext:: CreateDeviceIndependentResources, crie um objeto de interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chamando o método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="46112-247">At the end of the MultiformattedText::CreateDeviceIndependentResources method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span> <span data-ttu-id="46112-248">A interface **IDWriteTextLayout** fornece recursos de formatação adicionais, como a capacidade de aplicar formatos diferentes a partes selecionadas de texto.</span><span class="sxs-lookup"><span data-stu-id="46112-248">The **IDWriteTextLayout** interface provides additional formatting features, such as the ability to apply different formats to selected portions of text.</span></span>
    ```C++
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    
    ```

    

### <a name="part-2-applying-formatting-with-idwritetextlayout"></a><span data-ttu-id="46112-249">Parte 2: aplicando a formatação com IDWriteTextLayout.</span><span class="sxs-lookup"><span data-stu-id="46112-249">Part 2: Applying Formatting with IDWriteTextLayout.</span></span>

<span data-ttu-id="46112-250">A formatação, como o tamanho da fonte, o peso e o sublinhado, pode ser aplicada a subcadeias de texto a serem exibidas usando a interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="46112-250">Formatting, such as the font size, weight, and underlining, can be applied to substrings of the text to be displayed by using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

1.  <span data-ttu-id="46112-251">Defina o tamanho da fonte para a subcadeia de caracteres "di" de "DirectWrite" como 100, declarando um [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) e chamando o método [**IDWriteTextLayout:: setfonts**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) .</span><span class="sxs-lookup"><span data-stu-id="46112-251">Set the font size for the substring "Di" of "DirectWrite" to 100 by declaring a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) and calling the [**IDWriteTextLayout::SetFontSize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) method.</span></span>
    ```C++
    // Format the "DirectWrite" substring to be of font size 100.
    if (SUCCEEDED(hr))
    {
        DWRITE_TEXT_RANGE textRange = {20,        // Start index where "DirectWrite" appears.
                                        6 };      // Length of the substring "Direct" in "DirectWrite".
        hr = pTextLayout_->SetFontSize(100.0f, textRange);
    }
    ```

    

2.  <span data-ttu-id="46112-252">Sublinhar a subcadeia de caracteres "DirectWrite" chamando o método [**IDWriteTextLayout::**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) ondele.</span><span class="sxs-lookup"><span data-stu-id="46112-252">Underline the substring "DirectWrite" by calling the [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) method.</span></span>
    ```C++
    // Format the word "DWrite" to be underlined.
    if (SUCCEEDED(hr))
    {
        
        DWRITE_TEXT_RANGE textRange = {20,      // Start index where "DirectWrite" appears.
                                       11 };    // Length of the substring "DirectWrite".
        hr = pTextLayout_->SetUnderline(TRUE, textRange);
    }
    ```

    

3.  <span data-ttu-id="46112-253">Defina a espessura da fonte como negrito para a subcadeia de caracteres "DirectWrite" chamando o método [**IDWriteTextLayout:: setespessuradafonte**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) .</span><span class="sxs-lookup"><span data-stu-id="46112-253">Set the font weight to bold for the substring "DirectWrite" by calling the [**IDWriteTextLayout::SetFontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) method.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        // Format the word "DWrite" to be bold.
        DWRITE_TEXT_RANGE textRange = {20,
                                       11 };
        hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
    }
    ```

    

### <a name="part-3-adding-typographic-features-with-idwritetypography"></a><span data-ttu-id="46112-254">Parte 3: adicionando recursos tipográficos com IDWriteTypography.</span><span class="sxs-lookup"><span data-stu-id="46112-254">Part 3: Adding Typographic Features with IDWriteTypography.</span></span>

1.  <span data-ttu-id="46112-255">Declare e crie um objeto de interface [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) chamando o método [**IDWriteFactory:: createtypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) .</span><span class="sxs-lookup"><span data-stu-id="46112-255">Declare and create an [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) interface object by calling the [**IDWriteFactory::CreateTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) method.</span></span>
    ```C++
    // Declare a typography pointer.
    IDWriteTypography* pTypography = NULL;

    // Create a typography interface object.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTypography(&pTypography);
    }
    
    ```

    

2.  <span data-ttu-id="46112-256">Adicione um recurso de fonte declarando um objeto de [**\_ \_ recurso de fonte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) que tem o conjunto estilístico 7 especificado e chamando o método [**IDWriteTypography:: AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) .</span><span class="sxs-lookup"><span data-stu-id="46112-256">Add a font feature by declaring a [**DWRITE\_FONT\_FEATURE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) object that has the stylistic set 7 specified and calling the [**IDWriteTypography::AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) method.</span></span>
    ```C++
    // Set the stylistic set.
    DWRITE_FONT_FEATURE fontFeature = {DWRITE_FONT_FEATURE_TAG_STYLISTIC_SET_7,
                                       1};
    if (SUCCEEDED(hr))
    {
        hr = pTypography->AddFontFeature(fontFeature);
    }
    
    ```

    

3.  <span data-ttu-id="46112-257">Defina o layout de texto para usar a tipografia sobre a cadeia de caracteres inteira declarando uma variável de [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) e chamando o método [**IDWriteTextLayout:: settypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) e passando o intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="46112-257">Set the text layout to use the typography over the whole string by declaring a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) variable and calling the [**IDWriteTextLayout::SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) method and passing in the text range.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        // Set the typography for the entire string.
        DWRITE_TEXT_RANGE textRange = {0,
                                       cTextLength_};
        hr = pTextLayout_->SetTypography(pTypography, textRange);
    }
    
    ```

    

4.  <span data-ttu-id="46112-258">Defina a nova largura e a altura do objeto de layout de texto no método multiformattedtext:: OnResize.</span><span class="sxs-lookup"><span data-stu-id="46112-258">Set the new width and height for the text layout object in the MultiformattedText::OnResize method.</span></span>
    ```C++
    if (pTextLayout_)
    {
        pTextLayout_->SetMaxWidth(static_cast<FLOAT>(width / dpiScaleX_));
        pTextLayout_->SetMaxHeight(static_cast<FLOAT>(height / dpiScaleY_));
    }
    ```

    

### <a name="part-4-draw-text-using-the-direct2d-drawtextlayout-method"></a><span data-ttu-id="46112-259">Parte 4: desenhar texto usando o método Direct2D DrawTextLayout.</span><span class="sxs-lookup"><span data-stu-id="46112-259">Part 4: Draw Text Using the Direct2D DrawTextLayout Method.</span></span>

<span data-ttu-id="46112-260">Para desenhar o texto com as configurações de layout de texto especificadas pelo objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , altere o código no método multiformattedtext::D rawtext para usar [**IDWriteTextLayout::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span><span class="sxs-lookup"><span data-stu-id="46112-260">To draw the text with the text layout settings specified by the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, change the code in the MultiformattedText::DrawText method to use [**IDWriteTextLayout::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span></span>

1.  <span data-ttu-id="46112-261">Delcare uma variável de [**d2d1 do \_ ponto \_ 2F**](../direct2d/d2d1-point-2f.md) e defina-a como o ponto superior esquerdo da janela.</span><span class="sxs-lookup"><span data-stu-id="46112-261">Delcare a [**D2D1\_POINT\_2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.</span></span>
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  <span data-ttu-id="46112-262">Desenhe o texto na tela chamando o método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) do destino de renderização [Direct2D](../direct2d/direct2d-portal.md) e passando o ponteiro [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="46112-262">Draw the text to the screen by calling the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method of the [Direct2D](../direct2d/direct2d-portal.md) render target and passing the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pointer.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

<span data-ttu-id="46112-263">A classe multiformattedtext é implementada em multiformattedtext. h e multiformattedtext. cpp.</span><span class="sxs-lookup"><span data-stu-id="46112-263">The MultiformattedText class is implemented in MultiformattedText.h and MultiformattedText.cpp.</span></span>

 

 