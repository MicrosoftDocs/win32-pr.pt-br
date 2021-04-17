---
title: Melhorando o desempenho de aplicativos Direct2D
description: Descreve as técnicas para melhorar o desempenho do Direct2D.
ms.assetid: e6b02925-4e75-42b0-b0c4-00f1ddb85e46
keywords:
- Direct2D, desempenho
- Direct2D, bitmaps
- Direct2D, uso de recursos
- Direct2D, método Flush
- Direct2D, conteúdo estático
- desempenho para Direct2D
- bitmaps para Direct2D
- Interoperação Direct2D, GDI
- Direct2D, interoperabilidade
- interoperabilidade, Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interoperabilidade, Graphics Device Interface (GDI)
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5a413b96e00514b64b3cf1b1ee451a84a9e9ff09
ms.sourcegitcommit: 6eb53540b8d882fd035d428567d7d1c5ec17042c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/12/2020
ms.locfileid: "104454436"
---
# <a name="improving-the-performance-of-direct2d-apps"></a>Melhorando o desempenho de aplicativos Direct2D

Embora o [Direct2D](./direct2d-portal.md) seja acelerado por hardware e seja destinado a alto desempenho, você deve usar os recursos corretamente para maximizar a taxa de transferência. As técnicas que mostramos aqui são derivadas de estudar cenários comuns e podem não se aplicar a todos os cenários de aplicativo. Portanto, uma compreensão cuidadosa do comportamento do aplicativo e das metas de desempenho pode ajudar a atingir os resultados desejados.

-   [Uso de recursos](#resource-usage)
    -   [Reutilizar recursos](#reuse-resources)
-   [Restringir o uso de flush](#restrict-the-use-of-flush)
-   [Bitmaps](#create-large-bitmaps)
    -   [Criar bitmaps grandes](#create-large-bitmaps)
    -   [Criar um Atlas de bitmaps](#create-an-atlas-of-bitmaps)
    -   [Criar bitmaps compartilhados](#create-shared-bitmaps)
    -   [Copiando bitmaps](#copying-bitmaps)
-   [Usar bitmap em ladrilhos sobre tracejado](#use-tiled-bitmap-over-dashing)
-   [Diretrizes gerais para a renderização de conteúdo estático complexo](#general-guidelines-for-rendering-complex-static-content)
    -   [Cache de cena completa usando um bitmap de cor](#full-scene-caching-using-a-color-bitmap)
    -   [Por cache primitivo usando um bitmap A8 e o método FillOpacityMask](#per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method)
-   [Cache por primitivo usando a realização de geometria](#per-primitive-caching-using-geometry-realizations)
-   [Renderização de geometria](#geometry-rendering)
    -   [Usar primitiva de desenho específico sobre geometria de desenho](#use-specific-draw-primitive-over-draw-geometry)
    -   [Renderizando geometria estática](#rendering-static-geometry)
    -   [Usar um contexto de dispositivo multithread](#use-a-multithreaded-device-context)
-   [Desenho de texto com Direct2D](#use-a-multithreaded-device-context)
    -   [DrawTextLayout versus DrawText](#drawtextlayout-vs-drawtext)
    -   [Escolhendo o modo de renderização de texto correto](#choosing-the-right-text-rendering-mode)
    -   [Cache](#full-scene-caching-using-a-color-bitmap)
-   [Recortando uma forma arbitrária](#clipping-an-arbitrary-shape)
    -   [PushLayer no Windows 8](#pushlayer-in-windows-8)
    -   [Clipes alinhados por eixo](#axis-aligned-clips)
-   [Interoperabilidade de DXGI: Evite comutadores frequentes](#dxgi-interoperability-avoid-frequent-switches)
-   [Saber seu formato de pixel](#know-your-pixel-format)
-   [Complexidade da cena](#scene-complexity)
    -   [Entender a complexidade da cena](#understand-scene-complexity)
-   [Melhorando o desempenho para aplicativos de impressão Direct2D](#improving-performance-for-direct2d-printing-apps)
    -   [Definir os valores de propriedade corretos ao criar o controle de impressão D2D](#set-the-right-property-values-when-you-create-the-d2d-print-control)
    -   [Evite usar determinados padrões de desenho Direct2D](#avoid-using-certain-direct2d-drawing-patterns)
    -   [Desenhar texto de maneira direta e simples](#draw-text-in-a-direct-and-plain-way)
    -   [Desenhe os bitmaps originais quando possível](#draw-the-original-bitmaps-when-possible)
-   [Conclusão](#conclusion)

## <a name="resource-usage"></a>Uso de recursos

Um recurso é uma alocação de algum tipo, seja na memória de vídeo ou do sistema. Bitmaps e pincéis são exemplos de recursos.

No Direct2D, os recursos podem ser criados em software e hardware. A criação e a exclusão de recursos no hardware são operações caras porque exigem muita sobrecarga para a comunicação com a placa de vídeo. Vamos ver como o Direct2D renderiza o conteúdo para um destino.

No Direct2D, todos os comandos de renderização são colocados entre uma chamada para [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e uma chamada para [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw). Essas chamadas são feitas para um destino de renderização. Você deve chamar o método **BeginDraw** antes de chamar as operações de renderização. Depois de chamar **BeginDraw** , um contexto normalmente cria um lote de comandos de renderização, mas atrasa o processamento desses comandos até que uma dessas instruções seja verdadeira:

-   [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ocorreu. Quando **EndDraw** é chamado, ele faz com que todas as operações de desenho em lote sejam concluídas e retorna o status da operação.
-   Você faz uma chamada explícita para [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush): o método **flush** faz com que o lote seja processado e todos os comandos pendentes sejam emitidos.
-   O buffer que contém os comandos de renderização está cheio. Se esse buffer ficar cheio antes que as duas condições anteriores sejam atendidas, os comandos de renderização serão liberados.

Até que os primitivos sejam liberados, o Direct2D mantém referências internas a recursos correspondentes, como bitmaps e pincéis.

### <a name="reuse-resources"></a>Reutilizar recursos

Como já mencionado, a criação e a exclusão de recursos são caras no hardware. Portanto, reutilize os recursos quando possível. Veja o exemplo de criação de bitmap no desenvolvimento de jogos. Normalmente, os bitmaps que compõem uma cena em um jogo são todos criados ao mesmo tempo com todas as diferentes variações necessárias para renderização de quadro a quadro posterior. No momento da renderização real da cena e da rerenderização, esses bitmaps são reutilizados em vez de recriados.

> [!Note]  
> Não é possível reutilizar recursos para a operação de redimensionamento de janela. Quando uma janela é redimensionada, alguns recursos dependentes de escala, como destinos de renderização compatíveis e, possivelmente, alguns recursos de camada devem ser recriados porque o conteúdo da janela deve ser redesenhado. Isso pode ser importante para manter a qualidade geral da cena renderizada.

 

## <a name="restrict-the-use-of-flush"></a>Restringir o uso de flush

Como o método [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) faz com que os comandos de renderização em lote sejam processados, recomendamos que você não o use. Para cenários mais comuns, deixe o gerenciamento de recursos para Direct2D.

## <a name="bitmaps"></a>Bitmaps

Como mencionado anteriormente, a criação e a exclusão de recursos são operações muito caras no hardware. Um bitmap é um tipo de recurso que é usado com frequência. A criação de bitmaps na placa de vídeo é cara. Reusá-los pode ajudar a tornar o aplicativo mais rápido.

### <a name="create-large-bitmaps"></a>Criar bitmaps grandes

As placas de vídeo normalmente têm um tamanho mínimo de alocação de memória. Se for solicitada uma alocação que seja menor do que isso, um recurso desse tamanho mínimo será alocado e a memória excedente será desperdiçada e não estará disponível para outras coisas. Se você precisar de muitos bitmaps pequenos, uma técnica melhor é alocar um bitmap grande e armazenar todo o conteúdo de bitmap pequeno nesse bitmap grande. Em seguida, subáreas do bitmap maior podem ser lidas onde são necessários os bitmaps menores. Geralmente, você deve incluir o preenchimento (pixels pretos transparentes) entre os bitmaps pequenos para evitar qualquer interação entre as imagens menores durante as operações. Isso também é conhecido como *Atlas* e tem a vantagem de reduzir a sobrecarga de criação de bitmap e o desperdício de memória de pequenas alocações de bitmap. Recomendamos que você mantenha a maioria dos bitmaps em pelo menos 64 KB e limite o número de bitmaps menores que 4 KB.

### <a name="create-an-atlas-of-bitmaps"></a>Criar um Atlas de bitmaps

Há alguns cenários comuns para os quais um bitmap do Atlas pode fornecer muito bem. Os bitmaps pequenos podem ser armazenados dentro de um bitmap grande. Esses pequenos bitmaps podem ser extraídos do bitmap maior quando você precisar deles, especificando o retângulo de destino. Por exemplo, um aplicativo tem que desenhar vários ícones. Todos os bitmaps associados aos ícones podem ser carregados em um bitmap grande com antecedência. E, no momento da renderização, eles podem ser recuperados do bitmap grande.

> [!Note]  
> Um bitmap Direct2D criado na memória de vídeo é limitado ao tamanho máximo de bitmap com suporte pelo adaptador no qual ele está armazenado. A criação de um bitmap maior do que isso pode resultar em um erro.

 

> [!Note]  
> A partir do Windows 8, o Direct2D inclui um [efeito do Atlas](atlas.md) que pode facilitar esse processo.

 

### <a name="create-shared-bitmaps"></a>Criar bitmaps compartilhados

A criação de bitmaps compartilhados permite que chamadores avançados criem objetos de bitmap Direct2D que são apoiados diretamente por um objeto existente, já compatível com o destino de renderização. Isso evita a criação de várias superfícies e ajuda a reduzir a sobrecarga de desempenho.

> [!Note]  
> Os bitmaps compartilhados geralmente são limitados a destinos de software ou a destinos interoperáveis com DXGI. Use os métodos [**CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)), [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))e [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para criar bitmaps compartilhados.

 

### <a name="copying-bitmaps"></a>Copiando bitmaps

A criação de uma superfície DXGI é uma operação cara, portanto, reutilizar superfícies existentes quando possível. Mesmo no software, se um bitmap estiver principalmente no formato desejado, exceto por uma pequena parte, será melhor atualizar essa parte do que lançar todo o bitmap e recriar tudo. Embora você possa usar o [**CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) para obter os mesmos resultados, a renderização geralmente é uma operação muito mais cara do que a cópia. Isso ocorre porque, para melhorar a localidade do cache, o hardware não armazena de fato um bitmap na mesma ordem de memória que o bitmap é endereçado. Em vez disso, o bitmap pode ser swizzled. O swizzling é ocultado da CPU pelo driver (que é lento e usado apenas em partes de extremidade inferior) ou pelo Gerenciador de memória na GPU. Devido a restrições de como os dados são gravados em um destino de renderização durante a renderização, os destinos de renderização normalmente não são swizzled ou swizzled de forma que seja menos ideal do que pode ser obtido se você souber que nunca precisará renderizar para a superfície. Portanto, os métodos [CopyFrom](/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap) \* são fornecidos para copiar retângulos de uma origem para o bitmap Direct2D.

CopyFrom pode ser usado em qualquer uma de suas três formas:

-   [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)
-   [**CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)

## <a name="use-tiled-bitmap-over-dashing"></a>Usar bitmap em ladrilhos sobre tracejado

A renderização de uma linha tracejada é uma operação muito cara devido à alta qualidade e à precisão do algoritmo subjacente. Para a maioria dos casos que não envolvem geometrias de rectilinear, o mesmo efeito pode ser gerado mais rapidamente com o uso de bitmaps em ladrilhos.

## <a name="general-guidelines-for-rendering-complex-static-content"></a>Diretrizes gerais para a renderização de conteúdo estático complexo

Armazenar o conteúdo em cache se você renderizar o mesmo quadro de conteúdo ao longo do quadro, especialmente quando a cena for complexa.

Há três técnicas de cache que você pode usar:

-   Cache de cena completa usando um bitmap de cor.
-   Por cache primitivo usando um bitmap A8 e o método [**FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) .
-   Cache por primitivo usando a realização de geometria.

Vamos examinar cada um deles mais detalhadamente.

### <a name="full-scene-caching-using-a-color-bitmap"></a>Cache de cena completa usando um bitmap de cor

Ao renderizar conteúdo estático, em cenários como animação, crie outro bitmap de cor completa em vez de gravar diretamente no bitmap da tela. Salve o destino atual, defina o destino para o bitmap intermediário e processe o conteúdo estático. Em seguida, volte para o bitmap da tela original e desenhe o bitmap intermediário nele.

Veja um exemplo:


```C++
// Create a bitmap.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_B8G8R8A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &sceneBitmap);

// Preserve the pre-existing target.
ComPtr<ID2D1Image> oldTarget;
m_d2dContext->GetTarget(&oldTarget);

// Render static content to the sceneBitmap.
m_d2dContext->SetTarget(sceneBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Render sceneBitmap to oldTarget.
m_d2dContext->SetTarget(oldTarget.Get());
m_d2dContext->DrawBitmap(sceneBitmap.Get());
```



Este exemplo usa bitmaps intermediários para armazenar em cache e alterna o bitmap ao qual o contexto do dispositivo aponta quando ele é renderizado. Isso evita a necessidade de criar um destino de renderização compatível com a mesma finalidade.

### <a name="per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method"></a>Por cache primitivo usando um bitmap A8 e o método FillOpacityMask

Quando a cena completa não é estática, mas consiste em elementos como geometry ou text estáticos, você pode usar uma técnica de cache por primitiva. Essa técnica preserva as características de suavização do primitivo que está sendo armazenado em cache e funciona com a alteração dos tipos de pincel. Ele usa um bitmap A8 em que A8 é um tipo de formato de pixel que representa um canal alfa com 8 bits. Os bitmaps A8 são úteis para desenhar geometria/texto como uma máscara. Quando você deve manipular a opacidade de conteúdo estático, em vez de manipular o próprio conteúdo, você pode traduzir, girar, distorcer ou dimensionar a opacidade da máscara.

Veja um exemplo:


```C++
// Create an opacity bitmap.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

// Preserve the pre-existing target.
ComPtr<ID2D1Image> oldTarget;
m_d2dContext->GetTarget(&oldTarget);

// Render to the opacityBitmap.
m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Call the FillOpacityMask method
// Note: for this call to work correctly the anti alias mode must be D2D1_ANTIALIAS_MODE_ALIASED. 
m_d2dContext->SetTarget(oldTarget.Get());
m_d2dContext->FillOpacityMask(
    opacityBitmap.Get(),
    m_contentBrush().Get(),
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS);
```



## <a name="per-primitive-caching-using-geometry-realizations"></a>Cache por primitivo usando a realização de geometria

Outra técnica de cache por primitivo, chamada de realização de geometria, oferece maior flexibilidade ao lidar com a geometria. Quando você deseja desenhar repetidamente geometrias com alias ou com alias, é mais rápido convertê-las em realizações de geometria e desenhar repetidamente as realizações do que é para desenhar repetidamente as geometrias. As realizações de geometria também geralmente consomem menos memória que as máscaras de opacidade (especialmente para geometrias grandes) e são menos sensíveis a alterações em escala. Para obter mais informações, consulte [visão geral de realização de geometria](geometry-realizations-overview.md).

Veja um exemplo:


```C++
    // Compute a flattening tolerance based on the scales at which the realization will be used.
    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(...);

    ComPtr<ID2D1GeometryRealization> geometryRealization;

    // Create realization of the filled interior of the geometry.
    m_d2dDeviceContext1->CreateFilledGeometryRealization(
        geometry.Get(),
        flatteningTolerance,
        &geometryRealization
        );

    // In your app's rendering code, draw the geometry realization with a brush.
    m_d2dDeviceContext1->BeginDraw();
    m_d2dDeviceContext1->DrawGeometryRealization(
        geometryRealization.Get(),
        m_brush.Get()
        );
    m_d2dDeviceContext1->EndDraw();
```



## <a name="geometry-rendering"></a>Renderização de geometria

### <a name="use-specific-draw-primitive-over-draw-geometry"></a>Usar primitiva de desenho específico sobre geometria de desenho

Use chamadas *primitivas* de desenho mais específicas, como [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) sobre chamadas [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) genéricas. Isso ocorre porque, com **DrawRectangle**, a geometria já é conhecida e, portanto, o processamento é mais rápido.

### <a name="rendering-static-geometry"></a>Renderizando geometria estática

Em cenários em que a geometria é estática, use as técnicas de cache por primitivo explicadas acima. As máscaras de opacidade e as realizações de geometria podem melhorar muito a velocidade de renderização de cenas que contêm geometria estática.

### <a name="use-a-multithreaded-device-context"></a>Usar um contexto de dispositivo multithread

Os aplicativos que esperam renderizar quantidades significativas de conteúdo geométrico complexo devem considerar especificar as [**Opções de contexto de dispositivo d2d1 habilitar sinalizador de \_ \_ \_ \_ \_ \_ \_ otimizações de vários threads**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_device_context_options) ao criar um contexto de dispositivo [Direct2D](./direct2d-portal.md) . Quando esse sinalizador for especificado, o Direct2D distribuirá a renderização em todos os núcleos lógicos presentes no sistema, o que pode reduzir significativamente o tempo de renderização geral.

Observações:

-   A partir de Windows 8.1, esse sinalizador afeta apenas a renderização de geometria de caminho. Ele não tem impacto sobre os bastidores que contêm apenas outros tipos primitivos (como texto, bitmaps ou realizações de geometria).
-   Esse sinalizador também não tem impacto ao renderizar no software (ou seja, ao renderizar com um dispositivo Direct3D detorcedor). Para controlar multithreading de software, os chamadores devem usar \_ o \_ sinalizador D3D11 criar dispositivo \_ impedir \_ \_ otimizações internas de Threading \_ ao criar o dispositivo Direct3D de detorção.
-   A especificação desse sinalizador pode aumentar o conjunto de trabalho de pico durante a renderização e também pode aumentar a contenção de thread em aplicativos que já aproveitam o processamento multi-threaded.

## <a name="drawing-text-with-direct2d"></a>Desenho de texto com Direct2D

A funcionalidade de renderização de texto Direct2D é oferecida em duas partes. A primeira parte, exposta como o método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) e [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , permite que um chamador passe uma cadeia de caracteres e parâmetros de formatação ou um objeto de layout de texto DWrite para vários formatos. Isso deve ser adequado para a maioria dos chamadores. A segunda maneira de renderizar texto, exposto como o método [**ID2D1RenderTarget::D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) , fornece rasterização para clientes que já conhecem a posição dos glifos que desejam renderizar. As duas regras gerais a seguir podem ajudar a melhorar o desempenho de texto ao desenhar em Direct2D.

### <a name="drawtextlayout-vs-drawtext"></a>DrawTextLayout versus DrawText

Tanto o [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) quanto o [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) permitem que um aplicativo processe facilmente o texto formatado pela API do [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) . **DrawTextLayout** desenha um objeto [**DWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) existente para o [**renderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)e **DrawText** constrói um layout DirectWrite para o chamador, com base nos parâmetros que são passados. Se o mesmo texto tiver que ser renderizado várias vezes, use **DrawTextLayout** em vez de **DrawText**, pois o **DrawText** cria um layout toda vez que ele é chamado.

### <a name="choosing-the-right-text-rendering-mode"></a>Escolhendo o modo de renderização de texto correto

Defina o modo de suavização de texto como [**\_ \_ modo AntiAlias de texto d2d1 em \_ escala de \_ cinza**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) explicitamente. A qualidade do processamento de texto em escala de cinza é comparável ao ClearType, mas é muito mais rápida.

### <a name="caching"></a>Cache

Use a cena completa ou o cache de bitmap por primitiva, como com o desenho de outros primitivos.

## <a name="clipping-an-arbitrary-shape"></a>Recortando uma forma arbitrária

A figura aqui mostra o resultado da aplicação de um clipe a uma imagem.

![uma imagem que mostra um exemplo de uma imagem antes e depois de um clipe.](images/clip.png)

Você pode obter esse resultado usando camadas com uma máscara de geometria ou o método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) com um pincel de opacidade.

Aqui está um exemplo que usa uma camada:


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



Aqui está um exemplo que usa o método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) :


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



Neste exemplo de código, ao chamar o método PushLayer, você não passa uma camada de aplicativo criado. O Direct2D cria uma camada para você. O Direct2D é capaz de gerenciar a alocação e a destruição desse recurso sem qualquer envolvimento do aplicativo. Isso permite que o Direct2D reutilize as camadas internamente e aplique otimizações de gerenciamento de recursos.

No Windows 8, muitas otimizações foram feitas no uso de camadas e recomendamos que você tente usar APIs de camada em vez de [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) sempre que possível.

### <a name="pushlayer-in-windows-8"></a>PushLayer no Windows 8

A interface [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) é derivada da interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) e é a chave para exibir o conteúdo de Direct2D no Windows 8, para obter mais informações sobre essa interface, confira [dispositivos e contextos de dispositivo](devices-and-device-contexts.md). Com a interface de contexto do dispositivo, você pode ignorar a chamada do método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) e, em seguida, passar NULL para o método [**ID2D1DeviceContext::P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) . O Direct2D gerencia automaticamente o recurso de camada e pode compartilhar recursos entre camadas e grafos de efeitos.

### <a name="axis-aligned-clips"></a>Clipes alinhados por eixo

Se a região a ser recortada estiver alinhada ao eixo da superfície de desenho, em vez de arbitrária. Esse caso é adequado para usar um retângulo de clipe em vez de uma camada. O lucro de desempenho é mais para geometria com alias do que a geometria de suavização de serrilhado. Para obter mais informações sobre clipes alinhados por eixo, consulte o tópico [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .

## <a name="dxgi-interoperability-avoid-frequent-switches"></a>Interoperabilidade de DXGI: Evite comutadores frequentes

O Direct2D pode interoperar diretamente com superfícies do Direct3D. Isso é muito útil para a criação de aplicativos que renderizam uma mistura de conteúdo 2D e 3D. Mas cada comutador entre o Direct2D de desenho e o conteúdo do Direct3D afeta o desempenho.

Ao renderizar para uma superfície DXGI, o Direct2D salva o estado dos dispositivos Direct3D durante a renderização e a restaura quando a renderização é concluída. Sempre que um lote de processamento Direct2D é concluído, o custo desse salvamento e restauração e o custo da liberação de todas as operações de 2D são pagos e, ainda assim, o dispositivo Direct3D não é liberado. Portanto, para aumentar o desempenho, limite o número de comutadores de renderização entre Direct2D e Direct3D.

## <a name="know-your-pixel-format"></a>Saber seu formato de pixel

Ao criar um destino de renderização, você pode usar a estrutura de [**\_ \_ formato de pixel d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) especificar o formato de pixel e o modo alfa usados pelo destino de renderização. Um canal alfa faz parte do formato de pixel que especifica o valor de cobertura ou as informações de opacidade. Se um destino de renderização não usar o canal alfa, ele deverá ser criado usando o modo alfa do [**d2d1, \_ \_ \_ ignore**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) a. Isso poupa o tempo gasto na renderização de um canal alfa que não é necessário.

Para obter mais informações sobre formatos de pixel e modos alfa, consulte [supported pixel formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).

## <a name="scene-complexity"></a>Complexidade da cena

Ao analisar os pontos de acesso de desempenho em uma cena que será renderizada, saber se a cena é associada à taxa de preenchimento ou se a associação de vértice pode fornecer informações úteis.

-   Taxa de preenchimento: a taxa de preenchimento refere-se ao número de pixels que uma placa gráfica pode renderizar e gravar na memória de vídeo por segundo.
-   Vértice associado: uma cena é associada ao vértice quando ele contém uma grande geometria complexa.

### <a name="understand-scene-complexity"></a>Entender a complexidade da cena

Você pode analisar a complexidade da sua cena alterando o tamanho do destino de renderização. Se os ganhos de desempenho estiverem visíveis para uma redução proporcional no tamanho do destino de renderização, o aplicativo será associado à taxa de preenchimento. Caso contrário, a complexidade da cena é o afunilamento de desempenho.

Quando uma cena é associada à taxa de preenchimento, reduzir o tamanho do destino de renderização pode melhorar o desempenho. Isso ocorre porque o número de pixels a serem renderizados será reduzido proporcionalmente com o tamanho do destino de renderização.

Quando uma cena é associada ao vértice, reduza a complexidade da geometria. Mas lembre-se de que isso é feito às custas da qualidade da imagem. Portanto, uma decisão de compensação cuidadosa deve ser feita entre a qualidade desejada e o desempenho necessário.

## <a name="improving-performance-for-direct2d-printing-apps"></a>Melhorando o desempenho para aplicativos de impressão Direct2D

O [Direct2D](./direct2d-portal.md) oferece compatibilidade com a impressão. Você pode enviar os mesmos comandos de desenho Direct2D (na forma de listas de comandos Direct2D) para o controle de impressão Direct2D para impressão, se você não souber quais dispositivos você está desenhando ou como o desenho é traduzido para impressão.

Você pode ajustar ainda mais o uso do controle de impressão [Direct2D](./direct2d-portal.md) e seus comandos de desenho Direct2D para fornecer resultados de impressão com melhor desempenho.

O controle de impressão de [Direct2D](./direct2d-portal.md) gera mensagens de depuração quando vê um padrão de código Direct2D que leva a uma qualidade de impressão ou desempenho mais baixo (como os padrões de código listados posteriormente neste tópico) para lembrá-lo de onde você pode evitar problemas de desempenho. Para ver essas mensagens de depuração, você precisa habilitar a [camada de depuração Direct2D](direct2ddebuglayer-portal.md) em seu código. Consulte [depurar mensagens](direct2ddebuglayer-debugmessages.md) para obter instruções para habilitar a saída da mensagem de depuração.

### <a name="set-the-right-property-values-when-you-create-the-d2d-print-control"></a>Definir os valores de propriedade corretos ao criar o controle de impressão D2D

Há três propriedades que você pode definir ao criar o controle de impressão [Direct2D](./direct2d-portal.md) . Duas dessas propriedades afetam como o controle de impressão Direct2D lida com determinados comandos Direct2D e, por sua vez, impacta o desempenho geral.

-   Modo de subconjunto de fontes: o controle de impressão [Direct2D](./direct2d-portal.md) subdefine os recursos de fonte usados em cada página antes de enviar a página a ser impressa. Esse modo reduz o tamanho dos recursos de página necessários para a impressão. Dependendo do uso da fonte na página, você pode escolher diferentes modos de subconjuntos de fontes para obter o melhor desempenho.
    -   [**D2d1 \_ O \_ modo de subconjunto de fontes de impressão \_ \_ \_ padrão**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) fornece o melhor desempenho de impressão na maioria dos casos. Quando definido para esse modo, o controle de impressão [Direct2D](./direct2d-portal.md) usa uma estratégia heurística para decidir quando subagrupar as fontes.
    -   Para trabalhos de impressão curtos com 1 ou 2 páginas, recomendamos o [**\_ modo de \_ subconjunto de fontes de impressão d2d1 \_ \_ \_ EACHPAGE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) , em que o controle de impressão [Direct2D](./direct2d-portal.md) subconjuntos e insere recursos de fonte em cada página e, em seguida, descarta esse subconjunto de fontes após a página ser impressa. Essa opção garante que cada página possa ser impressa imediatamente após ser gerada, mas aumenta ligeiramente o tamanho dos recursos da página necessários para a impressão (com geralmente subconjuntos de fontes grandes).
    -   Para trabalhos de impressão com muitas páginas de textos e tamanhos de fontes pequenos (como 100 páginas de texto que usam uma única fonte), recomendamos o [**\_ \_ \_ \_ modo de \_ subconjunto de fontes de impressão d2d1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode), em que o controle de impressão [Direct2D](./direct2d-portal.md) não subagrupará os recursos de fonte; em vez disso, ele envia os recursos originais da fonte junto com a página que usa a fonte pela primeira vez e reutiliza os recursos de fonte para as páginas posteriores, sem reenviá-los.
-   DPI de rasterização: quando o controle de impressão [Direct2D](./direct2d-portal.md) precisa rasterizar comandos Direct2D durante a conversão de DIRECT2D-XPS, ele usa esse dpi para rasterização. Em outras palavras, se a página não tiver nenhum conteúdo rasterizado, a definição de qualquer DPI não alterará o desempenho e a qualidade. Dependendo do uso da rasterização na página, você pode escolher DPIs de rasterização diferentes para obter o melhor equilíbrio entre a fidelidade e o desempenho.
    -   150 é o valor padrão se você não especificar um valor ao criar o controle de impressão [Direct2D](./direct2d-portal.md) , que é o melhor equilíbrio entre qualidade de impressão e desempenho de impressão na maioria dos casos.
    -   Valores de DPI mais altos geralmente resultam em melhor qualidade de impressão (assim como em mais detalhes preservados), mas reduz o desempenho devido aos bitmaps maiores que ele gera. Não recomendamos nenhum valor de DPI maior que 300, já que isso não introduzirá informações extras visualmente perceptível por olhos humanos.
    -   O DPI inferior pode significar um melhor desempenho, mas também pode produzir uma qualidade menor.

### <a name="avoid-using-certain-direct2d-drawing-patterns"></a>Evite usar determinados padrões de desenho Direct2D

Há diferenças entre o que o [Direct2D](./direct2d-portal.md) pode representar visualmente e o que o subsistema de impressão pode manter e transportar ao longo de todo o pipeline de impressão. O controle de impressão Direct2D une essas lacunas por aproximar ou rasterizando primitivos Direct2D para os quais o subsistema de impressão não dá suporte nativo. Essa aproximação geralmente resulta em menos fidelidade de impressão, menor desempenho de impressão ou ambos. Portanto, embora um cliente possa usar os mesmos padrões de desenho para a renderização de tela e impressão, ele não é ideal em todos os casos. É melhor não usar Direct2D primitivos e padrões tanto quanto possível para o caminho de impressão, ou para você ter a rasterização, na qual você tem controle total sobre a qualidade e o tamanho das imagens rasterizadas.

Aqui está uma lista de casos em que o desempenho de impressão e a qualidade não serão ideais e talvez você queira considerar a variação do caminho de código para o melhor desempenho de impressão.

-   Evite usar o modo de mistura primitiva diferente de [**d2d1 \_ Primitive \_ Blend \_ SOURCEOVER**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend).
-   Evite usar modos de composição ao desenhar uma imagem diferente [**da \_ \_ origem do \_ modo \_ composto d2d1**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_composite_mode) e o **\_ \_ destino do modo \_ \_ composto d2d1**.
-   Evite desenhar um meta arquivo GDI.
-   Evite enviar por push um recurso de camada que copia o plano de fundo de origem (chamando [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-pushlayer) com a [**\_ camada d2d1 \_ OPTIONS1 \_ inicializar \_ de \_ background**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) para a **\_ camada d2d1 \_ PARAMETERS1** struct).
-   Evite criar um pincel de bitmap ou um pincel de imagem com o \_ modo d2d1 Extend \_ \_ fixe. Recomendamos que você use \_ o \_ espelho do modo d2d1 Extend \_ se não se importar em pixels fora da imagem associada (como, a imagem anexada ao pincel é conhecida como maior que a região de destino preenchida).
-   Evite desenhar bitmaps com [transformações em perspectiva](3d-perspective-transform.md).

### <a name="draw-text-in-a-direct-and-plain-way"></a>Desenhar texto de maneira direta e simples

O Direct2D tem várias otimizações ao renderizar textos para serem exibidos para melhorar o desempenho e/ou melhor qualidade visual. Mas nem todas as otimizações melhoram o desempenho e a qualidade da impressão, já que a impressão em papel geralmente está em um DPI muito maior, e a impressão não precisa acomodar cenários como animação. Portanto, recomendamos que você desenhe o texto original ou os glifos diretamente e evite qualquer uma das otimizações a seguir ao criar a lista de comandos para impressão.

-   Evite desenhar texto com o método [**FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillopacitymask) .
-   Evite desenhar o texto no modo com alias.

### <a name="draw-the-original-bitmaps-when-possible"></a>Desenhe os bitmaps originais quando possível

Se o bitmap de destino for um JPEG, PNG, TIFF ou JPEG-XR, você poderá criar um bitmap do WIC a partir de um arquivo de disco ou de um fluxo na memória, em seguida, criar um bitmap do [Direct2D](./direct2d-portal.md) a partir desse bitmap do WIC usando [**ID2D1DeviceContext:: CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))e, por fim, passar diretamente pelo Direct2D bitmap para o controle de impressão Direct2D sem mais manipulação. Ao fazer isso, o controle de impressão Direct2D é capaz de reutilizar o fluxo de bitmap, que geralmente leva a um melhor desempenho de impressão (ignorando codificação e decodificação de bitmap redundante) e melhor qualidade de impressão (quando os metadados, como perfis de cor, no bitmap serão preservados).

O desenho do bitmap original fornece os benefícios a seguir para os aplicativos.

-   Em geral, a impressão [Direct2D](./direct2d-portal.md) preserva as informações originais (sem perda ou ruído) até o final do pipeline, especialmente quando os aplicativos não sabem (ou não querem saber) os detalhes do pipeline de impressão (como a impressora na qual ele está imprimindo, qual DPI é a impressora de destino e assim por diante).
-   Em muitos casos, atrasar a rasterização de bitmap significa melhor desempenho (como ao imprimir uma foto 96dpi em uma impressora 600dpi).
-   Em determinados casos, passar as imagens originais é a única maneira de honrar a alta fidelidade (como perfis de cores incorporados).

No entanto, um você não pode optar por essa otimização porque:

-   Ao consultar as informações da impressora e a rasterização antecipada, você pode rasterizar o próprio conteúdo com controle total da aparência final em papel.
-   Em determinados casos, a rasterização antecipada pode realmente melhorar o desempenho de ponta a ponta do aplicativo (como impressão de carteiras de tamanho).
-   Em determinados casos, passar os bitmaps originais requer uma alteração significativa da arquitetura de código existente (como carregamento de atraso de imagem e caminhos de atualização de recursos encontrados em determinados aplicativos).

## <a name="conclusion"></a>Conclusão

Embora o Direct2D seja acelerado por hardware e seja destinado a alto desempenho, você deve usar os recursos corretamente para maximizar a taxa de transferência. As técnicas que vimos aqui são derivadas de estudar cenários comuns e podem não se aplicar a todos os cenários de aplicativos.

 

 
