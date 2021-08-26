---
description: As APIs de apresentação são um conjunto de métodos que controlam o estado do dispositivo que afeta o que o usuário vê no monitor. Esses métodos incluem a configuração de modos de exibição e métodos uma vez por quadro usados para apresentar imagens ao usuário.
ms.assetid: fb2ddc0d-50ac-48aa-8a5c-f232b0f8e7aa
title: Introdução à apresentação de uma cena (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9abf584bad1bfbbde2bbfa2e9281acf3ad2173403507e06bbdc2abc5f5edd1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846546"
---
# <a name="introduction-to-presenting-a-scene-direct3d-9"></a>Introdução à apresentação de uma cena (Direct3D 9)

As APIs de apresentação são um conjunto de métodos que controlam o estado do dispositivo que afeta o que o usuário vê no monitor. Esses métodos incluem a configuração de modos de exibição e métodos uma vez por quadro usados para apresentar imagens ao usuário.

-   [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
-   [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
-   [**IDirect3DDevice9::GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
-   [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
-   [**IDirect3DDevice9::GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)

A familiaridade com os termos a seguir é necessária para entender as APIs de apresentação.

-   buffer frontal. Um retângulo de memória que é convertido pelo adaptador de gráficos e exibido no monitor ou em outro dispositivo de saída.
-   buffer de fundo. Uma superfície cujo conteúdo pode ser promovido para o buffer frontal.
-   cadeia de permuta. Uma coleção de buffers de fundo que podem ser apresentados serialmente ao buffer frontal. Normalmente, uma cadeia de permuta de tela inteira apresenta imagens subsequentes com a DDI (interface de driver de dispositivo invertida) e uma cadeia de permuta em janelas apresenta imagens com o DDI blitting.

Como o Direct3D 9 tem uma cadeia de permuta como uma propriedade do dispositivo, sempre há pelo menos uma cadeia de permuta por dispositivo. A interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) tem um conjunto de métodos que manipulam a cadeia de permuta implícita e são uma cópia da própria interface da cadeia de permuta. Os aplicativos podem criar cadeias de permuta adicionais; no entanto, isso não é necessário para o aplicativo típico de janela única ou de tela inteira.

O buffer frontal não é exposto diretamente no Direct3D 9. Como resultado, os aplicativos não podem bloquear ou renderizar no buffer frontal. Para obter detalhes, [consulte Acessando o buffer frontal de cores (Direct3D 9)](accessing-the-color-front-buffer.md).

> [!Note]  
> O DirectX 7 forneceu várias APIs de apresentação que foram chamadas juntas. Um bom exemplo disso é a sequência IDirectDraw7::SetCooperativeLevel, IDirectDraw7::SetDisplayMode e IDirectDraw7::CreateSurface. Além disso, os métodos IDirectDrawSurface7::Flip e IDirectDrawSurface7::Blt sinalizaram o transporte de quadros renderizados para o monitor. O Direct3D 9 colapsa esses grupos de APIs em dois métodos principais, Redefinir e Apresentar. Redefinir subsumes SetCooperativeLevel, SetDisplayMode, CreateSurface e alguns dos parâmetros a inverter. Os subsumes presentes são inversão e a apresentação usa blit.

 

Uma chamada para [**IDirect3D9::CreateDevice representa**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) uma redefinição implícita do dispositivo. A API do Direct3D 9 não tem noção de uma superfície primária; não é possível criar um objeto que representa a superfície primária. Ele é considerado uma propriedade interna do dispositivo.

As rampas gama são associadas a uma cadeia de permuta e são manipuladas com os métodos [**IDirect3DDevice9::GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) e [**IDirect3DDevice9::SetGammaRamp.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Apresentando uma cena](presenting-a-scene.md)
</dt> </dl>

 

 
