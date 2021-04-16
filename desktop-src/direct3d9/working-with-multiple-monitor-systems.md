---
description: 'O conceito de modo de tela inteira exclusivo é mantido no Direct3D 9, mas é mantido totalmente implícito nas chamadas de método IDirect3D9:: CreateDevice e IDirect3DDevice9:: Reset.'
ms.assetid: c3503d62-d9f9-4eec-8af3-ebcbfe7064d4
title: Trabalhando com vários sistemas de monitor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184a11f06d2296100a0b546e29770f44977b4de3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105768810"
---
# <a name="working-with-multiple-monitor-systems-direct3d-9"></a>Trabalhando com vários sistemas de monitor (Direct3D 9)

O conceito de modo de tela inteira exclusivo é mantido no Direct3D 9, mas é mantido totalmente implícito nas chamadas de método [**IDirect3D9:: CreateDevice**](/windows/desktop/api) e [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) . Sempre que um dispositivo é redefinido com êxito ou criado na operação de tela inteira, o objeto do Direct3D que criou o dispositivo é marcado como proprietário de todos os adaptadores nesse sistema. Esse estado é conhecido como modo exclusivo e, neste ponto, o objeto Direct3D possui modo exclusivo. O modo exclusivo significa que os dispositivos criados por qualquer outro objeto de Direct3D9 não podem assumir a operação de tela inteira nem alocar memória de vídeo. Além disso, quando um objeto de Direct3D9 assume o modo exclusivo, todos os dispositivos que não sejam o dispositivo que estava em tela inteira são colocados no estado perdido. Para obter informações sobre como lidar com dispositivos perdidos, consulte [dispositivos perdidos (Direct3D 9)](lost-devices.md).

Juntamente com o modo exclusivo, o objeto do Direct3D9 é informado da janela de foco a ser usada pelo dispositivo. O modo exclusivo é liberado quando o último dispositivo de tela inteira pertencente a esse objeto de Direct3D9 é redefinido para o modo de janela ou destruído.

Os dispositivos podem ser divididos em duas categorias quando um objeto de Direct3D9 possui um modo exclusivo. A primeira categoria de dispositivos é aquela que foi criada pelo mesmo objeto Direct3D9 que criou o dispositivo que já está em tela inteira, que tem a mesma janela de foco que o dispositivo que já está em tela inteira e representa um adaptador diferente de qualquer dispositivo de tela inteira. Os dispositivos nessa categoria não têm restrições sobre sua capacidade de redefinição ou criação e não são colocados no estado perdido. Os dispositivos nessa categoria podem até mesmo ser colocados no modo de tela inteira.

Os dispositivos que não estão nessa categoria, que seriam aqueles criados por um objeto de Direct3D9 diferente ou com uma janela de foco diferente, ou para algum adaptador com um dispositivo já em tela inteira, não podem ser redefinidos e permanecem no estado perdido até que o modo exclusivo seja perdido.

A implicação prática é que um aplicativo de vários monitores pode posicionar vários dispositivos no modo de tela inteira, mas somente se todos esses dispositivos forem para adaptadores diferentes, foram criados pelo mesmo objeto de Direct3D9 e todos compartilham a mesma janela de foco.

Quando você cria um novo dispositivo usando o mesmo objeto [**IDirect3D9**](/windows/desktop/api) e janela de foco, seu dispositivo original perderá suas superfícies. Será necessário chamar [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) no primeiro dispositivo para que seu aplicativo o use. Por exemplo, para criar dois dispositivos, faça o seguinte:

1.  Criar dispositivo 1
2.  Criar dispositivo 2
3.  Redefinir o dispositivo 1

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dicas de programação](programming-tips.md)
</dt> </dl>

 

 
