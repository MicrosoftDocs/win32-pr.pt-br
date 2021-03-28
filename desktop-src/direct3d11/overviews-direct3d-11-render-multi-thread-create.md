---
title: Criação de objeto com multithreading
description: Use a interface ID3D11Device para criar recursos e objetos, use o ID3D11DeviceContext para renderização.
ms.assetid: e1765192-865c-4a62-9be7-6e95280ee8ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cbfbe73efc96b301216deb5ccbf623354ddbb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916295"
---
# <a name="object-creation-with-multithreading"></a>Criação de objeto com multithreading

Use a interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) para criar recursos e objetos, use o [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) para [renderização](overviews-direct3d-11-render-multi-thread-render.md).

Aqui estão alguns exemplos de como criar recursos:

-   [Como criar um buffer de vértice](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
-   [Como: criar um buffer de índice](overviews-direct3d-11-resources-buffers-index-how-to.md)
-   [Como: criar um buffer de constantes](overviews-direct3d-11-resources-buffers-constant-how-to.md)
-   [Como: inicializar uma textura a partir de um arquivo](overviews-direct3d-11-resources-textures-how-to.md)

## <a name="multithreading-considerations"></a>Considerações de multithread

A quantidade de simultaneidade de criação de recursos e renderização que seu aplicativo pode atingir depende do nível de suporte multithreading que o Driver implementa. Se o driver oferecer suporte a criações simultâneas, o aplicativo deverá ter problemas de simultaneidade muito menos. No entanto, se o driver não oferecer suporte à criação simultânea de objeto, a quantidade de simultaneidade será extremamente limitada. Para entender a quantidade de suporte disponível em um driver, consulte o driver para obter o valor do membro **DriverConcurrentCreates** da estrutura [**de \_ \_ \_ Threading de dados do recurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) . Para obter mais informações sobre como verificar o suporte de driver de multithreading, consulte [como verificar o suporte ao driver](overviews-direct3d-11-render-multi-thread-support.md).

As operações simultâneas não levam necessariamente ao melhor desempenho. Por exemplo, criar e carregar uma textura normalmente é limitado pela largura de banda da memória. A tentativa de criar e carregar várias texturas pode não ser mais rápida do que fazer uma textura de cada vez, mesmo que isso deixe vários núcleos de CPU ociosos. No entanto, a criação de vários sombreadores usando vários threads pode aumentar o desempenho, pois essa operação é menos dependente dos recursos do sistema, como a largura de banda da memória.

Quando o driver e o hardware de gráficos dão suporte a multithreading, normalmente é possível inicializar recursos recém-criados com mais eficiência, passando um ponteiro para dados iniciais no parâmetro *pInitialData* (por exemplo, em uma chamada para o método [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) ).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




