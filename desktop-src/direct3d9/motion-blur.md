---
description: Você pode aprimorar a velocidade percebida de um objeto em uma cena 3D desfocando o objeto e deixando uma trilha borrada de imagens de objeto por trás do objeto. Os aplicativos Direct3D realizam isso renderizando o objeto várias vezes por quadro.
ms.assetid: 8b1a1f0d-5857-4ab4-828c-8ca7c17a4890
title: Desfoque de movimento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fccb5c00d1208041afc31d4afe1cf0c7a5425037
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500517"
---
# <a name="motion-blur-direct3d-9"></a>Desfoque de movimento (Direct3D 9)

Você pode aprimorar a velocidade percebida de um objeto em uma cena 3D desfocando o objeto e deixando uma trilha borrada de imagens de objeto por trás do objeto. Os aplicativos Direct3D realizam isso renderizando o objeto várias vezes por quadro.

Lembre-se de que os aplicativos do Direct3D normalmente renderizam cenas em um buffer fora da tela. O conteúdo do buffer é exibido na tela quando o aplicativo chama o método [**IDirect3DDevice9::P reenviado**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) . O aplicativo do Direct3D pode renderizar o objeto várias vezes em uma cena antes de exibir o quadro na tela.

Programaticamente, seu aplicativo faz várias chamadas para um método DrawPrimitive, passando repetidamente o mesmo objeto 3D. Antes de cada chamada, a posição do objeto é ligeiramente atualizada, produzindo uma série de imagens de objeto desfocada na superfície de renderização de destino. Se o objeto tiver uma ou mais texturas, seu aplicativo poderá aprimorar o efeito de desfoque de movimento renderizando a primeira imagem do objeto com todas as suas texturas quase transparentes. Cada vez que o objeto é renderizado, a transparência da textura do objeto diminui. Quando seu aplicativo renderiza o objeto em sua posição final, ele deve renderizar as texturas do objeto sem transparência. A exceção é se você estiver adicionando um desfoque de movimento a outro efeito que requer transparência de textura. Em qualquer caso, a imagem inicial do objeto no quadro deve ser a mais transparente. A imagem final deve ser a menos transparente.

Depois que o aplicativo renderiza a série de imagens de objeto na superfície de renderização de destino e renderiza o restante da cena, ele deve chamar o método [**IDirect3DDevice9::P reenviado**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para exibir o quadro na tela.

Se seu aplicativo estiver simulando o efeito do usuário passando por uma cena em alta velocidade, ele poderá adicionar desfoque de movimento à cena inteira. Nesse caso, seu aplicativo renderiza toda a cena várias vezes por quadro. Cada vez que a cena é renderizada, seu aplicativo deve mover um pouco o ponto de vista. Se a cena for altamente complexa, o usuário poderá ver uma degradação de desempenho visível conforme a aceleração é aumentada devido ao número crescente de renderizações de cena por quadro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suavização](antialiasing.md)
</dt> </dl>

 

 
