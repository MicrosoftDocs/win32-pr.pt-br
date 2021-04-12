---
title: A funcionalidade do aplicativo de desktop será afetada se não for executada no modo de janela
description: No Windows 10, os aplicativos do Windows não estão mais em tela inteira por padrão – em vez disso, eles são janelas e operações como minimizar, restaurar, maximizar, redimensionar (e qualquer outra operação que você sempre conseguiu fazer em qualquer outra janela de aplicativo do Windows clássica) agora é possível.
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aae44fda5847e5b86616b40ab1bf4ab8cbd206b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364282"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a>A funcionalidade do aplicativo de desktop será afetada se não for executada no modo de janela

No Windows 10, os aplicativos do Windows não estão mais em tela inteira por padrão – em vez disso, eles são janelas e operações como minimizar, restaurar, maximizar, redimensionar (e qualquer outra operação que você sempre conseguiu fazer em qualquer outra janela de aplicativo do Windows clássica) agora é possível.

## <a name="manifestations"></a>Manifestações

A alteração mais perceptível agora é que você pode ser dimensionado para tamanhos arbitrários que não são apenas o tamanho da tela/altura da tela. Um usuário pode redimensionar continuamente a janela do aplicativo para sua preferência (até o tamanho mínimo da janela do aplicativo). Isso é diferente do Windows 8,0 ou Windows 8.1, em que o ato de redimensionar uma janela era uma ação discreta (os usuários redimensionaram uma miniatura da janela, o que, em seguida, fazia com que a janela fosse redimensionada quando o usuário confirmou a ação). Hoje em diante, quando o usuário arrasta a janela pelo canto inferior (ou outro local de borda), ele é um redimensionamento contínuo e o aplicativo recebe as mensagens de redimensionamento em uma linha, em vez da alteração de tamanho.

## <a name="mitigations"></a>Atenuações

Para mitigar isso para aplicativos do Windows 8,0 e 8,1:

-   Se o recurso esperado dentro da funcionalidade do aplicativo for interrompido, a mitigação do usuário será posicionar o aplicativo no modo de tela inteira (usando o botão "ir para a tela inteira" no canto superior direito da barra de título).
-   Se a inicialização do aplicativo for afetada de que ele não é aberto conforme o esperado, o usuário ainda deverá ser capaz de alternar para o modo tablet para forçar o aplicativo a ser iniciado no modo de tela inteira sem intervenção do usuário.

A melhor maneira de lidar com isso é alterar o aplicativo para estar ciente do fato de que ele pode ser dimensionado para locais/alturas de tamanho não-monitor (ou seja, não ter uma tabela codificada de altura/largura e esperar apenas aquelas, ou esperar também taxas codificadas). Os desenvolvedores de aplicativos devem esperar que, à medida que o aplicativo é redimensionado, que outra mensagem de redimensionamento possa ocorrer logo após a entrega da mensagem de redimensionamento atual – como resultado, se o aplicativo iniciar animações durante o redimensionamento, é possível que o aplicativo receba outra mensagem de redimensionamento logo após (portanto, é importante garantir que esse tipo de situação não cause

 

 




