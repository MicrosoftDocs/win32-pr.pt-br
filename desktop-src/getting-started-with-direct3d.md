---
description: O Direct3D é uma API de nível baixo para desenhar primitivos com o pipeline de renderização ou executar operações paralelas com o sombreador de computação.
ms.assetid: 55063BF2-34A3-4E56-882C-86F0949DE557
title: Introdução ao Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2b5a579b589a747c4e7640b3c868d488a7e58f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771624"
---
# <a name="getting-started-with-direct3d"></a>Introdução ao Direct3D

O Direct3D é uma API de nível baixo para desenhar primitivos com o pipeline de renderização ou para executar operações paralelas com o sombreador de computação.

## <a name="what-is-direct3d"></a>O que é o Direct3D?

O Direct3D é uma API de nível baixo que você pode usar para desenhar triângulos, linhas ou pontos por quadro, ou para iniciar operações altamente paralelas na GPU.

Avalia

-   Oculta diferentes implementações de GPU por trás de uma abstração coerente. Mas você ainda precisa saber como desenhar gráficos 3D.
-   Foi projetado para impulsionar um processador separado para gráficos separados. As GPUs mais novas têm centenas ou milhares de processadores paralelos.
-   Enfatiza o processamento paralelo. Você configura uma porção de processamento ou estado de computação e, em seguida, inicia uma operação. Você não espera por comentários imediatos da operação. Você não combina operações de CPU e GPU.

## <a name="which-direct3d-apis-can-you-use"></a>Quais APIs do Direct3D você pode usar?

As APIs do Direct3D escolhidas dependem do estilo do aplicativo que você deseja escrever.

-   Se você quiser escrever um aplicativo UWP, use um subconjunto de APIs do Direct3D 11, DXGI e HLSL. Para obter uma lista dessas APIs, consulte [Win32 e APIs com para aplicativos UWP](/uwp/win32-and-com/win32-and-com-for-uwp-apps). Para saber como escrever um aplicativo da Windows Store do Direct3D 11, consulte [criar gráficos 3D com DirectX](/previous-versions/windows/apps/hh465137(v=win.10)).
-   Se você escrever um aplicativo de área de trabalho, poderá usar o conjunto completo de APIs do Direct3D 11, DXGI e HLSL.
-   A partir do Windows 8, não damos mais suporte ao XNA Framework para aplicativos de desktop. Mas os aplicativos da Windows Store, os aplicativos UWP e os aplicativos da área de trabalho podem usar o conjunto completo das APIs [XAudio2](/windows/desktop/xaudio2/xaudio2-apis-portal) e [DirectXMath](/windows/desktop/dxmath/directxmath-portal) . Os aplicativos da área de trabalho podem usar o conjunto completo de APIs do [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) , enquanto aplicativos da Windows Store e aplicativos UWP podem usar a maioria das APIs do XInput; para obter mais informações, consulte [versões do XInput](/windows/desktop/xinput/xinput-versions).

## <a name="which-direct3d-version"></a>Qual versão do Direct3D?

A versão da API do Direct3D que você escolher depende do sistema operacional e do nível de hardware que você deseja direcionar.

-   Se você quiser direcionar o Windows 8 e versões posteriores, use as APIs do Direct3D 11.
-   Use as APIs do Direct3D 9 com o Windows XP e versões posteriores. Todo o hardware dá suporte a APIs do Direct3D 9, até mesmo hardware de nível mais novo do Direct3D 11.
-   Use as APIs do Direct3D 10 com o Windows Vista e posterior. Somente o hardware do Direct3D 10 de nível e posterior dá suporte a APIs do Direct3D 10.
-   Use as APIs do Direct3D 10,1 e do Direct3D 11 com o Windows 7 e posterior. Você também pode usar as APIs do Direct3D 10,1 e do Direct3D 11 com o Windows Vista com Service Pack 2 (SP2) baixando [KB 971644](https://support.microsoft.com/kb/971644).

## <a name="direct3d-rendering-pipeline"></a>Pipeline de renderização do Direct3D

No pipeline de [renderização](./direct3d11/overviews-direct3d-11-graphics-pipeline.md)do Direct3D, os dados fluem de várias fontes, como os condados de um rio.

-   Algumas partes do fluxo são programáveis.
-   Algumas partes têm botões e discagens.
-   As fontes de dados são fluxos de série de pacotes (vértices) ou matrizes indexáveis (recursos de sombreador).
-   Os recursos de vértices e sombreador fluem em primitivos, que você pode ampliar.
-   Os primitivos e os recursos de sombreador fluem em operações de pixel.

## <a name="direct3d-compute-shader"></a>Sombreador do Direct3D Compute

Com o [sombreador](./direct3d11/direct3d-11-advanced-stages-compute-shader.md)do Direct3D Compute, todos os processadores da GPU são executados em paralelo. Portanto, o sombreador de computação se comporta mais como um lago do que um rio.
