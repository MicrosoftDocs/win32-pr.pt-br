---
description: Você pode aprimorar a velocidade percebida de um objeto em uma cena 3D desfocado o objeto e deixando uma trilha desfocado de imagens de objeto atrás do objeto. Os aplicativos Direct3D podem fazer isso renderizar o objeto várias vezes por quadro.
ms.assetid: 8b1a1f0d-5857-4ab4-828c-8ca7c17a4890
title: Desfoque de movimento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3daa0b35a0c375cc798b619f18f1e363001050de4dcc950e6c6828a7d365801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628316"
---
# <a name="motion-blur-direct3d-9"></a>Desfoque de movimento (Direct3D 9)

Você pode aprimorar a velocidade percebida de um objeto em uma cena 3D desfocado o objeto e deixando uma trilha desfocado de imagens de objeto atrás do objeto. Os aplicativos Direct3D podem fazer isso renderizar o objeto várias vezes por quadro.

Lembre-se de que os aplicativos Direct3D normalmente renderizam cenas em um buffer fora da tela. O conteúdo do buffer é exibido na tela quando o aplicativo chama o [**método IDirect3DDevice9::P resent.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) Seu aplicativo Direct3D pode renderizar o objeto várias vezes em uma cena antes de exibir o quadro na tela.

Programaticamente, seu aplicativo faz várias chamadas para um método DrawPrimitive, passando repetidamente o mesmo objeto 3D. Antes de cada chamada, a posição do objeto é atualizada ligeiramente, produzindo uma série de imagens de objeto desfocado na superfície de renderização de destino. Se o objeto tiver uma ou mais texturas, seu aplicativo poderá aprimorar o efeito de desfoque de movimento renderizar a primeira imagem do objeto com todas as texturas quase transparentes. Cada vez que o objeto é render, a transparência da textura do objeto diminui. Quando o aplicativo renderiza o objeto em sua posição final, ele deve renderizar as texturas do objeto sem transparência. A exceção é se você estiver adicionando desfoque de movimento a outro efeito que requer transparência de textura. Em qualquer caso, a imagem inicial do objeto no quadro deve ser a mais transparente. A imagem final deve ser a menos transparente.

Depois que o aplicativo renderizar a série de imagens de objeto na superfície de renderização de destino e renderizar o restante da cena, ele deverá chamar o método [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para exibir o quadro na tela.

Se seu aplicativo estiver simulando o efeito do usuário se movendo por uma cena em alta velocidade, ele poderá adicionar desfoque de movimento a toda a cena. Nesse caso, seu aplicativo renderiza toda a cena várias vezes por quadro. Cada vez que a cena é renderiza, seu aplicativo deve mover um pouco o ponto de vista. Se a cena for altamente complexa, o usuário poderá ver uma degradação visível do desempenho à medida que a aceleração é aumentada devido ao número crescente de renderizações de cena por quadro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suavização](antialiasing.md)
</dt> </dl>

 

 
