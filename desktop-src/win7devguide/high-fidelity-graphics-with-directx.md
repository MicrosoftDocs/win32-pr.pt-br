---
title: Gráficos de alta fidelidade com DirectX
description: Os desenvolvedores de aplicativos do Windows têm muito usado o Microsoft DirectX para fornecer gráficos 3D de alta qualidade, acelerados por hardware.
ms.assetid: db555657-90b9-4db2-a0c2-bfaa526a8dd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda45f911293b9d31b9ae28d89c25ed93ce33696
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641739"
---
# <a name="high-fidelity-graphics-with-directx"></a>Gráficos de alta fidelidade com DirectX

Os desenvolvedores de aplicativos do Windows têm muito usado o Microsoft DirectX para fornecer gráficos 3D de alta qualidade, acelerados por hardware. Quando a tecnologia apresentou 1995, os desenvolvedores podiam fornecer gráficos 3D de alta qualidade para jogos e aplicativos de engenharia para jogos e profissionais que desejam pagar outros para uma placa gráfica 3D. Agora, até mesmo os PCs mais baratos incluem hardware habilitado para gráficos 3D.

Para aproveitar esses recursos gráficos, o Windows Vista introduziu a infraestrutura do Windows Display Driver Model (WDDM) para DirectX, que permitia que vários aplicativos e serviços compartilhem os recursos da GPU (unidade de processamento gráfico). O Gerenciador de Janelas da Área de Trabalho (DWM) usa essa tecnologia para animar a alternância de tarefas em 3D, fornecer imagens em miniatura dinâmicas de janelas de aplicativos e fornecer efeitos de vidro de Windows Aero para aplicativos de desktop.

O Windows 7 coloca ainda mais recursos gráficos em mãos de desenvolvedores de aplicativos. Por meio de um novo conjunto de DirectXAPIs, os desenvolvedores do Microsoft Win32 podem aproveitar as inovações mais recentes em GPUs para adicionar gráficos, texto e imagens rápidos, escalonáveis, de alta qualidade, 2D e 3D a seus aplicativos. Nas exibições de *LCD* mais recentes, o DirectXAPIs pode exibir o conteúdo da área de trabalho e da janela usando profundidade de cor maior que 8 bits por componente de cor.

Com o DirectX, os desenvolvedores do Win32 também podem usar o paralelismo da GPU para computação de uso geral, como o processamento de imagens, e podem renderizar para hardware DirectX 10, hardware DirectX 9, CPU ou para um computador remoto com Windows. Essas tecnologias foram projetadas para interoperar com o Windows Graphics Device Interface (GDI) e o Windows GDI+, garantindo que os desenvolvedores possam facilmente preservar seus investimentos existentes no código Win32. (Veja [o que há de novo no SDK do DirectX de março de 2009](/previous-versions//bb173043(v=vs.85)).)

Esses recursos gráficos aprimorados são fornecidos pelas seguintes APIs baseadas em *com*:

-   [Direct2D](../direct2d/direct2d-portal.md) para desenhar gráficos 2D.
-   [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) para organizar e renderizar texto.
-   [Windows Imaging Component](/windows/desktop/wic/-wic-lh) para processamento e exibição de imagens.
-   [Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics) para desenhar gráficos 3D.
-   O [Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para desenhar gráficos 3D e fornecer acesso a tecnologias de GPU de última geração, como mosaico, suporte limitado para streaming de textura e computação de uso geral.
-   O [dxgi (infra-estrutura de gráficos do DirectX)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) para gerenciar dispositivos de vídeo locais e remotos e recursos de GPU e fornecer interoperabilidade entre o DirectX e o GDI.

## <a name="direct2d"></a>Direct2D

Criado com base no Microsoft Direct3D 10, o [Direct2D](../direct2d/direct2d-portal.md) oferece aos desenvolvedores do Win32 APIs de modo imediato, independente de resolução e 2D que usam o poder do hardware de gráficos de última geração, mas que interoperam bem com os aplicativos GDI/GDI+ atuais e aplicativos do Direct3D 10. O Direct2D fornece renderização 2D de alta qualidade com desempenho superior ao GDI e ao GDI+. Ele fornece aos desenvolvedores do Win32 um controle mais preciso sobre os recursos e seu gerenciamento. (Consulte [Direct2D](../direct2d/direct2d-portal.md).)

## <a name="directwrite"></a>DirectWrite

Muitos dos aplicativos atuais precisam dar suporte à renderização de texto de alta qualidade, fontes de estrutura de tópicos independentes de resolução e suporte completo a texto e layout Unicode. O [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), um novo componente do DirectX, fornece esses recursos e muito mais:

-   Um sistema de layout de texto independente de dispositivo que melhora a legibilidade do texto em documentos e na interface do usuário.
-   Renderização de texto *ClearType* de alta qualidade, sub-pixel, que pode usar a tecnologia de renderização GDI, [Direct2D](../direct2d/direct2d-portal.md)ou específica do aplicativo.
-   Texto acelerado por hardware, quando usado com [Direct2D](../direct2d/direct2d-portal.md).
-   Suporte para texto de vários formatos.
-   Suporte para os recursos de tipografia avançada de fontes *OpenType* .
-   Suporte para layout e renderização de texto em todos os idiomas com suporte.
-   Layout e renderização compatíveis com GDI.

O sistema de fontes [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) permite o uso de fontes "qualquer fonte em qualquer lugar", em que os usuários não precisam executar uma etapa de instalação separada apenas para usar uma fonte e uma hierarquia estrutural aprimorada de agrupamento de fontes para ajudar com a descoberta de fontes manual ou programática. As APIs dão suporte à medição, ao desenho e ao teste de impacto de texto de vários formatos. O DirectWrite lida com o texto em todos os idiomas com suporte para aplicativos globais e localizados, criando a infraestrutura de linguagem principal encontrada no Windows 7. O DirectWrite também fornece APIs de renderização de glifo de nível baixo para desenvolvedores que desejam executar seu próprio layout e processamento de Unicode para glifo. (Consulte [DirectWrite](../directwrite/direct-write-portal.md).)

## <a name="windows-imaging-component"></a>Windows Imaging Component

No Windows Vista, o [Windows Imaging Component](/windows/desktop/wic/-wic-lh) introduziu uma estrutura extensível para trabalhar com imagens e metadados de imagem. Os formatos de imagem com suporte do Windows Imaging Component incluem *JPEG*, *png* e *TIFF*, e os formatos de metadados com suporte incluem *XMP* e *EXIF*. Com o Windows 7, o Windows Imaging Component amplia sua conformidade com os padrões fornecendo suporte para decodificação de imagem progressiva, recursos de *png* expandidos, metadados *GIF* e metadados que abrangem segmentos *APPn* . (Veja [o que há de novo para o WIC no Windows 7](/previous-versions//ee720061(v=vs.85)).)

## <a name="direct3d-11"></a>Direct3D 11

O Microsoft Direct3D 11 estende a funcionalidade do pipeline do Direct3D 10 e fornece jogos do Windows 7 e aplicativos 3D de ponta com acesso eficiente, robusto e escalonável para a próxima geração de GPUs e CPUs com vários núcleos. Além da funcionalidade encontrada no Direct3D 10, o Direct3D 11 apresenta vários recursos novos.

As superfícies de geometria e de ordem superior agora podem ser mosaico para dar suporte a conteúdo escalonável e dinâmico em representações de área de patch e subdivisão.

Para fazer um bom uso do poder de processamento paralelo disponível de vários núcleos de CPU, o multithreading aumenta o número de chamadas de renderização em potencial por quadro, distribuindo o aplicativo, o tempo de execução e as chamadas de driver entre vários núcleos. Além disso, a criação e o gerenciamento de recursos foram otimizados para uso multithread, permitindo um gerenciamento de textura dinâmica mais eficiente para streaming.

Novos sombreadores de computação de uso geral foram criados para o Direct3D 11. Ao contrário dos sombreadores existentes, eles são extensões para o pipeline programável que permitem que seu aplicativo faça mais trabalho completamente na GPU, independentemente da CPU. O [**DrawAuto**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto), que foi introduzido no Direct3D 10, foi estendido para interagir com um sombreador de computação.

Várias melhorias foram feitas na[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)(linguagem de sombreamento de alto nível), como uma forma limitada de vínculo dinâmico em sombreadores para melhorar a complexidade da especialização e construções de programação orientada a objeto como classes e interfaces. (Veja [o que há de novo no SDK do DirectX de março de 2009](/previous-versions//bb173043(v=vs.85)).)

## <a name="direct3d-10-improvements"></a>Aprimoramentos do Direct3D 10

O Direct3D 10 inclui um pipeline de gráficos reprojetado com estágios de sombreador programáveis e objetos de estado imutáveis para inicializar os estágios de função fixa. Os objetos de estado simplificam o pipeline e melhoram o desempenho, minimizando o número de alterações de estado necessárias. A programação de estágios de sombreador agora oferece extensões de linguagem de sombreamento de alto nível para dar suporte a instruções de sombreamento ilimitado, recursos de sombreamento generalizado e cálculos de inteiros e de bit inteiro.

O pipeline também apresenta o estágio Geometry Shader, que descarrega o trabalho inteiramente da CPU para a GPU. Esse novo estágio permite que você crie geometria, transmita os dados para a memória e processe a geometria sem interação de CPU.

Várias outras melhorias foram projetadas especificamente para um desempenho mais rápido. A renderização de predicado executa a remoção de oclusão para reduzir a quantidade de geometria processada. As APIs de instanciação podem reduzir drasticamente a quantidade de geometria que precisa ser transferida para a GPU, desenhando várias instâncias de objetos semelhantes. As matrizes de textura permitem que a GPU Faça troca de textura sem intervenção da CPU.

Foram feitas várias adições ao Direct3D 10 e ao Direct3D 11 para estender a gama de configurações que podem ser direcionadas a essas APIs. A [Warp (plataforma de rasterização avançada do Windows)](/windows/desktop/direct3darticles/directx-warp) implementa RENDERIZAÇÃO de CPU rápida e escalonável de vários núcleos para o Direct3D 10, permitindo a renderização de gráficos com recursos completos em sistemas sem hardware de gráficos. A adição de novos "níveis de recursos", especificamente chamados de [Direct3D 10 nível 9](/windows/desktop/direct3d11/d3d11-graphics-reference-10level9), permite que o Direct3D 10 e o Direct3D 11APIs direcionem o hardware do Microsoft Direct3D 9, expandindo o número de configurações que um aplicativo Direct3D 10 ou Direct3D 11 pode ser direcionado a quase todos os sistemas de computador do mercado. (Consulte os [gráficos do Direct3D 10](../direct3d10/d3d10-graphics.md).)

## <a name="directxgdi-interoperability"></a>Interoperabilidade do DirectX/GDI

No Windows Vista, o comportamento de um aplicativo que usa DirectX e GDI para processar para uma superfície compartilhada é diferente dependendo se o DWM está ativado ou desativado. Além disso, quando o DWM está ativado, os aplicativos que usam DirectX e GDI se comportam de forma diferente no Windows Vista do que no Windows XP. Isso fazia com que muitos ISVs desabilitem o DWM ao executar seus aplicativos no Windows Vista para garantir um comportamento consistente. Com as melhorias no DirectX no Windows 7, um aplicativo agora pode misturar com DirectX e GDI livremente sem desabilitar o DWM. O Windows 7 também apresenta um desempenho aprimorado para cenários que exigem interoperação entre o DirectX e o GDI utilizando as APIs do Direct3D 10 mais eficientes. (Consulte [visão geral de interoperabilidade Direct2D e GDI](../direct2d/direct2d-and-gdi-interoperation-overview.md).)

 

 