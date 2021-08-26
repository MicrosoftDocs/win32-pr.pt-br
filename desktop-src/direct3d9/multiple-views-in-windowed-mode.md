---
description: 'Além da cadeia de permuta que é proprietária e manipulada por meio do objeto Direct3DDevice, um aplicativo pode usar o método IDirect3DDevice9:: CreateAdditionalSwapChain para criar cadeias de permuta adicionais para apresentar várias exibições do mesmo dispositivo.'
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: Várias exibições no modo de janela (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2784a4f2bd855293e427aa9297d2e5725a74a3f5bce52b4b53cdf3d9081062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069016"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a>Várias exibições no modo de janela (Direct3D 9)

Além da cadeia de permuta que é proprietária e manipulada por meio do objeto Direct3DDevice, um aplicativo pode usar o método [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) para criar cadeias de permuta adicionais para apresentar várias exibições do mesmo dispositivo.

Normalmente, o aplicativo cria uma cadeia de permuta por exibição e associa cada cadeia de troca a uma determinada exibição. O aplicativo renderiza as imagens nos buffers de fundo de cada cadeia de permuta e, em seguida, usa o método [**IDirect3DDevice9::P Resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para apresentá-las individualmente. Observe que apenas uma cadeia de permuta por vez pode ser de tela inteira em cada adaptador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Apresentando uma cena](presenting-a-scene.md)
</dt> </dl>

 

 
