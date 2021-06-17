---
description: Saiba mais sobre como renderizar um efeito para o Direct3D 10. Um efeito pode ser usado para armazenar informações ou renderizar usando um grupo de estado.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Renderizar um efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79db595585c6587648fba12afa5fbb22ff33e845
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262568"
---
# <a name="rendering-an-effect-direct3d-10"></a>Renderizar um efeito (Direct3D 10)

Um efeito pode ser usado para armazenar informações ou renderizar usando um grupo de estado. Cada técnica especifica sombreadores de vértice, sombreadores de geometria, sombreadores de pixel, estado do sombreador, estado de amostra e textura e outro estado de pipeline. Portanto, depois de organizar o estado em um efeito, você pode encapsular o efeito de renderização que resulta desse estado criando e renderizar o efeito.

Há algumas etapas para preparar um efeito para renderização. A primeira é a compilação, que verifica o código HLSL como em relação à sintaxe da linguagem HLSL e às regras da estrutura de efeito. Você pode compilar um efeito de seu aplicativo usando chamadas à API ou pode compilar um efeito offline usando o utilitário do compilador de efeito. Depois que o efeito for compilado com êxito, crie-o chamando um conjunto diferente (mas muito semelhante) de APIs.

Depois que o efeito é criado, há duas etapas restantes para usá-lo. Primeiro, você deve inicializar os valores de estado de efeito (os valores das variáveis de efeito) usando vários métodos para definir o estado. Para algumas variáveis, isso pode ser feito uma vez quando um efeito é criado; outros devem ser atualizados sempre que seu aplicativo chamar o loop de renderização. Depois que as variáveis de efeito são definidas, você diz ao runtime para renderizar o efeito aplicando uma técnica. Todos esses tópicos são discutidos mais detalhadamente abaixo.

-   [Compilar um efeito (Direct3D 10)](d3d10-graphics-programming-guide-effects-compile.md)
-   [Criar um efeito (Direct3D 10)](d3d10-graphics-programming-guide-effects-create.md)
-   [Definir estado de efeito (Direct3D 10)](d3d10-graphics-programming-guide-effects-set-state.md)
-   [Aplicar uma técnica (Direct3D 10)](d3d10-graphics-programming-guide-effects-apply-technique.md)

Naturalmente, há [considerações de desempenho](d3d10-graphics-programming-guide-effects-performance.md) para usar efeitos. Essas considerações são, em grande parte, as mesmas se você não estiver usando um efeito. Coisas como minimizar a quantidade de alterações de estado ou organizar as variáveis que precisam ser atualizadas por frequência. Essas táticas são usadas para minimizar a quantidade de dados que precisam ser enviados da CPU para a GPU e, portanto, minimizar possíveis problemas de sincronização.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



