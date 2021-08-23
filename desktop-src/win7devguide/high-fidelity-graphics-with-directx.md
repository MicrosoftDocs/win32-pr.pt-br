---
title: Gráficos de alta fidelidade com DirectX
description: Windows desenvolvedores de aplicativos por muito tempo usaram o Microsoft DirectX para fornecer gráficos 3D de alta qualidade, acelerados por hardware.
ms.assetid: db555657-90b9-4db2-a0c2-bfaa526a8dd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9ecb5d6403745162f19b16eea15c22ef7f9676b14bd291226af2f8321483b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086639"
---
# <a name="high-fidelity-graphics-with-directx"></a>Gráficos de alta fidelidade com DirectX

Windows desenvolvedores de aplicativos por muito tempo usaram o Microsoft DirectX para fornecer gráficos 3D de alta qualidade, acelerados por hardware. Quando a tecnologia começou em 1995, os desenvolvedores podiam fornecer gráficos 3D de alta qualidade para jogos e aplicativos de engenharia para gamers e profissionais dispostos a pagar extra por uma placa gráfica 3D. Agora, até mesmo os PCs mais baratos incluem hardware de gráficos 3D com capacidade.

Para aproveitar esses recursos gráficos, o Windows Vista introduziu a infraestrutura do WDDM (Modelo de Driver de Exibição) do Windows para DirectX que permitia que vários aplicativos e serviços compartilhem os recursos da GPU (unidade de processamento gráfico). O Gerenciador de Janelas da Área de Trabalho (DWM) usa essa tecnologia para animar a alternação de tarefas em 3D, fornecer imagens em miniatura dinâmicas de janelas de aplicativos e fornecer efeitos Windows Aero glass para aplicativos da área de trabalho.

Windows 7 coloca ainda mais funcionalidade de gráficos nas mãos dos desenvolvedores de aplicativos. Por meio de um novo conjunto de DirectXAPIs, os desenvolvedores do Microsoft Win32 podem aproveitar as inovações mais recentes em GPUs para adicionar gráficos, texto e imagens rápidos, escalonáveis, de alta qualidade, 2D e 3D a seus aplicativos. Nas exibições *mais recentes do LCD,* o DirectXAPIs pode exibir o conteúdo da área de trabalho e da janela usando a profundidade de cor maior que 8 bits por componente de cor.

Com o DirectX, os desenvolvedores do Win32 também podem usar o paralelismo da GPU para computação de uso geral, como processamento de imagem, e podem renderizar para hardware do DirectX 10, hardware DirectX 9, CPU ou para um computador Windows remoto. Essas tecnologias foram projetadas para interoperar com Windows Graphics Device Interface (GDI) e Windows GDI+, garantindo que os desenvolvedores possam preservar facilmente seus investimentos existentes no código Win32. (Consulte Novidades no SDK do DirectX de março de [2009](/previous-versions//bb173043(v=vs.85)).)

Esses recursos gráficos aprimorados são fornecidos pelas seguintes APIs baseadas em *COM:*

-   [Direct2D](../direct2d/direct2d-portal.md) para desenhar gráficos 2D.
-   [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) para organizar e renderizar texto.
-   [Windows componente de imagens](/windows/desktop/wic/-wic-lh) para processamento e exibição de imagens.
-   [Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics) para desenhar gráficos 3D.
-   [Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para desenhar gráficos 3D e fornecer acesso a tecnologias de GPU de última geração, como mosaico, suporte limitado para streaming de textura e computação de uso geral.
-   [DirectX Graphic Infrastructure (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) para gerenciar dispositivos de exibição locais e remotos e recursos de GPU e fornecer interoperabilidade entre DirectX e GDI.

## <a name="direct2d"></a>Direct2D

Criado no Microsoft Direct3D 10, o [Direct2D](../direct2d/direct2d-portal.md) oferece aos desenvolvedores do Win32 APIs 2D independentes de resolução e de modo imediato que usam o poder do hardware gráfico de última geração, mas interoperam bem com os aplicativos GDI/GDI+ atuais e os aplicativos Direct3D 10. Direct2D fornece renderização 2D de alta qualidade com desempenho superior ao GDI e GDI+. Ele fornece aos desenvolvedores do Win32 um controle mais fino sobre os recursos e seu gerenciamento. (Consulte [Direct2D](../direct2d/direct2d-portal.md).)

## <a name="directwrite"></a>DirectWrite

Muitos dos aplicativos atuais precisam dar suporte à renderização de texto de alta qualidade, fontes de estrutura de contorno independentes de resolução e suporte completo a texto e layout Unicode. [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), um novo componente DirectX, fornece estes recursos e muito mais:

-   Um sistema de layout de texto independente de dispositivo que melhora a capacidade de leitura de texto em documentos e na interface do usuário.
-   Renderização de texto De alta qualidade, sub pixel, *ClearType* que pode usar GDI, [Direct2D](../direct2d/direct2d-portal.md)ou tecnologia de renderização específica do aplicativo.
-   Texto acelerado por hardware, quando usado com [Direct2D](../direct2d/direct2d-portal.md).
-   Suporte para texto de vários formatos.
-   Suporte para os recursos avançados de tipografia de *fontes OpenType.*
-   Suporte para o layout e renderização de texto em todos os idiomas com suporte.
-   Renderização e layout compatíveis com GDI.

O [sistema de](/windows/desktop/DirectWrite/direct-write-portal) fontes DirectWrite permite o uso da fonte "qualquer fonte em qualquer lugar", em que os usuários não têm que executar uma etapa de instalação separada apenas para usar uma fonte e uma hierarquia estrutural aprimorada do grupo de fontes para ajudar com a descoberta manual ou programática de fontes. As APIs são suportando medição, desenho e teste de acerto de texto de vários formatos. DirectWrite lida com texto em todos os idiomas com suporte para aplicativos globais e localizados, com base na infraestrutura de linguagem principal encontrada no Windows 7. DirectWrite também fornece APIs de renderização de glifo de baixo nível para desenvolvedores que querem executar seu próprio layout e processamento Unicode para glifo. (Consulte [DirectWrite](../directwrite/direct-write-portal.md).)

## <a name="windows-imaging-component"></a>Windows Imaging Component

No Windows Vista, o [Windows Imaging Component](/windows/desktop/wic/-wic-lh) introduziu uma estrutura extensível para trabalhar com imagens e metadados de imagem. Os formatos de imagem com suporte pelo Windows componente de imagens incluem *JPEG,* *PNG* e *TIFF* e os formatos de metadados com suporte incluem *XMP* e *EXIF*. Com Windows 7, o componente de imagens Windows amplia sua conformidade de padrões fornecendo suporte para decodificação de imagem progressiva, recursos *de PNG* expandidos, metadados *GIF* e metadados que abrangem segmentos *APPn.* (Consulte [Novidades do WIC no Windows 7](/previous-versions//ee720061(v=vs.85)).)

## <a name="direct3d-11"></a>Direct3D 11

O Microsoft Direct3D 11 estende a funcionalidade do Windows pipeline do Direct3D 10 e fornece 7 jogos e aplicativos 3D de alto nível com acesso eficiente, robusto e escalonável à próxima geração de GPUs e CPUs de vários núcleos. Além da funcionalidade encontrada no Direct3D 10, o Direct3D 11 apresenta vários novos recursos.

As superfícies geometry e de ordem alta agora podem ser mosaicas para dar suporte a conteúdo dinâmico e escalonável em representações de superfície de patch e subdivisão.

Para fazer bom uso da potência de processamento paralelo disponível de vários núcleos de CPU, o multithreading aumenta o número de chamadas de renderização potenciais por quadro distribuindo o aplicativo, o runtime e as chamadas de driver em vários núcleos. Além disso, a criação e o gerenciamento de recursos foram otimizados para uso multithread, permitindo um gerenciamento de textura dinâmico mais eficiente para streaming.

Novos sombreadores de computação de uso geral foram criados para o Direct3D 11. Ao contrário dos sombreadores existentes, essas são extensões para o pipeline programável que permitem que seu aplicativo faça mais trabalho completamente na GPU, independentemente da CPU. [**DrawAuto**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto), que foi introduzido no Direct3D 10, foi estendido para interagir com um sombreador de computação.

Várias melhorias foram feitas na[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)(linguagem de sombreamento de alto nível), como uma forma limitada de vinculação dinâmica em sombreadores para melhorar a complexidade da especialização e constructos de programação orientados a objeto, como classes e interfaces. (Consulte Novidades no SDK do DirectX de março de [2009](/previous-versions//bb173043(v=vs.85)).)

## <a name="direct3d-10-improvements"></a>Melhorias do Direct3D 10

O Direct3D 10 inclui um pipeline de gráficos reprojetado com estágios de sombreador programáveis e objetos de estado imutáveis para inicializar os estágios de função fixa. Os objetos de estado simplificam o pipeline e melhoram o desempenho minimizando o número de alterações de estado necessárias. A programação dos estágios do sombreador agora oferece extensões de linguagem de sombreamento de alto nível para dar suporte a instruções de sombreador ilimitadas, recursos de sombreador generalizados e cálculos inteiros e bit a bit.

O pipeline também apresenta o estágio do sombreador de geometria, que descarrega o trabalho inteiramente da CPU para a GPU. Esse novo estágio permite criar geometria, transmitir os dados para a memória e renderizar a geometria sem interação com a CPU.

Várias outras melhorias foram projetadas especificamente para um desempenho mais rápido. A renderização predicada executa a redução de oclusão para reduzir a quantidade de geometria renderizada. A instanciação de APIs pode reduzir drasticamente a quantidade de geometria que precisa ser transferida para a GPU desenhando várias instâncias de objetos semelhantes. Matrizes de textura permitem que a GPU faça a troca de textura sem intervenção da CPU.

Várias adições foram feitas ao Direct3D 10 e direct3D 11 para estender a gama de configurações que podem ser direcionadas com essas APIs. O [Windows WARP (Advanced Rasterization Platform)](/windows/desktop/direct3darticles/directx-warp) implementa uma renderização de CPU escalonável rápida e de vários núcleos para o Direct3D 10, permitindo renderização de gráficos completos em sistemas sem hardware gráfico. A adição de novos "Níveis de Recurso", especificamente chamados [de Direct3D 10 Nível 9](/windows/desktop/direct3d11/d3d11-graphics-reference-10level9), permite que as 11APIs direct3D 10 e Direct3D conduzam o hardware de 9 classes do Microsoft Direct3D, expandindo o número de configurações que um aplicativo Direct3D 10 ou Direct3D 11 pode direcionar para quase todos os sistemas de computadores no mercado. (Consulte [Elementos gráficos do Direct3D 10](../direct3d10/d3d10-graphics.md).)

## <a name="directxgdi-interoperability"></a>Interoperabilidade do DirectX/GDI

No Windows Vista, o comportamento de um aplicativo que usa DirectX e GDI para renderizar em uma superfície compartilhada é diferente dependendo se o DWM está on ou off. Além disso, quando o DWM está em, os aplicativos que usam DirectX e GDI se comportam de maneira diferente no Windows Vista do que no Windows XP. Isso fez com que muitos ISVs desabilitasse a DWM ao executar seus aplicativos no Windows Vista para garantir um comportamento consistente. Com as melhorias no DirectX no Windows 7, um aplicativo agora pode misturar gratuitamente o DirectX e o GDI sem desabilitar a DWM. Windows 7 também apresenta um desempenho aprimorado para cenários que exigem interoperação entre DirectX e GDI utilizando as APIs mais eficientes do Direct3D 10. (Consulte [Direct2D visão geral de interoperação GDI](../direct2d/direct2d-and-gdi-interoperation-overview.md)e .)

 

 