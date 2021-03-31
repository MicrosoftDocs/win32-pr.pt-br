---
title: A interface do usuário do Edge é suprimida nos cenários "in-out" e "inércia"
description: A interface do usuário do Edge é suprimida nos cenários "in-out" e "inércia"
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef08eab653349beab0710d59d45bedc2874ced44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160369"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a>A interface do usuário do Edge é suprimida nos cenários "in-out" e "inércia"

## <a name="platform"></a>Plataforma

<dl> Clientes-Windows 8.1  
</dl>

## <a name="description"></a>Descrição

Há alguns casos em que os usuários podem invocar involuntariamente a interface do usuário do Edge (botões, a barra de aplicativos e a troca de aplicativos). Apresentamos um recurso para permitir que os desenvolvedores projetem sua interface do usuário para toda a tela sem fazer capacidades (por exemplo, bordas) para impedir que o usuário acesse acidentalmente as bordas.

Há dois casos que podem levar mais frequência a endedor de borda inadvertidamente:

-   No panorama rápido, a velocidade e a imprecisão da interação podem ocasionalmente fazer com que elas venham da borda da tela
-   Se os usuários saírem e reinserirem rapidamente a área da tela durante a criação de tinta com o dedo, por exemplo, em um aplicativo de pintura, esse comportamento de entrada pode acionar erroneamente a interface do usuário do Edge e interromper a experiência

Para melhorar a experiência do usuário e do desenvolvedor, a interface de usuário do Edge agora será suprimida em duas instâncias específicas:

-   Quando um usuário está panorâmica em um aplicativo que dá suporte a DManip inércia e passa para fora da tela enquanto o inércia está ocorrendo, a interface do usuário do Edge não será invocada dentro de uma janela de tempo limite
-   Em dispositivos certificados, quando um usuário passa rapidamente de dentro da tela para fora da tela e volta para dentro (movimento interno) dentro de determinados parâmetros, a interface do usuário do Edge não será invocada

## <a name="manifestations"></a>Manifestações

Os usuários que passarem rapidamente para a borda ao usar um aplicativo verão uma redução na invocação de borda não intencional.

## <a name="solution"></a>Solução

Os desenvolvedores devem manter essas atenuações em mente e devem ser capazes de usar a tela inteira sem medo de que os usuários dispararão acidentalmente a interface do usuário do Edge enquanto interagem com o aplicativo ao longo do limite.

 

 




