---
title: Diretrizes da interface do usuário para extensões de classe auxiliar NDF
description: Ao criar sua classe auxiliar, você precisará criar um texto para ajudar o usuário a entender a causa de um incidente e as possíveis etapas de reparo que podem ser tomadas.
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e48357ba6561ab135e2c341409c22d1edf3fb7d
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104293541"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a>Diretrizes da interface do usuário para extensões de classe auxiliar NDF

Ao criar sua classe auxiliar, você precisará criar um texto para ajudar o usuário a entender a causa de um incidente e as possíveis etapas de reparo que podem ser tomadas.

## <a name="root-cause-and-repair"></a>Causa e reparo raiz

Quando ocorrer um incidente, uma caixa de diálogo será exibida para informar o usuário sobre o que aconteceu. O texto que você cria aparecerá em duas áreas separadas.

-   **Causa raiz**: uma breve descrição da causa do problema. Contém informações para ajudar um administrador ou usuário avançado a solucionar o problema.
-   **Reparo**: expande a causa raiz para fornecer mais detalhes sobre as etapas que um usuário pode executar, sem ficar muito demorado.

Cada causa ou reparo raiz deve ter um título e uma descrição. Todo o texto antes do primeiro \\ caractere "n" será usado para o título. Todo o texto após o primeiro \\ caractere "n" (incluindo todas as quebras de linha subsequentes) será usado para a descrição.

## <a name="title-guidelines"></a>Diretrizes de título

O título de uma causa raiz ou reparo deve seguir estas diretrizes:

-   Deve ter de 128 caracteres ou menos. (recomenda-se 40 caracteres ou menos).
-   Não deve terminar com um ponto.

## <a name="description-guidelines"></a>Diretrizes de descrição

A descrição de uma causa raiz ou reparo deve seguir estas diretrizes:

-   Deve ter de 512 caracteres ou menos.
-   Cada frase deve terminar com um ponto.
-   O \\ caractere "n" pode ser usado para criar uma quebra de linha na descrição.

 

 




