---
title: Introdução a multithreading no Direct3D 11
description: O multithreading foi projetado para melhorar o desempenho executando o trabalho usando um ou mais threads ao mesmo tempo.
ms.assetid: b4bef1e4-8d34-455c-8aed-01af974c66c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527b78d8b29a507247c8eb067c20739004ace687
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294081"
---
# <a name="introduction-to-multithreading-in-direct3d-11"></a>Introdução a multithreading no Direct3D 11

O multithreading foi projetado para melhorar o desempenho executando o trabalho usando um ou mais threads ao mesmo tempo.

No passado, isso costuma ser feito gerando um único thread principal para renderização e um ou mais threads para fazer trabalho de preparação, como criação de objeto, carregamento, processamento e assim por diante. No entanto, com a sincronização interna no Direct3D 11, o objetivo por trás do multithreading é utilizar cada ciclo de CPU e GPU sem fazer com que o processador Aguarde um outro processador (particularmente não fazendo a GPU esperar porque ele afeta diretamente a taxa de quadros). Ao fazer isso, você pode gerar a maior quantidade de trabalho, mantendo a melhor taxa de quadros. O conceito de um único quadro para renderização não é mais necessário, pois a API implementa a sincronização.

O multithreading requer alguma forma de sincronização. Por exemplo, se vários threads executados em um aplicativo precisarem acessar um único contexto de dispositivo ([**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)), esse aplicativo deve usar algum mecanismo de sincronização, como seções críticas, para sincronizar o acesso a esse contexto de dispositivo. Isso ocorre porque o processamento dos comandos de renderização (geralmente feitos na GPU) e a geração de comandos de renderização (geralmente feitos na CPU por meio da criação de objeto, carregamento de dados, alteração de estado, processamento de dados) geralmente usam os mesmos recursos (texturas, sombreadores, estado do pipeline e assim por diante). Organizar o trabalho em vários threads requer sincronização para impedir que um thread modifique ou leia dados que estão sendo modificados por outro thread.

Embora o uso de um [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)(contexto de dispositivo) não seja thread-safe, o uso de um dispositivo Direct3D 11 ([**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) é thread-safe. Como cada **ID3D11DeviceContext** é single-threaded, apenas um thread pode chamar um **ID3D11DeviceContext** de cada vez. Se vários threads tiverem que acessar um único **ID3D11DeviceContext**, eles deverão usar algum mecanismo de sincronização, como seções críticas, para sincronizar o acesso a esse **ID3D11DeviceContext**. No entanto, não é necessário que vários threads usem seções críticas ou primitivos de sincronização para acessar um único **ID3D11Device**. Portanto, se um aplicativo usar **ID3D11Device** para criar objetos de recurso, esse aplicativo não precisará usar a sincronização para criar vários objetos de recurso ao mesmo tempo.

O suporte a multithreading divide a API em duas áreas funcionais distintas:

-   [Criação de objeto com multithreading](overviews-direct3d-11-render-multi-thread-create.md)
-   [Renderização imediata e adiada](overviews-direct3d-11-render-multi-thread-render.md)

O desempenho de multithreads depende do suporte do driver. [Como verificar o suporte ao driver](overviews-direct3d-11-render-multi-thread-support.md) fornece mais informações sobre como consultar o driver e o que significam os resultados.

O Direct3D 11 foi projetado desde o início para dar suporte a multithreading. O Direct3D 10 implementa suporte limitado para multithreading usando a [camada thread-safe](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers). Esta página lista as diferenças de comportamento entre as duas versões do DirectX: [segmentação de diferenças entre versões do Direct3D](overviews-direct3d-11-render-multi-thread-differences.md).

## <a name="multithreading-and-dxgi"></a>Multithread e DXGI

Somente um thread por vez deve usar o contexto imediato. No entanto, seu aplicativo também deve usar esse mesmo thread para operações de DXGI (infraestrutura gráfica do Microsoft DirectX), especialmente quando o aplicativo faz chamadas para o método [**IDXGISwapChain::P reenviado**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) .

> [!Note]  
> É inválido usar um contexto imediato simultaneamente com a maioria das funções de interface DXGI. Para os SDKs do DirectX de março de 2009 e posteriores, as únicas funções DXGI que são seguras são [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)e [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

 

Para obter mais informações sobre como usar DXGI com vários threads, consulte [multithread Considerations](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Multithread](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 