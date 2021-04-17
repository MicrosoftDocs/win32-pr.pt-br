---
description: 'Quando um dispositivo é redefinido com êxito (IDirect3DDevice9:: Reset) ou criado (IDirect3D9:: CreateDevice) em operações de tela inteira, o objeto do Direct3D que criou o dispositivo é marcado como proprietário de todos os adaptadores nesse sistema.'
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Operações de Multiple-Monitor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04427db6c91ff85706040589a89f6fdcfb3761e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105762477"
---
# <a name="multiple-monitor-operations-direct3d-9"></a>Operações de Multiple-Monitor (Direct3D 9)

Quando um dispositivo é redefinido com êxito ([**IDirect3DDevice9:: Reset**](/windows/desktop/api)) ou criado ([**IDirect3D9:: CreateDevice**](/windows/desktop/api)) em operações de tela inteira, o objeto do Direct3D que criou o dispositivo é marcado como proprietário de todos os adaptadores nesse sistema. Esse estado é conhecido como modo exclusivo e o objeto Direct3D possui modo exclusivo. Modo exclusivo significa que os dispositivos criados por qualquer outro objeto do Direct3D não podem assumir operações de tela inteira nem alocar memória de vídeo. Além disso, quando um objeto do Direct3D assume um modo exclusivo, todos os dispositivos diferentes daquele que foi colocado em tela inteira são colocados no estado perdido. Para obter detalhes, consulte [dispositivos perdidos (Direct3D 9)](lost-devices.md).

Juntamente com o modo exclusivo, o objeto do Direct3D é informado da janela de foco que o dispositivo usará. O modo exclusivo é liberado quando o dispositivo de tela inteira final de Propriedade do objeto do Direct3D é redefinido para o modo de janela ou destruído.

Os dispositivos podem ser divididos em duas categorias quando um objeto do Direct3D possui um modo exclusivo. A primeira categoria de dispositivos tem as seguintes características.

-   Eles são criados pelo mesmo objeto do Direct3D que criou o dispositivo que está em tela inteira.
-   Eles têm a mesma janela de foco que o dispositivo que está em tela inteira.
-   Eles representam um adaptador diferente de qualquer dispositivo de tela inteira.

Os dispositivos nessa categoria não têm restrições sobre sua capacidade de redefinição ou criação, e eles não são colocados no estado perdido. Os dispositivos nessa categoria podem até mesmo ser colocados no modo de tela inteira.

Dispositivos que não estão na primeira categoria – dispositivos criados por outro objeto do Direct3D, criados com uma janela de foco diferente e criados para um adaptador com um dispositivo que já está em tela inteira-não podem ser redefinidos e permanecer no estado perdido até que o modo exclusivo seja perdido. Como resultado, um aplicativo de vários monitores pode posicionar vários dispositivos no modo de tela inteira, mas somente se todos esses dispositivos forem para adaptadores diferentes, foram criados pelo mesmo objeto do Direct3D e compartilham a mesma janela de foco.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Apresentando uma cena](presenting-a-scene.md)
</dt> </dl>

 

 



