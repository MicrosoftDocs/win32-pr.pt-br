---
title: Roteiro para aplicativos DirectX para Desktop
description: Aqui estão os principais recursos para ajudá-lo a começar a usar o DirectX e o C++ para desenvolver aplicativos de área de trabalho com uso intensivo de gráficos, como jogos.
ms.assetid: d7921f38-e384-4a83-b458-ee71f7044468
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca95e1fe281253705620136afdced3cb705fe02
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104008643"
---
# <a name="roadmap-for-desktop-directx-apps"></a>Roteiro para aplicativos DirectX para Desktop

Aqui estão os principais recursos para ajudá-lo a começar a usar o DirectX e o C++ para desenvolver aplicativos de área de trabalho com uso intensivo de gráficos, como jogos. Essa não é uma lista abrangente de todos os recursos ou recursos disponíveis.

## <a name="get-started"></a>Introdução

Aqui estão alguns tópicos importantes. Configurar seu projeto do DirectX, acclimating-lo para o Windows e aplicativos de exemplo.

| Tópico | Descrição |
|-|-|
| [Crie seu primeiro aplicativo do Windows usando DirectX](building-your-first-directx-app.md) | Use este tutorial básico para começar a usar o desenvolvimento de aplicativos DirectX e, em seguida, use o roteiro para continuar explorando o DirectX. |
| [Introdução ao DirectX para Windows](getting-started-with-a-directx-game.md) | Examine as etapas que você deve seguir para começar a desenvolver um jogo usando DirectX e C++. |
| [Código completo de uma estrutura do DirectX](complete-code-sample-for-using-a-corewindow-with-directx.md) | Obtenha o código para uma estrutura de renderização básica do DirectX. |
| [Como usar o Direct3D 11](/windows/desktop/direct3d11/how-to-use-direct3d-11) | Esta seção demonstra como usar a API do Microsoft Direct3D 11 para realizar várias tarefas comuns. |
| [Guia de programação para Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews) | O guia de programação contém informações sobre como usar o pipeline programável do Microsoft Direct3D 11 para criar gráficos 3D em tempo real para aplicativos de área de trabalho. |
| [Ferramentas para elementos gráficos do DirectX](/windows/desktop/direct3dtools/dx-graphics-tools) | Documentação para ferramentas usadas para dar suporte ao desenvolvimento do DirectX. |
| [O que há de novo no Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews-introduction) | Uma análise de todos os recursos adicionados nas versões mais recentes do DirectX e do Direct3D (atualmente 11,2). |
| [Baixar o Visual Studio 2013](https://msdn.microsoft.com/windows/apps/br229516.aspx) | Você deve ter Visual Studio Express 2013 para Windows Desktop para criar jogos da Windows Store. Para obter um tour pelo Visual Studio, consulte [desenvolver aplicativos da Windows Store usando o visual studio 2012](/previous-versions/windows/apps/br211384(v=win.10)). Para obter informações sobre os novos recursos do Visual Studio, consulte [destaques do produto para Visual Studio 2013](/previous-versions/visualstudio/visual-studio-2013/bb386063(v=vs.120)). |
| [Onde está o SDK do DirectX?](../directx-sdk--august-2009-.md) | Contém diretrizes para desenvolvedores que desejam trazer seus projetos do DirectX para Microsoft Visual Studio. |

## <a name="sample-applications"></a>Aplicativos de exemplo

| Tópico | Descrição |
|-|-|
| [Exemplo de Win32 do tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) | Exemplo de tutorial de Direct3D de desktop básico. |
| [Exemplo de renderização de vídeo DirectX](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20video%20rendering%20sample) | Um exemplo que demonstra a renderização de vídeo personalizada com o Direct3D. |

## <a name="review-key-direct3d-11-concepts"></a>Examinar os principais conceitos do Direct3D 11

| Tópico | Descrição |
|-|-|
| [Pipeline de gráficos](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline) | Cobre o pipeline básico do Direct3D 11 Graphics. |
| [Renderização](/windows/desktop/direct3d11/overviews-direct3d-11-render) | Aborda os modelos de renderização Direct3D, componentes, sombreadores e fluxo de chamada de API. |
| [Recursos](/windows/desktop/direct3d11/overviews-direct3d-11-resources) | Cobre "recursos" do Direct3D, como buffers e outros tipos de recursos de GPU. |
| [Effect](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects) | Aborda a instanciação e os efeitos do Direct3D multi-Shader.  |
| [Como: criar uma cadeia de permuta](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-swap-chain) | Como criar a cadeia de permuta usada para desenhar pixels em uma região da tela. |
| [Como: criar um dispositivo e um contexto imediato](/windows/desktop/direct3d11/overviews-direct3d-11-devices-initialize) | Como criar uma abstração de dispositivo Direct3D e um contexto imediato para desenho. |
| [Como criar um buffer de vértice](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-vertex-how-to) | Como criar uma lista simples de vértices de malha para processamento pela GPU. |
| [Como: criar um buffer de índice](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-index-how-to) | Como criar um buffer de índice que habilita o sombreador de vértice para percorrer a ordem dos vértices em uma malha. |
| [Como: criar um buffer de constantes](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to) | Como passar dados constantes (uniformes) entre a CPU e a GPU durante a renderização. |
| [Como: criar uma textura](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create) | Como criar uma textura ou outro recurso de buffer que pode ser amostrado pela GPU. |
| [Como: inicializar uma textura a partir de um arquivo](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-how-to) | Como carregar uma textura de um arquivo e processá-lo para uso pelo pipeline do sombreador. |
| [Como: compilar um sombreador](../direct3d11/how-to--compile-a-shader.md) | Como compilar um sombreador para uso em seu aplicativo de gráficos. |

## <a name="graphics-apis"></a>APIs de gráficos

| Tópico | Descrição |
|-|-|
| [Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference) | Documentação das principais APIs para a virtualização da GPU e seus recursos, e para desenhar gráficos usando um modelo de sombreador unificado. |
| [Direct3D HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) | Documentação de referência para High-Level idioma do sombreador, a sintaxe e as regras usadas para definir os programas de sombreador executados como parte do pipeline de gráficos em um modelo de sombreador unificado. |
| [DXGI (interface gráfica do DirectX)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) | Documentação das APIs de baixo nível usadas para adquirir a interface de GPU e os recursos do sistema. |
| [Direct2D](/windows/desktop/Direct2D/direct2d-portal) | Documentação para as APIs do Direct2D, que dão suporte ao desenho de primitivos 2D. Normalmente, o Direct2D é usado para interfaces de usuário personalizadas, processamento de imagens e envio em lote e jogos simples. |
| [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) | Documentação para as APIs do DirectWrite, que dão suporte à renderização e ao dimensionamento de fontes personalizadas. |
| [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api) | Documentação para as APIs do WIC, que são usadas para ler e gerenciar diferentes formatos de imagem de bitmap. |
| [Superfícies do DirectDraw (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds) para texturas | Documentação para as APIs de DDS, que são usadas para compactação de textura 2D e descompactação em conjunto com as APIs do WIC. |
| [DirectXMath](/windows/desktop/dxmath/directxmath-portal) | Documentação para as APIs do DirectXMath, que dão suporte ao Direct3D com um conjunto de tipos e funções adequadas para o desenvolvimento de gráficos em tempo real 3D. (Anteriormente XNAMath.) |
| [DirectCompute](https://walbourn.github.io/) | Documentação para as APIs do DirectCompute, usadas para computação ou funcionalidade de sombreador de uso geral. |

## <a name="audio-media-and-input-apis"></a>APIs de áudio, mídia e entrada

| Tópico | Descrição |
|-|-|
| [Guia de Programação em XAudio2](/windows/desktop/xaudio2/programming-guide) | Nó de nível superior da documentação conceitual da API de áudio do XAudio2. |
| [Referência de programação em XAudio2](/windows/desktop/xaudio2/programming-reference) | Nó de nível superior para a documentação de referência da API de áudio do XAudio2. |
| [Guia de programação do XInput](/windows/desktop/xinput/programming-guide) | Nó de nível superior da documentação conceitual da API do controlador XInput. |
| [Referência de programação XInput](/windows/desktop/xinput/programming-reference) | Nó de nível superior para a documentação de referência da API do controlador XInput. |
| [Media Foundation](/windows/desktop/medfound/about-the-media-foundation-sdk) | Nó de nível superior para a documentação da API de reprodução de mídia (áudio/vídeo) do Media Foundation (MF). Normalmente, o MF é usado em jogos para reprodução de trilha sonora, enquanto XAudio2 é usado para áudio dinâmico. |

## <a name="port-to-directx-11"></a>Porta para DirectX 11

| Tópico | Descrição |
|-|-|
| [Migrando para o Direct3D 11](/windows/desktop/direct3d11/d3d11-programming-guide-migrating) | Diretrizes básicas para mover a base de código DirectX 9 para DirectX 11. |
| [Técnicas de codificação de uso duplo para jogos](https://walbourn.github.io/) | Postagem detalhada no blog sobre o desenvolvimento para os níveis de recurso DirectX 9 \_ \* e DirectX 11 \_ \* em um único aplicativo. |
| [Implementando buffers de sombra para o nível de recurso do Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)) | Diretrizes para implementar mapas de sombra no nível de recurso do DirectX 9 \_ \* . |

## <a name="work-with-c"></a>Trabalhar com C++

Se você for um velho lado com C++ em plataformas Windows, as coisas podem parecer um pouco diferentes. Aqui estão algumas dicas para tópicos que podem ajudá-lo a obter um identificador sobre a diferença.

> [!NOTE]
> Alguns desses tópicos existem para ajudá-lo a manter seu aplicativo C++/CX. Recomendamos que você use [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt) para novos aplicativos. C++/WinRT é uma projeção de linguagem C++17 completamente moderna e padrão para APIs do WinRT (Windows Runtime), implementada como uma biblioteca com base em cabeçalho e arquivo, projetada para fornecer acesso de primeira classe à API moderna do Windows.

| Tópico | Descrição |
|-|-|
| [**Referência de linguagem de Visual C++ (C++/CX)**](/cpp/cppcx/visual-c-language-reference-c-cx?view=vs-2019) | Página de alto nível que vincula ao conteúdo relacionado ao C++. |
| [**Referência rápida (Windows Runtime e Visual C++)**](/cpp/cppcx/quick-reference-c-cx?view=vs-2019) | Tabela que fornece informações rápidas sobre Visual C++ de operadores de extensões de componente (C++/CX) e palavras-chave. |
| [**Sistema de tipos (C++/CX)**](/cpp/cppcx/type-system-c-cx?view=vs-2019) | Conteúdo de referência para os tipos com suporte no C++/CX. |
| [**Namespaces (C++/CX)**](/cpp/cppcx/namespaces-reference-c-cx?view=vs-2019) | Conteúdo de referência para os namespaces que contêm tipos específicos de C++ que podem ser usados em aplicativos da Windows Store. |

| | |
|-|-|
| [Programação assíncrona (DirectX e C++)](/previous-versions/windows/apps/hh994919(v=win.10)) | Saiba mais sobre programação assíncrona e multithread para aplicativos e jogos do DirectX. |
| [Programação assíncrona em C++](/previous-versions/windows/apps/hh780559(v=win.10)) | Descreve as maneiras básicas de usar a classe Task para consumir Windows Runtime métodos assíncronos. |
| [**Classe Task (Tempo de Execução de Simultaneidade)**](/previous-versions/visualstudio/visual-studio-2012/hh750113(v=vs.110)) | Documentação de referência para a classe Task. |
| [Paralelismo de tarefas (Tempo de Execução de Simultaneidade)](/previous-versions/visualstudio/visual-studio-2010/dd492427(v=vs.100)) | Uma discussão aprofundada sobre a classe Task e como usá-la. |

## <a name="additional-useful-libraries-for-windows-c-programming"></a>Bibliotecas úteis adicionais para programação do Windows C++

| | |
|-|-|
| [Biblioteca de modelos padrão do C++](https://msdn.microsoft.com/library/c191tb28(v=VS.71).aspx) | Windows Runtime tipos funcionam bem com os tipos de biblioteca de modelos padrão. A maioria dos aplicativos da Windows Store do C++ usa algoritmos e coleções de bibliotecas de modelos padrão, exceto no limite da ABI. |
| [Biblioteca de Padrões Paralelos](/previous-versions/visualstudio/visual-studio-2010/dd492418(v=vs.100)) | A PPL fornece algoritmos e tipos que simplificam o paralelismo de tarefas e o paralelismo de dados na CPU.  |
| [C++ Accelerated Massive Parallelism (C++ AMP)](/previous-versions/visualstudio/visual-studio-2012/hh265137(v=vs.110)) | C++ AMP fornece acesso à GPU para paralelismo de dados de uso geral em placas de vídeo que dão suporte ao DirectX 11. |

## <a name="blogs-and-other-resources"></a>Blogs e outros recursos

| Tópico | Descrição |
|-|-|
| [Blog sobre jogos para Windows e DirectX](https://walbourn.github.io/) | Blog atualizado regularmente de um colaborador de desenvolvimento principal do DirectX e um excelente recurso para o DirectX desenvolvedores. |
| [Blog de desenvolvedores do Windows DirectX](https://devblogs.microsoft.com/directx/) | O blog oficial do Windows DirectX. |
| [Blog do DirectX de Shawn Hargreave](https://www.shawnhargreaves.com/blogindex.html)) | Blog de desenvolvimento de outro colaborador de desenvolvimento do Windows DirectX bem respeitado. |
| [Kit de ferramentas do DirectX](https://directxtk.codeplex.com/) | Site do CodePlex para o kit de ferramentas do DirectX (DxTK), que contém uma série de APIs de suporte úteis para carregar malhas, reproduzir sons e outros comportamentos comuns. |
| [Biblioteca de processamento de texturas DirectXTex](https://directxtex.codeplex.com/) | O site de plex de código para a DxTEX (biblioteca de processamento de textura do DirectX), que contém APIs de suporte para processamento de textura e compactação/descompactação. |