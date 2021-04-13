---
description: Além da cadeia de permuta que é proprietária e manipulada por meio da interface IDirect3DDevice9, um aplicativo pode criar cadeias de permuta adicionais para apresentar várias exibições do mesmo dispositivo.
ms.assetid: 4fc09b9c-7adb-4f5d-80e0-2d39bc10420e
title: Apresentando várias exibições no modo de janela (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 039b02c487e06c7464dc8163c719371dc2b23706
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500729"
---
# <a name="presenting-multiple-views-in-windowed-mode-direct3d-9"></a>Apresentando várias exibições no modo de janela (Direct3D 9)

Além da cadeia de permuta que é proprietária e manipulada por meio da interface [**IDirect3DDevice9**](/windows/desktop/api) , um aplicativo pode criar cadeias de permuta adicionais para apresentar várias exibições do mesmo dispositivo. O aplicativo normalmente cria uma cadeia de permuta por exibição usando o método [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) e associa cada cadeia de permuta a uma janela específica. O aplicativo renderiza as imagens nos buffers de fundo de cada cadeia de permuta e as apresenta individualmente.

Apenas uma cadeia de troca de cada vez pode ser de tela inteira em cada adaptador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dicas de programação](programming-tips.md)
</dt> </dl>

 

 
