---
description: Um efeito pode ser usado para armazenar informações ou para renderizar usando um grupo de estado.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Renderizando um efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfba9432412846e2dc634d6ab68be999b504e06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163960"
---
# <a name="rendering-an-effect-direct3d-10"></a>Renderizando um efeito (Direct3D 10)

Um efeito pode ser usado para armazenar informações ou para renderizar usando um grupo de estado. Cada técnica especifica sombreadores de vértice, sombreadores de geometria, sombreadores de pixel, estado do sombreador, estado de amostra e textura e outro Estado de pipeline. Assim, depois de organizar o estado em um efeito, você pode encapsular o efeito de renderização que resulta desse Estado criando e renderizando o efeito.

Há algumas etapas para preparar um efeito para a renderização. A primeira é compilar, que verifica o HLSL como código em relação à sintaxe da linguagem HLSL e às regras de estrutura de efeito. Você pode compilar um efeito do seu aplicativo usando chamadas à API ou pode compilar um efeito offline usando o utilitário do compilador de efeito. Depois que o efeito for compilado com êxito, crie-o chamando um conjunto diferente (mas muito semelhante) de APIs.

Depois que o efeito é criado, há duas etapas restantes para usá-lo. Primeiro, você deve inicializar os valores de estado de efeito (os valores das variáveis de efeito) usando vários métodos para definir o estado. Para algumas variáveis, isso pode ser feito uma vez quando um efeito é criado; outras devem ser atualizadas sempre que seu aplicativo chamar o loop de renderização. Depois que as variáveis de efeito são definidas, você informa ao tempo de execução para renderizar o efeito aplicando uma técnica. Esses tópicos são discutidos mais detalhadamente abaixo.

-   [Compilar um efeito (Direct3D 10)](d3d10-graphics-programming-guide-effects-compile.md)
-   [Criar um efeito (Direct3D 10)](d3d10-graphics-programming-guide-effects-create.md)
-   [Definir estado de efeito (Direct3D 10)](d3d10-graphics-programming-guide-effects-set-state.md)
-   [Aplicar uma técnica (Direct3D 10)](d3d10-graphics-programming-guide-effects-apply-technique.md)

Naturalmente, há [considerações de desempenho](d3d10-graphics-programming-guide-effects-performance.md) para o uso de efeitos. Essas considerações são basicamente as mesmas se você não estiver usando um efeito. Coisas como, minimizando a quantidade de alterações de estado ou organizando as variáveis que precisam ser atualizadas por frequência. Essas táticas são usadas para minimizar a quantidade de dados que precisam ser enviados da CPU para a GPU e, portanto, minimizar possíveis problemas de sincronização.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



