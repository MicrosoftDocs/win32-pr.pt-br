---
description: O Direct3D é uma API de baixo nível para desenhar primitivos com o pipeline de renderização ou executar operações paralelas com o sombreador de computação.
ms.assetid: 55063BF2-34A3-4E56-882C-86F0949DE557
title: Como começar a trabalhar com o Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea01f24659bfbb5eb0667a0ae1cbfa3529a206b7b7ce7e3d3a4388e71fabd571
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092546"
---
# <a name="getting-started-with-direct3d"></a>Como começar a trabalhar com o Direct3D

O Direct3D é uma API de baixo nível para desenhar primitivos com o pipeline de renderização ou para executar operações paralelas com o sombreador de computação.

## <a name="what-is-direct3d"></a>O que é o Direct3D?

O Direct3D é uma API de baixo nível que você pode usar para desenhar triângulos, linhas ou pontos por quadro ou para iniciar operações altamente paralelas na GPU.

Direct3D:

-   Oculta diferentes implementações de GPU por trás de uma abstração coerente. Mas você ainda precisa saber como desenhar gráficos 3D.
-   Foi projetado para impulsionar um processador específico de gráficos separado. As GPUs mais novas têm centenas ou milhares de processadores paralelos.
-   Enfatiza o processamento paralelo. Você configura um monte de renderização ou estado de computação e, em seguida, inicia uma operação. Você não aguarda comentários imediatos da operação. Você não combina operações de CPU e GPU.

## <a name="which-direct3d-apis-can-you-use"></a>Quais APIs do Direct3D você pode usar?

As APIs do Direct3D escolhidas dependem do estilo do aplicativo que você deseja escrever.

-   Se você quiser escrever um aplicativo UWP, use um subconjunto de APIs direct3D 11, DXGI e HLSL. Para ver uma lista dessas APIs, consulte [APIs Win32 e COM para aplicativos UWP](/uwp/win32-and-com/win32-and-com-for-uwp-apps). Para saber como escrever um aplicativo do Direct3D 11 Windows Store, consulte Criar [gráficos 3D com o DirectX.](/previous-versions/windows/apps/hh465137(v=win.10))
-   Se você escrever um aplicativo da área de trabalho, poderá usar o conjunto completo de APIs Direct3D 11, DXGI e HLSL.
-   Começando com Windows 8, não damos mais suporte ativamente à estrutura XNA para aplicativos da área de trabalho. Mas Windows aplicativos da Store, aplicativos UWP e aplicativos da área de trabalho podem usar o conjunto completo das APIs [XAudio2](/windows/desktop/xaudio2/xaudio2-apis-portal) e [DirectXMath.](/windows/desktop/dxmath/directxmath-portal) Os aplicativos da área de trabalho podem usar o conjunto completo das APIs [XInput,](/windows/desktop/xinput/xinput-game-controller-apis-portal) enquanto os aplicativos da Windows Store e aplicativos UWP podem usar a maioria das APIs XInput; Para obter mais informações, consulte [Versões XInput](/windows/desktop/xinput/xinput-versions).

## <a name="which-direct3d-version"></a>Qual versão do Direct3D?

A versão da API do Direct3D escolhida depende do sistema operacional e do nível de hardware que você deseja direcionar.

-   Se você quiser direcionar Windows 8 e posteriores, use AS APIs do Direct3D 11.
-   Use APIs do Direct3D 9 com Windows XP e posteriores. Todo o hardware dá suporte a APIs do Direct3D 9, até mesmo hardware de nível 11 mais recente do Direct3D.
-   Use as APIs do Direct3D 10 com Windows Vista e posteriores. Somente hardwares de nível 10 e posteriores do Direct3D são suportados por APIs do Direct3D 10.
-   Use as APIs direct3D 10.1 e Direct3D 11 com Windows 7 e posteriores. Você também pode usar as APIs direct3D 10.1 e Direct3D 11 com o Windows Vista com Service Pack 2 (SP2) baixando [o KB 971644](https://support.microsoft.com/kb/971644).

## <a name="direct3d-rendering-pipeline"></a>Pipeline de renderização do Direct3D

No [pipeline](./direct3d11/overviews-direct3d-11-graphics-pipeline.md)de renderização do Direct3D, os dados fluem de várias fontes, como os afluentes de um rio.

-   Algumas partes do fluxo são programáveis.
-   Algumas partes têm botões e discagem.
-   As fontes de dados são fluxos seriais de pacotes (vértices) ou matrizes indexáveis (recursos de sombreador).
-   Os vértices e os recursos do sombreador fluem para primitivos, que você pode ampliar.
-   Primitivos e recursos de sombreador fluem para operações de pixel.

## <a name="direct3d-compute-shader"></a>Sombreador de computação Direct3D

Com o sombreador de [computação](./direct3d11/direct3d-11-advanced-stages-compute-shader.md)Direct3D, todos os processadores da GPU são executados em paralelo. Portanto, o sombreador de computação se comporta mais como uma cinza do que um rio.
