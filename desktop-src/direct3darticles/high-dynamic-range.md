---
title: Usar DirectX com exibições de alto alcance dinâmico e cor avançada
description: Este tópico fornece uma visão geral técnica da renderização do conteúdo do Direct3D 11 e do Direct3D 12 de intervalo dinâmico para uma exibição HDR10 usando o suporte a cores avançadas do Windows 10.
ms.assetid: ''
ms.topic: article
ms.date: 04/23/2020
ms.openlocfilehash: 14d025e5431c42299c2c7f20ff198efa93959d7b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104567962"
---
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a>Usando o DirectX com altas exibições de intervalo dinâmico e cor avançada

Este tópico fornece uma visão geral técnica da saída do conteúdo do Direct3D 11 e do Direct3D 12 de intervalo dinâmico para uma exibição HDR10 usando o suporte a cores avançadas do Windows 10. Ele resume algumas das principais diferenças conceituais entre a saída para HDR10, em comparação com os monitores de SDR (intervalo dinâmico padrão) tradicionais. Ele também aborda os principais requisitos técnicos de seu aplicativo para dar suporte adequado à cor avançada do Windows, bem como recomendações e práticas recomendadas.

## <a name="introduction"></a>Introdução

O Windows 10 dá suporte a HDR e a outros monitores de cores avançadas, que fornecem uma fidelidade de cor significativamente maior do que a exibição do SDR tradicional. Você pode usar Direct3D, Direct2D e outras APIs de gráficos para renderizar conteúdo HDR para uma exibição compatível.

A cor avançada do Windows refere-se a várias tecnologias relacionadas, introduzidas pela primeira vez com o Windows 10 versão 1703, que fornecem suporte para exibições que excedem os recursos de cores das telas tradicionais de alcance dinâmico Standard (SDR). Os três principais recursos estendidos são descritos abaixo. O tipo mais comum de exibição de cor avançada, HDR10, dá suporte a todos os três recursos estendidos.

### <a name="high-dynamic-range"></a>Intervalo dinâmico alto

Intervalo dinâmico refere-se à diferença entre a luminância máxima e a mínima em uma cena; Isso geralmente é medido em nits (candelas por centímetro quadrado). Os bastidores do mundo real, como este pôr-no-sol, geralmente têm intervalos dinâmicos de 10 ordens de magnitude; o olho humano pode discernir um intervalo ainda maior após a adaptação.

![imagem de um sol com brilho e pontos mais escuros na cena rotulados](images/HDR-HDR.jpg)

Desde o Direct3D 9, os mecanismos gráficos conseguiram renderizar internamente suas cenas com esse nível de fidelidade fisicamente precisa. No entanto, uma exibição de faixa dinâmica padrão típica pode reproduzir apenas um pouco mais de três ordens de magnitude de luminância e, portanto, qualquer conteúdo processado por HDR tinha que ser tonemapped (compactado) no intervalo limitado da exibição. Novas exibições HDR, incluindo aquelas que estão em conformidade com o padrão HDR10 (BT. 2100), passam por essa limitação.

### <a name="wide-color-gamut-with-automatic-system-color-management"></a>Ampla gama de cores com o gerenciamento automático de cores do sistema

A gama de cores refere-se ao intervalo e à saturação de matizes que uma exibição pode reproduzir. A cor natural mais saturada que o olho humano pode perceber é pura, leve em monodesvio, como o que é produzido por uma laser. No entanto, as exibições de consumidor principais podem, muitas vezes, reproduzir cores apenas na gama de sRGB, que representa apenas cerca de 35% de todas as cores que podem ser exibidas pelo homem. O diagrama a seguir é uma representação do "Spectral local" humano ou de todas as cores experceptívels (em um determinado nível de luminância), onde o triângulo menor é a gama de sRGB.

![diagrama da gama de Spectral humana local e sRGB](images/HDR-WCG.jpg)

O high-end, Professional PC, exibe as gamas de cores com suporte muito mais amplas do que sRGB, como Adobe RGB e D65-P3. E esses monitores de ampla gama estão se tornando mais comuns. No entanto, antes da cor avançada, o Windows não executou nenhum gerenciamento de cores no nível do sistema para aplicativos. Isso significava que, se um aplicativo do DirectX renderizasse, por exemplo, um puro vermelho ou RGB (1,0, 0,0, 0,0) para sua cadeia de permuta, o Windows simplesmente examinaria o vermelho mais saturado que a exibição poderia reproduzir, independentemente da gama de cores real da exibição.

Os aplicativos que precisavam de alta precisão de cor poderiam consultar os recursos de cores da exibição (por exemplo, usando perfis ICC) e executar seu próprio gerenciamento de cores em processo para direcionar corretamente a gama de cores da exibição. No entanto, a grande maioria dos aplicativos e do conteúdo Visual pressupõe que a exibição é sRGB e depende do sistema operacional para atender a essa suposição.

A cor avançada do Windows adiciona o gerenciamento automático de cores no nível do sistema. O Gerenciador de Janelas da Área de Trabalho (DWM) é o compositor do Windows. Quando a cor avançada está habilitada, o DWM executa uma conversão de cor explícita do conteúdo visual do aplicativo colorspace para um espaço de cor de composição canônico, que é scRGB. Em seguida, o Windows converte por cor o conteúdo do framebuffer composto no espaço de cores nativa da exibição. Dessa forma, o conteúdo tradicional do sRGB obtém automaticamente o comportamento preciso de cor, enquanto os aplicativos avançados com reconhecimento de cores podem aproveitar os recursos de cores completas da tela.

### <a name="deep-precisionbit-depth"></a>Profundidade de bit/precisão profunda

Precisão numérica ou profundidade de bits, refere-se à representação ou distinção entre cores semelhantes, mas distintas, sem faixas nem artefatos. O PC principal exibe suporte a 8 bits por canal de cor, enquanto o olho humano requer pelo menos 10-12 bits de precisão para evitar distorções perceptível, sem recorrer a técnicas como pontilhamento ou dependendo das condições de exibição.

![imagem de Windmills em um canal de 2 bits simulado por cor versus 8 bits por canal](images/HDR-bitdepth.jpg)

Antes da cor avançada, os aplicativos de janela restritas do DWM para produzir conteúdo de saída em apenas 8 bits por canal de cor, mesmo que a exibição tenha suporte para uma profundidade de bits mais alta. Quando a cor avançada está habilitada, o DWM executa sua composição usando o ponto flutuante de metade de precisão do IEEE (FP16), eliminando quaisquer afunilamentos e permitindo a precisão total da exibição a ser usada.

## <a name="system-requirements"></a>Requisitos do Sistema

### <a name="operating-system-os"></a>OS (sistema operacional)

O suporte avançado a cores fornecido pela primeira vez com o Windows 10, versão 1703, e foi significativamente melhorado com cada atualização. Este tópico pressupõe que seu aplicativo está direcionando para o Windows 10, versão 1903 ou posterior.

### <a name="display"></a>Monitor

Para aproveitar o alto intervalo dinâmico, você deve ter uma exibição que dê suporte ao padrão HDR10. O Windows funciona melhor com exibições que são [certificadas pela VESA DisplayHDR](https://displayhdr.org/).

### <a name="graphics-processor-gpu"></a>Processador gráfico (GPU)

Uma GPU recente é necessária. Para dar suporte a exibições do HDR10, o Windows 10 requer um dos seguintes.

* NVIDIA GeForce 1000 Series (Pascal) ou mais recente
* AMD Radeon RX 400 Series (Polaris) ou mais recente
* Série Intel Core 7 selecionada (KABY Lake) ou mais recente

Observe que os requisitos de hardware adicionais se aplicam dependendo dos cenários, incluindo aceleração de codec de hardware (HEVC de 10 bits, VP9 de 10 bits etc.) e suporte do PlayReady (SL3000). Entre em contato com seu fornecedor de GPU para obter informações mais específicas.

### <a name="graphics-driver-wddm"></a>Driver de gráficos (WDDM)

O driver de gráficos mais recente disponível é altamente recomendado, seja de Windows Update ou do site do fabricante do computador ou fornecedor da GPU. Para o Windows 10, versão 1903 e posterior, recomendamos drivers que suportam pelo menos o Windows Display Driver Model (WDDM) versão 2,6.

## <a name="supported-rendering-apis"></a>APIs de renderização com suporte

O Windows 10 dá suporte a uma ampla variedade de APIs e estruturas de renderização. O suporte à cor avançada depende fundamentalmente de seu aplicativo ser capaz de executar uma apresentação moderna usando DXGI ou as APIs de camada Visual.

* [DXGI (infraestrutura gráfica do DirectX)](../direct3ddxgi/dx-graphics-dxgi.md)
* [Camada Visual (Windows. UI. composição)](/windows/uwp/composition/visual-layer)

Portanto, qualquer API de renderização que possa produzir saída para um desses métodos de apresentação pode dar suporte à cor avançada. Isso inclui, mas não se limita a esses.

* [Direct3D 11](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [Direct3D 12](../direct3d12/direct3d-12-graphics.md)
* [Direct2D](../direct2d/direct2d-portal.md)
* [Win2D](https://github.com/Microsoft/Win2D)
  * Requer o uso das APIs de nível inferior **CanvasSwapChain** ou **CanvasSwapChainPanel** .
* [**Windows.UI.Input.Inking**](/uwp/api/Windows.UI.Input.Inking)
  * Dá suporte à renderização de tinta seca personalizada usando DirectX.
* [XAML](/windows/uwp/xaml-platform/)
  * Dá suporte à reprodução de vídeos HDR usando o **mediaplayerelement**.
  * Dá suporte à decodificação de imagens JPEG XR usando o elemento **Image** .
  * Dá suporte à interoperabilidade do DirectX usando **SwapChainPanel**.

## <a name="handling-dynamic-display-capabilities"></a>Manipulando recursos de exibição dinâmica

O Windows 10 dá suporte a uma enorme variedade de monitores avançados com capacidade de cor, desde painéis integrados de energia e eficiência até monitores e TVs de jogos de ponta. Os usuários do Windows esperam que seu aplicativo manipule integralmente todas essas variações, incluindo exibições de SDR existentes.

O Windows 10 fornece controle sobre o HDR e recursos de cores avançados para o usuário. Seu aplicativo deve detectar a configuração atual do vídeo e responder dinamicamente a quaisquer alterações no recurso. Isso pode ocorrer por vários motivos, por exemplo, porque o usuário habilitou ou desabilitou um recurso ou moveu o aplicativo entre diferentes monitores ou o estado de energia do sistema mudou.

### <a name="universal-windows-platform-uwp-apps"></a>Aplicativos da Plataforma Universal do Windows (UWP)

Se você estiver escrevendo um aplicativo UWP, independentemente da API de renderização de gráficos que estiver usando, use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) para obter recursos de exibição. Obtenha uma instância de **AdvancedColorInfo** de [**DisplayInformation:: GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).

Para verificar qual tipo de cor avançado está ativo no momento, use a propriedade [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) . No Windows 10, versão 1903 e posterior, isso retorna um dos três valores possíveis: **SDR**, **WCG** ou **HDR**. Essa é a propriedade mais importante a ser verificada e você deve configurar seu pipeline de renderização e de apresentação em resposta ao tipo ativo.

Para verificar quais tipos de cores avançados têm suporte, mas não necessariamente ativos, chame [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable). Você pode usar essas informações, por exemplo, para solicitar que o usuário navegue até o aplicativo de configurações do Windows para que ele possa habilitar HDR ou WCG.

Os outros membros de **AdvancedColorInfo** fornecem informações quantitativas sobre o volume de cores físicas do painel (luminescência e crominância), correspondentes aos metadados HDR estáticos SMPTE St. 2086. Você deve usar essas informações para configurar o mapeamento de gamut e tonemapping HDR do seu aplicativo.

Para lidar com alterações em recursos de cores avançadas, registre-se para o evento [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) . Esse evento será gerado se qualquer parâmetro dos recursos de cores avançados da exibição for alterado por qualquer motivo.

Manipule esse evento obtendo uma nova instância de **AdvancedColorInfo** e verificando quais valores foram alterados.

### <a name="desktop-win32-directx-apps"></a>Aplicativos DirectX da área de trabalho (Win32)

Se você estiver escrevendo um aplicativo Win32 e usando o DirectX para renderizar, use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) para obter recursos de exibição. Obtenha uma instância desta estrutura por meio de [**IDXGIOutput6:: GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).

Para verificar qual tipo de cor avançado está ativo no momento, use a propriedade **colorspace** , que é do tipo [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)e contém um dos seguintes valores:

* **DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR
* **DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR

> [!Note]
> Outros tipos de cores avançados, como WCG, são tratados como SDR por DXGI. Não é possível usar DXGI para identificar uma exibição WCG.

> [!Note]
> DXGI não permite verificar quais tipos de cores avançados têm suporte, mas não estão ativos no momento.

A maioria dos outros membros de **DXGI_OUTPUT_DESC1** fornece informações quantitativas sobre o volume de cores físicas do painel (luminescência e crominância), que corresponde aos metadados HDR estáticos SMPTE St. 2086. Você deve usar essas informações para configurar o mapeamento de gamut e tonemapping HDR do seu aplicativo.

Os aplicativos Win32 não têm um mecanismo nativo para responder a alterações de recursos de cores avançadas. Em vez disso, se seu aplicativo usar um loop de renderização, você deverá consultar [**IDXGIFactory1:: IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) com cada quadro. Se ele reportar **false**, você deverá obter um novo **DXGI_OUTPUT_DESC1** e verificar quais valores foram alterados.

Além disso, a bomba de mensagens Win32 deve lidar com a [**WM_SIZE**](../winmsg/wm-size.md) mensagem, que indica que seu aplicativo pode ter sido movido entre diferentes exibições.

> [!Note]
> Para obter uma nova **DXGI_OUTPUT_DESC1**, você deve obter a exibição atual. No entanto, você não deve chamar **IDXGISwapChain:: GetContainingOutput**. Isso ocorre porque as cadeias de permuta retornarão uma saída DXGI obsoleta quando **DXGIFactory:: IsCurrent** for false e recriar a cadeia de permuta para obter uma saída atual resultará em uma tela preta temporária. Em vez disso, recomendamos que você enumere os limites de todas as saídas de DXGI e determine qual delas tem a maior interseção com os limites da janela do aplicativo.

O exemplo de código a seguir vem do [repositório DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).

```cpp
// Retrieve the current default adapter.
ComPtr<IDXGIAdapter1> dxgiAdapter;
ThrowIfFailed(m_dxgiFactory->EnumAdapters1(0, &dxgiAdapter));

// Iterate through the DXGI outputs associated with the DXGI adapter,
// and find the output whose bounds have the greatest overlap with the
// app window (i.e. the output for which the intersection area is the
// greatest).

UINT i = 0;
ComPtr<IDXGIOutput> currentOutput;
ComPtr<IDXGIOutput> bestOutput;
float bestIntersectArea = -1;

while (dxgiAdapter->EnumOutputs(i, &currentOutput) != DXGI_ERROR_NOT_FOUND)
{
    // Get the retangle bounds of the app window
    int ax1 = m_windowBounds.left;
    int ay1 = m_windowBounds.top;
    int ax2 = m_windowBounds.right;
    int ay2 = m_windowBounds.bottom;

    // Get the rectangle bounds of current output
    DXGI_OUTPUT_DESC desc;
    ThrowIfFailed(currentOutput->GetDesc(&desc));
    RECT r = desc.DesktopCoordinates;
    int bx1 = r.left;
    int by1 = r.top;
    int bx2 = r.right;
    int by2 = r.bottom;

    // Compute the intersection
    int intersectArea = ComputeIntersectionArea(ax1, ay1, ax2, ay2, bx1, by1, bx2, by2);
    if (intersectArea > bestIntersectArea)
    {
        bestOutput = currentOutput;
        bestIntersectArea = static_cast<float>(intersectArea);
    }

    i++;
}

// Having determined the output (display) upon which the app is primarily being 
// rendered, retrieve the HDR capabilities of that display by checking the color space.
ComPtr<IDXGIOutput6> output6;
ThrowIfFailed(bestOutput.As(&output6));

DXGI_OUTPUT_DESC1 desc1;
ThrowIfFailed(output6->GetDesc1(&desc1));
```

## <a name="setting-up-your-directx-swap-chain"></a>Configurando sua cadeia de permuta do DirectX

Depois de determinar que a exibição atualmente dá suporte a recursos de cores avançados, configure sua cadeia de permuta da seguinte maneira.

### <a name="use-a-flip-presentation-model-effect"></a>Usar um efeito de modelo de apresentação de inversão

Ao criar sua cadeia de permuta usando o **CreateSwapChainFor [HWND | Composição | CoreWindow]** , você deve usar o modelo de flip dxgi selecionando a opção **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** ou **DXGI_SWAP_EFFECT_FLIP_DISCARD** , que torna sua cadeia de permuta qualificada para o processamento avançado de cores do DWM e várias otimizações de tela inteira. Para obter mais informações, consulte o tópico [para obter o melhor desempenho, use o modelo de flip-dxgi](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) .

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a>Opção 1. Usar o formato de pixel FP16 e o espaço de cores scRGB

O Windows 10 dá suporte a duas combinações principais de formato de pixel e espaço de cores para a cor avançada. Selecione uma com base nos requisitos específicos do seu aplicativo.

Para aplicativos de uso geral, ao criar sua cadeia de permuta, é recomendável especificar [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format). Isso também é conhecido como *FP16* em sua [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1). Por padrão, uma cadeia de permuta criada com um formato de pixel de ponto flutuante é tratada como se ela usa o espaço de cores [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) , que também é conhecido como *ScRGB*.

Essa combinação fornece o intervalo numérico e a precisão para especificar quase qualquer cor possível fisicamente e executar processamento arbitrário, incluindo a mesclagem. Além disso, se você estiver usando Direct2D, Win2D ou Windows. UI. composição, essa será a única combinação com suporte para qualquer cadeia de permuta ou destino intermediário que contenha conteúdo de cores avançado. 

A principal compensação dessa opção é que ela consome 64 bits por pixel, o que dobra a largura de banda da GPU e o consumo de memória em comparação com os formatos de pixel UINT8 SDR tradicionais. Além disso, o scRGB usa valores numéricos que estão fora do intervalo [0, 1] normalizado para representar cores que estão fora da gama sRGB e/ou maior que 80 nits de luminância. Por exemplo, scRGB (1,0, 1,0, 1,0) codifica o branco D65 padrão às 80 nits; Mas scRGB (12,5, 12,5, 12,5) codifica o mesmo D65 branco com um número muito mais brilhante de 1000 nits. Algumas operações gráficas exigem um intervalo numérico normalizado, e você deve modificar a operação ou renormalizar os valores de cor.

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a>Opção 2: usar o formato de pixel UINT10/RGB10 e o espaço de cores HDR10/BT. 2100

Para aplicativos que consomem conteúdo codificado em HDR10, como players de mídia ou aplicativos que devem ser usados principalmente em cenários de tela inteira, como jogos, ao criar sua cadeia de permuta, você deve considerar a especificação de [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) em [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1). Por padrão, isso é tratado como usando o espaço de cores sRGB; Portanto, você deve chamar explicitamente [**IDXGISwapChain3:: SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)e definir como seu espaço de cor [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), também conhecido como HDR10/BT. 2100.

Essa combinação tem restrições mais rígidas do que FP16. Você pode usar isso somente com o Direct3D 11 ou o Direct3D 12. Além disso, o UINT10/HDR10 tem limitações como um formato intermediário porque usa a função ST. 2084 EOTF ("gama"), que é altamente não linear e otimizada como um formato de conexão e oferece apenas 2 bits de alfa.

No entanto, essa combinação pode oferecer otimizações de desempenho poderosas quando usadas na saída final do seu aplicativo. Ele consome os mesmos 32 bits por pixel que os formatos de pixel UINT8 SDR tradicionais. Além disso, em determinados cenários de tela inteira, o sistema operacional pode otimizar o desempenho verificando diretamente a superfície HDR10.

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a>Usando uma cadeia de troca de cor avançada quando a exibição está no modo de SDR

Você pode usar uma cadeia de troca de cor avançada mesmo que a exibição não dê suporte a alguns ou todos os recursos de cores avançados que seu conteúdo requer. Nesses casos, o Gerenciador de Janelas da Área de Trabalho (DWM) downconvertá seu conteúdo para se ajustar aos recursos da exibição. No Windows 10, versão 1903 e posterior, ele executará o recorte numérico; por exemplo, se você renderizar para uma cadeia de permuta FP16 scRGB, tudo fora do intervalo numérico [0, 1] será recortado.

Esse comportamento de downconversion também ocorrerá se a janela do aplicativo estiver ampliando duas ou mais exibições com diferentes recursos de cores avançados. **AdvancedColorInfo** e **IDXGIOutput6** são abstrados para relatar apenas as características da exibição "Main" (definidas como a exibição que contém o centro da janela).

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a>Renderizar corretamente o conteúdo do SDR com o nível de referência do SDR

Em muitos cenários, seu aplicativo desejará renderizar o conteúdo do SDR e do HDR; por exemplo, a renderização de legendas ou controles de transporte sobre o vídeo HDR ou a interface do usuário em uma cena de jogo. É importante entender o conceito de *nível branco de referência do SDR* para garantir que o conteúdo do SDR fique correto em uma tela HDR.

O Windows trata o conteúdo HDR como _mencionado na cena_, o que significa que um valor de cor específico deve ser exibido em um nível de luminância específico; por exemplo, scRGB (1,0, 1,0, 1,0) e HDR10 (497, 497, 497) codificam exatamente D65 branco à luminância de 80 nits. Enquanto isso, o conteúdo do SDR tradicionalmente tem sido _de saída – referenciado_ (ou exibido como referência), o que significa que sua luminância é deixada para o usuário ou para o dispositivo; por exemplo, sRGB (1,0, 1,0, 1,0) codifica D65 em branco como nos exemplos de HDR, mas em qualquer nível máximo de luminosidade em que a exibição é configurada. O Windows permite que o usuário ajuste o _nível de referência do SDR_ para sua preferência; Essa é a luminância que o Windows processará sRGB (1,0, 1,0, 1,0) em. Nos monitores HDR da área de trabalho, os níveis brancos de referência do SDR normalmente são definidos como cerca de 200 nits.

> [!Note]
> Em uma exibição que dá suporte a um controle de brilho, como em um laptop, o Windows também ajustará a luminância do conteúdo HDR (referenciado pela cena) para corresponder ao nível de brilho desejado do usuário, mas isso é invisível para o aplicativo. A menos que você esteja tentando garantir a reprodução precisa de bit do sinal HDR, geralmente é possível ignorar isso.

Se seu aplicativo sempre renderiza SDR e HDR em superfícies separadas e se baseia na composição do sistema operacional, o Windows executará automaticamente o ajuste correto para aumentar o conteúdo do SDR para o nível de branco desejado. Por exemplo, se seu aplicativo usar XAML e renderizar conteúdo HDR para seu próprio **SwapChainPanel**.

No entanto, se seu aplicativo executar sua própria composição de conteúdo de SDR e HDR em uma única superfície, você será responsável por executar o ajuste de nível de referência do SDR por conta própria. Caso contrário, o conteúdo do SDR pode parecer muito escuro, supondo condições de exibição de desktop típicas. Primeiro, você deve obter o nível branco de referência do SDR atual e, em seguida, ajustar os valores de cor de qualquer conteúdo SDR que esteja renderizando.

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a>Etapa 1. Obter o nível branco de referência do SDR atual

Atualmente, somente os aplicativos UWP podem obter o nível de referência do SDR atual por meio de [**AdvancedColorInfo. SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits). Essa API requer um [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).

### <a name="step-2-adjust-color-values-of-sdr-content"></a>Etapa 2. Ajustar valores de cor do conteúdo do SDR

O Windows define o nível branco de referência nominal, ou padrão, às 80 nits; Portanto, se você fosse processar um branco sRGB (1,0, 1,0, 1,0) padrão para uma cadeia de permuta FP16, ele seria reproduzido a uma luminância de 80 nits. Para corresponder ao nível branco de referência definido pelo usuário real, você deve ajustar o conteúdo do SDR de 80 nits para o nível especificado por meio de **AdvancedColorInfo. SdrWhiteLevelInNits**.

Se você estiver renderizando usando FP16 e ScRGB, ou qualquer espaço de cores que usa gama linear (1,0), poderá simplesmente multiplicar o valor de cor do SDR por _AdvancedColorInfo. SdrWhiteLevelInNits_  /  _80_. Se você estiver usando Direct2D, haverá uma constante predefinida [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), que tem um valor de 80.

```cpp
D2D1_VECTOR_4F inputColor; // Input SDR color value.
D2D1_VECTOR_4F outputColor; // Output color adjusted for SDR white level.
auto acInfo; // AdvancedColorInfo

float sdrAdjust = acInfo->SdrWhiteLevelInNits / D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL;

// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
outputColor.r = inputColor.r * sdrAdjust; // Assumes linear gamma color values.
outputColor.g = inputColor.g * sdrAdjust;
outputColor.b = inputColor.b * sdrAdjust;
outputColor.a = inputColor.a;
```

Se você estiver renderizando usando um espaço de cores gama não linear, como HDR10, executar o ajuste de nível de branco do SDR será mais complexo; Se você estiver escrevendo seu próprio sombreador de pixel, considere a possibilidade de converter em gama linear para aplicar o ajuste.

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a>Adapte o conteúdo do HDR aos recursos do vídeo usando o tonemapping

As telas de cores HDR e avançadas variam muito em termos de seus recursos. Por exemplo, a luminância mínima e máxima e a gama de cores são capazes de reproduzir. Em muitos casos, o conteúdo HDR conterá cores que excedem os recursos do vídeo. Para obter a melhor qualidade de imagem, é importante que você execute o HDR tonemapping, basicamente compactando o intervalo de cores para se ajustar à exibição, melhor preservando a intenção visual do conteúdo.

O parâmetro único mais importante para se adaptar é a luminância máxima, também conhecida como MaxCLL (nível de luz de conteúdo); tonemappers mais sofisticados também adaptarão a luminância mín (MinCLL) e/ou primárias de cores.

### <a name="step-1-get-the-displays-color-volume-capabilities"></a>Etapa 1. Obter os recursos de volume de cores da tela

#### <a name="universal-windows-platform-uwp-apps"></a>Aplicativos da Plataforma Universal do Windows (UWP)

Use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) para obter o volume de cores da tela.

#### <a name="win32-desktop-directx-apps"></a>Aplicativos DirectX do Win32 (Desktop)

Use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) para obter o volume de cores da tela.

### <a name="step-2-get-the-contents-color-volume-information"></a>Etapa 2. Obter as informações de volume de cores do conteúdo

Dependendo de onde veio seu conteúdo HDR, há várias maneiras possíveis de determinar suas informações de luminância e de gama de cores. Determinados arquivos de vídeo e imagem HDR contêm metadados SMPTE ST. 2086. Se o conteúdo tiver sido renderizado dinamicamente, você poderá extrair informações de cena dos estágios de renderização internos, por exemplo, a fonte de luz mais brilhante em uma cena.

Uma solução mais geral, mas computacionalmente dispendiosa, é executar um histograma ou outra passagem de análise no quadro renderizado. O [exemplo do SDK de imagens de cores avançadas do Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) demonstra como fazer isso usando o Direct2D; os trechos de código mais relevantes estão incluídos abaixo:

```cpp
// Perform histogram pipeline setup; this should occur as part of image resource creation.
// Histogram results in no visual output but is used to calculate HDR metadata for the image.
void D2DAdvancedColorImagesRenderer::CreateHistogramResources()
{
    auto context = m_deviceResources->GetD2DDeviceContext();

    // We need to preprocess the image data before running the histogram.
    // 1. Spatial downscale to reduce the amount of processing needed.
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1Scale, &m_histogramPrescale)
        );

    DX::ThrowIfFailed(
        m_histogramPrescale->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(0.5f, 0.5f))
        );

    // The right place to compute HDR metadata is after color management to the
    // image's native colorspace but before any tonemapping or adjustments for the display.
    m_histogramPrescale->SetInputEffect(0, m_colorManagementEffect.Get());

    // 2. Convert scRGB data into luminance (nits).
    // 3. Normalize color values. Histogram operates on [0-1] numeric range,
    //    while FP16 can go up to 65504 (5+ million nits).
    // Both steps are performed in the same color matrix.
    ComPtr<ID2D1Effect> histogramMatrix;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1ColorMatrix, &histogramMatrix)
        );

    histogramMatrix->SetInputEffect(0, m_histogramPrescale.Get());

    float scale = sc_histMaxNits / sc_nominalRefWhite;

    D2D1_MATRIX_5X4_F rgbtoYnorm = D2D1::Matrix5x4F(
        0.2126f / scale, 0, 0, 0,
        0.7152f / scale, 0, 0, 0,
        0.0722f / scale, 0, 0, 0,
        0              , 0, 0, 1,
        0              , 0, 0, 0);
    // 1st column: [R] output, contains normalized Y (CIEXYZ).
    // 2nd column: [G] output, unused.
    // 3rd column: [B] output, unused.
    // 4th column: [A] output, alpha passthrough.
    // We explicitly calculate Y; this deviates from the CEA 861.3 definition of MaxCLL
    // which approximates luminance with max(R, G, B).

    DX::ThrowIfFailed(histogramMatrix->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, rgbtoYnorm));

    // 4. Apply a gamma to allocate more histogram bins to lower luminance levels.
    ComPtr<ID2D1Effect> histogramGamma;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1GammaTransfer, &histogramGamma)
        );

    histogramGamma->SetInputEffect(0, histogramMatrix.Get());

    // Gamma function offers an acceptable tradeoff between simplicity and efficient bin allocation.
    // A more sophisticated pipeline would use a more perceptually linear function than gamma.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, sc_histGamma));
    // All other channels are passthrough.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE, TRUE));

    // 5. Finally, the histogram itself.
    HRESULT hr = context->CreateEffect(CLSID_D2D1Histogram, &m_histogramEffect);
    
    if (hr == D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES)
    {
        // The GPU doesn't support compute shaders and we can't run histogram on it.
        m_isComputeSupported = false;
    }
    else
    {
        DX::ThrowIfFailed(hr);
        m_isComputeSupported = true;

        DX::ThrowIfFailed(m_histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, sc_histNumBins));

        m_histogramEffect->SetInputEffect(0, histogramGamma.Get());
    }
}

// Uses a histogram to compute a modified version of MaxCLL (ST.2086 max content light level).
// Performs Begin/EndDraw on the D2D context.
void D2DAdvancedColorImagesRenderer::ComputeHdrMetadata()
{
    // Initialize with a sentinel value.
    m_maxCLL = -1.0f;

    // MaxCLL is not meaningful for SDR or WCG images.
    if ((!m_isComputeSupported) ||
        (m_imageInfo.imageKind != AdvancedColorKind::HighDynamicRange))
    {
        return;
    }

    // MaxCLL is nominally calculated for the single brightest pixel in a frame.
    // But we take a slightly more conservative definition that takes the 99.99th percentile
    // to account for extreme outliers in the image.
    float maxCLLPercent = 0.9999f;

    auto ctx = m_deviceResources->GetD2DDeviceContext();

    ctx->BeginDraw();

    ctx->DrawImage(m_histogramEffect.Get());

    // We ignore D2DERR_RECREATE_TARGET here. This error indicates that the device
    // is lost. It will be handled during the next call to Present.
    HRESULT hr = ctx->EndDraw();
    if (hr != D2DERR_RECREATE_TARGET)
    {
        DX::ThrowIfFailed(hr);
    }

    float *histogramData = new float[sc_histNumBins];
    DX::ThrowIfFailed(
        m_histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT,
            reinterpret_cast<BYTE*>(histogramData),
            sc_histNumBins * sizeof(float)
            )
        );

    unsigned int maxCLLbin = 0;
    float runningSum = 0.0f; // Cumulative sum of values in histogram is 1.0.
    for (int i = sc_histNumBins - 1; i >= 0; i--)
    {
        runningSum += histogramData[i];
        maxCLLbin = i;

        if (runningSum >= 1.0f - maxCLLPercent)
        {
            break;
        }
    }

    float binNorm = static_cast<float>(maxCLLbin) / static_cast<float>(sc_histNumBins);
    m_maxCLL = powf(binNorm, 1 / sc_histGamma) * sc_histMaxNits;

    // Some drivers have a bug where histogram will always return 0. Treat this as unknown.
    m_maxCLL = (m_maxCLL == 0.0f) ? -1.0f : m_maxCLL;
}
```

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a>Etapa 3. Executar a operação HDR tonemapping

O tonemapping é inerentemente a um processo com perdas e pode ser otimizado para várias métricas de perceptiva ou objetivo, portanto, não há um algoritmo padrão. O Windows fornece um efeito interno de [Tonemapper HDR](../direct2d/hdr-tone-map-effect.md) como parte do Direct2D, bem como no pipeline de reprodução de vídeo Media Foundation HDR. Alguns outros algoritmos comumente usados incluem ACES Películaal, Reinhard e ITU-R BT. 2390-3 EETF (função de transferência elétrica elétrica).

Um operador Reinhard tonemapper simplificado é mostrado abaixo.

```cpp
// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
D2D1_VECTOR_4F simpleReinhardTonemapper(
    float inputMax, // Content's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    float outputMax, // Display's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    D2D1_VECTOR_4F input // scRGB color.
)
{
    D2D1_VECTOR_4F output = input;

    // Vanilla Reinhard normalizes color values to [0, 1].
    // This modification scales to the luminance range of the display.
    output.r /= inputMax;
    output.g /= inputMax;
    output.b /= inputMax;

    output.r = (output.r / 1 + output.r);
    output.g = (output.g / 1 + output.g);
    output.b = (output.b / 1 + output.b);

    output.r *= outputMax;
    output.g *= outputMax;
    output.b *= outputMax;

    return output;
}
```

## <a name="capturing-hdr-and-wcg-content"></a>Capturando conteúdo HDR e WCG

APIs que dão suporte à especificação de formatos de pixel, como aqueles no namespace [**Windows. Graphics. Capture**](/uwp/api/windows.graphics.capture) e o método [**IDXGIOutput5::D uplicateoutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) , fornecem a capacidade de capturar conteúdo de cabeçalho e WCG sem perder informações de pixel. Observe que, após a aquisição de quadros de conteúdo, será necessário processamento adicional. Por exemplo, o mapeamento de tons de HDR para SDR (por exemplo, a cópia de captura de tela do SDR para compartilhamento da Internet) e o salvamento de conteúdo com o formato adequado (por exemplo, JPEG XR).

## <a name="additional-resources"></a>Recursos adicionais

* *Usando a renderização HDR com o DirectX Tool Kit* para [DirectX 11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)  /  [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering). Walkthrough de como adicionar suporte a HDR a um aplicativo DirectX usando o DirectX Tool Kit (DirectXTK).
* [Exemplo do SDK de imagens de cores avançadas do Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages). Exemplo de SDK do UWP implementando um WCG com reconhecimento de cor avançado e um visualizador de imagem do amDirect2D. Demonstra a gama completa de práticas recomendadas para aplicativos UWP, incluindo a resposta às alterações de funcionalidade de vídeo e o ajuste do nível branco do SDR.
* [Exemplo de área de trabalho HDR do Direct3D 12](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR). Exemplo de SDK de desktop implementando uma cena HDR básica do Direct3D 12.
* [Exemplo de UWP de HDR do Direct3D 12](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR). UWP equivalente da amostra acima.
* [Exemplo de PC do Xbox ATG SimpleHDR](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC). Exemplo de SDK de desktop implementando uma cena HDR básica do Direct3D 11.
