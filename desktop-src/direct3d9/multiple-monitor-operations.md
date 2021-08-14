---
description: Quando um dispositivo é redefinido com êxito (IDirect3DDevice9::Reset) ou criado (IDirect3D9::CreateDevice) em operações de tela inteira, o objeto Direct3D que criou o dispositivo é marcado como sendo de propriedade de todos os adaptadores nesse sistema.
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Multiple-Monitor operações de Multiple-Monitor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4f175c136cd432223eeaaf32cf44bfbb08e724b54b8afe1dbb9717c2d79a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728206"
---
# <a name="multiple-monitor-operations-direct3d-9"></a>Multiple-Monitor operações de Multiple-Monitor (Direct3D 9)

Quando um dispositivo é redefinido com êxito ([**IDirect3DDevice9::Reset**](/windows/desktop/api)) ou criado ([**IDirect3D9::CreateDevice**](/windows/desktop/api)) em operações de tela inteira, o objeto Direct3D que criou o dispositivo é marcado como sendo o próprio de todos os adaptadores nesse sistema. Esse estado é conhecido como modo exclusivo e o objeto Direct3D possui o modo exclusivo. Modo exclusivo significa que os dispositivos criados por qualquer outro objeto Direct3D não podem assumir operações de tela inteira nem alocar memória de vídeo. Além disso, quando um objeto Direct3D assume o modo exclusivo, todos os dispositivos que não foram de tela inteira são colocados em estado perdido. Para obter detalhes, consulte [Dispositivos perdidos (Direct3D 9)](lost-devices.md).

Juntamente com o modo exclusivo, o objeto Direct3D é informado da janela de foco que o dispositivo usará. O modo exclusivo é liberado quando o dispositivo de tela inteira final pertencente a esse objeto Direct3D é redefinido para o modo de janela ou destruído.

Os dispositivos podem ser divididos em duas categorias quando um objeto Direct3D possui o modo exclusivo. A primeira categoria de dispositivos tem as seguintes características.

-   Eles são criados pelo mesmo objeto Direct3D que criou o dispositivo que é de tela inteira.
-   Eles têm a mesma janela de foco que o dispositivo que é de tela inteira.
-   Eles representam um adaptador diferente de qualquer dispositivo de tela inteira.

Os dispositivos nessa categoria não têm restrições em relação à capacidade de redefinição ou criação e não são colocados em estado perdido. Os dispositivos nessa categoria podem até mesmo ser colocados no modo de tela inteira.

Dispositivos que não se enquadram na primeira categoria – dispositivos criados por outro objeto Direct3D, criados com uma janela de foco diferente e criados para um adaptador com um dispositivo que já está em tela inteira – não podem ser redefinidos e permanecem no estado perdido até que o modo exclusivo seja perdido. Como resultado, um aplicativo de vários monitores pode colocar vários dispositivos no modo de tela inteira, mas somente se todos esses dispositivos são para adaptadores diferentes, foram criados pelo mesmo objeto Direct3D e compartilham a mesma janela de foco.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Apresentando uma cena](presenting-a-scene.md)
</dt> </dl>

 

 



