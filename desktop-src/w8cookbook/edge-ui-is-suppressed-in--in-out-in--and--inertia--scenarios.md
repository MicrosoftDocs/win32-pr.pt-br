---
title: A interface do usuário do Edge é suprimida em cenários de "entrada/saída" e "inércia"
description: A interface do usuário do Edge é suprimida em cenários de "entrada/saída" e "inércia"
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec032fa97f54fc1b1325055c9b02bdebe9e817b0f85971c2e2a7062e93c284c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593956"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a>A interface do usuário do Edge é suprimida em cenários de "entrada/saída" e "inércia"

## <a name="platform"></a>Plataforma

<dl> Clientes – Windows 8.1  
</dl>

## <a name="description"></a>Descrição

Há alguns casos em que os usuários podem invocar sem querer a interface do usuário do Edge (Charms, Barra de Aplicativos, alternação de aplicativos). Apresentamos um recurso para permitir que os desenvolvedores projetem sua interface do usuário para toda a tela sem criar funcionalidades (por exemplo, bordas) para impedir que o usuário atinja acidentalmente as bordas.

Há dois casos que podem levar com mais frequência a passar o dedo de borda inadvertida:

-   Em um panorâmico rápido, a velocidade e a imprecisão da interação ocasionalmente podem fazer com que eles entre na borda da tela
-   Se os usuários sairem rapidamente e entrarem na área da tela enquanto estão de frente com o dedo, por exemplo, em um aplicativo de pintura, esse comportamento de entrada pode disparar por engano a interface do usuário do Edge e interromper a experiência do usuário

Para melhorar a experiência do usuário e do desenvolvedor, a interface do usuário do Edge agora será suprimida em duas instâncias específicas:

-   Quando um usuário estiver panorâmico em um aplicativo que dá suporte à Inércia DManip e passar o dedo para fora da tela enquanto a inércia estiver ocorrendo, a interface do usuário do Edge não será invocada em uma janela de tempo limite
-   Em dispositivos certificados, quando um usuário passa o dedo rapidamente de dentro da tela para fora da tela e volta para dentro (movimento de entrada) dentro de determinados parâmetros, a interface do usuário do Edge não será invocada

## <a name="manifestations"></a>Manifestações

Os usuários que deslizarem rapidamente para a borda ao usar um aplicativo verão uma diminuição na invocação de borda não intencional.

## <a name="solution"></a>Solução

Os desenvolvedores devem ter essas mitigações em mente e devem ser capazes de usar a tela inteira sem medo de que os usuários dispararão acidentalmente a interface do usuário do Edge ao interagir com o aplicativo ao longo da borda.

 

 




