---
title: Roteiro para aplicativos DirectX para Desktop
description: Aqui estão os principais recursos para ajudá-lo a começar a usar o DirectX e o C++ para desenvolver aplicativos de Área de Trabalho com uso intensivo de gráficos, como jogos.
ms.assetid: d7921f38-e384-4a83-b458-ee71f7044468
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5940e775de65d6d22a9b244d1bd0b881240cf296b740c9a0be9c38f3ab0725a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983886"
---
# <a name="roadmap-for-desktop-directx-apps"></a>Roteiro para aplicativos DirectX para Desktop

Aqui estão os principais recursos para ajudá-lo a começar a usar o DirectX e o C++ para desenvolver aplicativos de Área de Trabalho com uso intensivo de gráficos, como jogos. Essa não é uma lista abrangente de todos os recursos ou recursos disponíveis.

## <a name="get-started"></a>Introdução

Aqui estão alguns tópicos principais. Configurar seu projeto do DirectX, alimando-se a Windows aplicativos de exemplo.

| Tópico | Descrição |
|-|-|
| [Criar seu primeiro aplicativo Windows usando o DirectX](building-your-first-directx-app.md) | Use este tutorial básico para começar a usar o desenvolvimento de aplicativos DirectX e, em seguida, use o roteiro para continuar explorando o DirectX. |
| [Começar a trabalhar com o DirectX para Windows](getting-started-with-a-directx-game.md) | Revise as etapas que você deve seguir para começar a desenvolver um jogo usando DirectX e C++. |
| [Código completo para uma estrutura DirectX](complete-code-sample-for-using-a-corewindow-with-directx.md) | Obter o código para uma estrutura básica de renderização do DirectX. |
| [Como usar o Direct3D 11](/windows/desktop/direct3d11/how-to-use-direct3d-11) | Esta seção demonstra como usar a API do Microsoft Direct3D 11 para realizar várias tarefas comuns. |
| [Guia de programação para Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews) | O guia de programação contém informações sobre como usar o pipeline programável do Microsoft Direct3D 11 para criar gráficos 3D em tempo real para aplicativos da área de trabalho. |
| [Ferramentas para elementos gráficos do DirectX](/windows/desktop/direct3dtools/dx-graphics-tools) | Documentação para ferramentas usadas para dar suporte ao desenvolvimento do DirectX. |
| [Novidades no Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews-introduction) | Um detalhamento de todos os recursos adicionados nas versões mais recentes do DirectX e direct3D (atualmente 11.2). |
| [Baixar o Visual Studio 2013](https://msdn.microsoft.com/windows/apps/br229516.aspx) | Você deve ter Visual Studio Express 2013 para Windows Desktop para criar jogos Windows Store. Para ver um tour pelo Visual Studio, confira Desenvolver [aplicativos Windows Store usando Visual Studio 2012](/previous-versions/windows/apps/br211384(v=win.10)). Para obter informações sobre novos recursos no Visual Studio, consulte [Destaques do produto para Visual Studio 2013](/previous-versions/visualstudio/visual-studio-2013/bb386063(v=vs.120)). |
| [Onde está o SDK do DirectX?](../directx-sdk--august-2009-.md) | Contém diretrizes para devs que querem trazer seus projetos DirectX para Microsoft Visual Studio. |

## <a name="sample-applications"></a>Aplicativos de exemplo

| Tópico | Descrição |
|-|-|
| [Exemplo do Win32 do Tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) | Exemplo de tutorial básico do Direct3D da área de trabalho. |
| [Exemplo de renderização de vídeo do DirectX](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20video%20rendering%20sample) | Um exemplo que demonstra a renderização de vídeo personalizada com o Direct3D. |

## <a name="review-key-direct3d-11-concepts"></a>Revisar os principais conceitos do Direct3D 11

| Tópico | Descrição |
|-|-|
| [Pipeline de gráficos](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline) | Aborda o pipeline de gráficos básico do Direct3D 11. |
| [Renderização](/windows/desktop/direct3d11/overviews-direct3d-11-render) | Abrange os modelos de renderização direct3D, componentes, sombreadores e fluxo de chamada de API. |
| [Recursos](/windows/desktop/direct3d11/overviews-direct3d-11-resources) | Abrange "recursos" do Direct3D, como buffers e outros tipos de recursos de GPU. |
| [Efeitos](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects) | Abrange a instanciamento e os efeitos do sombreador múltiplo Direct3D.  |
| [Como criar uma cadeia de permuta](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-swap-chain) | Como criar a cadeia de permuta usada para desenhar pixels para uma região da tela. |
| [Como criar um dispositivo e um contexto imediato](/windows/desktop/direct3d11/overviews-direct3d-11-devices-initialize) | Como criar uma abstração de dispositivo Direct3D e um contexto imediato para desenho. |
| [Como criar um buffer de vértice](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-vertex-how-to) | Como criar uma lista simples de vértices de malha para processamento pela GPU. |
| [Como criar um buffer de índice](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-index-how-to) | Como criar um buffer de índice permitindo que o sombreador de vértice ande pela ordem dos vértices em uma malha. |
| [Como criar um buffer constante](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to) | Como passar dados constantes (uniformes) entre a CPU e a GPU durante a renderização. |
| [Como criar uma textura](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create) | Como criar uma textura ou outro recurso de buffer que pode ser amostrado pela GPU. |
| [Como inicializar uma textura de um arquivo](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-how-to) | Como carregar uma textura de um arquivo e processá-la para uso pelo pipeline do sombreador. |
| [Como compilar um sombreador](../direct3d11/how-to--compile-a-shader.md) | Como compilar um sombreador para uso em seu aplicativo gráfico. |

## <a name="graphics-apis"></a>APIs de elementos gráficos

| Tópico | Descrição |
|-|-|
| [Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference) | Documentação das APIs principais para a virtualização da GPU e seus recursos e para desenhar gráficos usando um modelo de sombreador unificado. |
| [Direct3D HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) | Documentação de referência para High-Level de sombreador, a sintaxe e as regras usadas para definir programas de sombreador executados como parte do pipeline gráfico em um modelo de sombreador unificado. |
| [DXGI (Interface gráfica do DirectX)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) | Documentação das APIs de baixo nível usadas para adquirir a interface de GPU e os recursos do sistema. |
| [Direct2D](/windows/desktop/Direct2D/direct2d-portal) | Documentação das APIs Direct2D, que suportam o desenho de primitivos 2D. Normalmente, o Direct2D é usado para interfaces de usuário personalizadas, processamento de imagens e lote e jogos simples. |
| [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) | Documentação das APIs DirectWrite, que suportam renderização e dimensionamento de fontes personalizadas. |
| [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api) | Documentação das APIs do WIC, que são usadas para ler e gerenciar diferentes formatos de imagem de bitmap. |
| [DirectDraw Surfaces (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds) para texturas | Documentação das APIs DDS, que são usadas para compactação de textura 2D e descompactação em conjunto com as APIs do WIC. |
| [DirectXMath](/windows/desktop/dxmath/directxmath-portal) | Documentação das APIs do DirectXMath, que suportam o Direct3D com um conjunto de tipos e funções adequados para o desenvolvimento de gráficos em tempo real 3D. (anteriormente XNAMath.) |
| [Directcompute](https://walbourn.github.io/) | Documentação das APIs do DirectCompute, usadas para a funcionalidade de sombreador de computação ou uso geral. |

## <a name="audio-media-and-input-apis"></a>APIs de áudio, mídia e entrada

| Tópico | Descrição |
|-|-|
| [Guia de Programação em XAudio2](/windows/desktop/xaudio2/programming-guide) | Nó de nível superior para a documentação conceitual da API de áudio XAudio2. |
| [Referência de programação em XAudio2](/windows/desktop/xaudio2/programming-reference) | Nó de nível superior para a documentação de referência da API de áudio XAudio2. |
| [Guia de Programação XInput](/windows/desktop/xinput/programming-guide) | Nó de nível superior para a documentação conceitual da API do controlador XInput. |
| [Referência de programação XInput](/windows/desktop/xinput/programming-reference) | Nó de nível superior para a documentação de referência da API do controlador XInput. |
| [Media Foundation](/windows/desktop/medfound/about-the-media-foundation-sdk) | Nó de nível superior para a documentação da API de reprodução de mídia Media Foundation (MF) (áudio/vídeo). Normalmente, o MF é usado em jogos para reprodução de trilha sonora, enquanto XAudio2 é usado para áudio dinâmico. |

## <a name="port-to-directx-11"></a>Porta para DirectX 11

| Tópico | Descrição |
|-|-|
| [Migrando para o Direct3D 11](/windows/desktop/direct3d11/d3d11-programming-guide-migrating) | Diretrizes básicas para mover a base de código DirectX 9 para DirectX 11. |
| [Técnicas de codificação de uso duplo para jogos](https://walbourn.github.io/) | Postagem detalhada no blog sobre o desenvolvimento para os níveis de recurso DirectX 9 \_ \* e DirectX 11 \_ \* em um único aplicativo. |
| [Implementando buffers de sombra para o nível de recurso do Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)) | Diretrizes para implementar mapas de sombra no nível de recurso do DirectX 9 \_ \* . |

## <a name="work-with-c"></a>Trabalhar com C++

se você for um velho lado com C++ em plataformas Windows, as coisas podem parecer um pouco diferentes. Aqui estão algumas dicas para tópicos que podem ajudá-lo a obter um identificador sobre a diferença.

> [!NOTE]
> Alguns desses tópicos existem para ajudá-lo a manter seu aplicativo C++/CX. Recomendamos que você use [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt) para novos aplicativos. C++/WinRT é uma projeção de linguagem C++17 completamente moderna e padrão para APIs do WinRT (Windows Runtime), implementada como uma biblioteca com base em cabeçalho e arquivo, projetada para fornecer acesso de primeira classe à API moderna do Windows.

| Tópico | Descrição |
|-|-|
| [**Referência de linguagem de Visual C++ (C++/CX)**](/cpp/cppcx/visual-c-language-reference-c-cx?view=vs-2019) | Página de alto nível que vincula ao conteúdo relacionado ao C++. |
| [**referência rápida (Windows Runtime e Visual C++)**](/cpp/cppcx/quick-reference-c-cx?view=vs-2019) | Tabela que fornece informações rápidas sobre Visual C++ de operadores de extensões de componente (C++/CX) e palavras-chave. |
| [**Sistema de tipos (C++/CX)**](/cpp/cppcx/type-system-c-cx?view=vs-2019) | Conteúdo de referência para os tipos com suporte no C++/CX. |
| [**Namespaces (C++/CX)**](/cpp/cppcx/namespaces-reference-c-cx?view=vs-2019) | conteúdo de referência para os namespaces que contêm tipos específicos do C++ que podem ser usados em aplicativos da Windows Store. |

| Tópico | Descrição |
|-|-|
| [Programação assíncrona (DirectX e C++)](/previous-versions/windows/apps/hh994919(v=win.10)) | Saiba mais sobre programação assíncrona e multithread para aplicativos e jogos do DirectX. |
| [Programação assíncrona em C++](/previous-versions/windows/apps/hh780559(v=win.10)) | descreve as maneiras básicas de usar a classe task para consumir Windows Runtime métodos assíncronos. |
| [**Classe Task (Tempo de Execução de Simultaneidade)**](/previous-versions/visualstudio/visual-studio-2012/hh750113(v=vs.110)) | Documentação de referência para a classe Task. |
| [Paralelismo de tarefas (Tempo de Execução de Simultaneidade)](/previous-versions/visualstudio/visual-studio-2010/dd492427(v=vs.100)) | Uma discussão aprofundada sobre a classe Task e como usá-la. |

## <a name="additional-useful-libraries-for-windows-c-programming"></a>bibliotecas úteis adicionais para a programação Windows C++

| Tópico | Descrição |
|-|-|
| [Biblioteca de modelos padrão do C++](https://msdn.microsoft.com/library/c191tb28(v=VS.71).aspx) | Windows Os tipos de tempo de execução funcionam bem com os tipos de biblioteca de modelos padrão. a maioria dos aplicativos da Windows Store do C++ usa coleções e algoritmos da biblioteca de modelos padrão, exceto no limite da ABI. |
| [Biblioteca de Padrões Paralelos](/previous-versions/visualstudio/visual-studio-2010/dd492418(v=vs.100)) | A PPL fornece algoritmos e tipos que simplificam o paralelismo de tarefas e o paralelismo de dados na CPU.  |
| [C++ Accelerated Massive Parallelism (C++ AMP)](/previous-versions/visualstudio/visual-studio-2012/hh265137(v=vs.110)) | C++ AMP fornece acesso à GPU para paralelismo de dados de uso geral em placas de vídeo que dão suporte ao DirectX 11. |

## <a name="blogs-and-other-resources"></a>Blogs e outros recursos

| Tópico | Descrição |
|-|-|
| [blog de jogos para Windows e DirectX](https://walbourn.github.io/) | Blog atualizado regularmente de um colaborador de desenvolvimento principal do DirectX e um excelente recurso para o DirectX desenvolvedores. |
| [Windows Blog de desenvolvedores do DirectX](https://devblogs.microsoft.com/directx/) | o blog oficial do Windows DirectX. |
| [Blog do DirectX de Shawn Hargreave](https://www.shawnhargreaves.com/blogindex.html)) | blog de desenvolvimento de outro Windows colaborador de desenvolvimento do DirectX bem respeitado. |
| [Kit de ferramentas do DirectX](https://directxtk.codeplex.com/) | Site do CodePlex para o kit de ferramentas do DirectX (DxTK), que contém uma série de APIs de suporte úteis para carregar malhas, reproduzir sons e outros comportamentos comuns. |
| [Biblioteca de processamento de texturas DirectXTex](https://directxtex.codeplex.com/) | O site de plex de código para a DxTEX (biblioteca de processamento de textura do DirectX), que contém APIs de suporte para processamento de textura e compactação/descompactação. |