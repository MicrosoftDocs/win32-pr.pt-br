---
description: Um buffer de profundidade, geralmente chamado de buffer z ou buffer w, é uma propriedade do dispositivo que armazena informações de profundidade a serem usadas pelo Direct3D.
ms.assetid: vs|directx_sdk|~\depth_buffers.htm
title: Buffers de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1ab41ba98ca5e3b08980ac90a572a19fc8a72a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456582"
---
# <a name="depth-buffers-direct3d-9"></a>Buffers de profundidade (Direct3D 9)

Um buffer de profundidade, geralmente chamado de buffer z ou buffer w, é uma propriedade do dispositivo que armazena informações de profundidade a serem usadas pelo Direct3D. Quando o Direct3D renderiza uma cena para uma superfície de destino, ele pode usar a memória em uma superfície de buffer de profundidade associado como um espaço de trabalho para determinar como os pixels dos polígonos rasterizados ocultam uns aos outros. O Direct3D usa uma superfície Direct3D fora da tela como o destino no qual os valores de cor finais são gravados. A superfície de buffer de profundidade que está associada com a superfície de destino de renderização é usada para armazenar informações de profundidade que indicam ao Direct3D qual a profundidade de cada pixel visível na cena.

Quando uma cena é rasterizada com o buffer de profundidade habilitado, cada ponto na superfície de renderização é testado. Os valores no buffer de profundidade podem ser uma coordenada z do ponto ou sua coordenada w homogênea - a partir da localização do ponto (x, y, z, w) no espaço de projeção. Um buffer de profundidade que usa valores z é geralmente chamado de buffer z e um que usa valores w é chamado de buffer w. Cada tipo de buffer de profundidade tem vantagens e desvantagens, que são discutidas posteriormente.

No início do teste, o valor de profundidade no buffer de profundidade é definido como o maior valor possível para a cena. O valor de cor na superfície de renderização é definido como o valor de cor de plano de fundo ou o valor da cor da textura em segundo plano nesse ponto. Cada polígono na cena é testado para verificar se cruza com a coordenada atual (x, y) na superfície de renderização. Se tiver, o valor de profundidade, que será a coordenada z em um buffer z, e a coordenada w em um buffer w-no ponto atual será testada para ver se ela é menor do que o valor de profundidade armazenado no buffer de profundidade. Se a profundidade do valor do polígono for menor, ele é armazenado no buffer de profundidade e o valor de cor do polígono é gravado para o ponto atual na superfície de renderização. Se o valor de profundidade do polígono nesse ponto for maior, o próximo polígono na lista é testado. Esse processo está ilustrado no diagrama a seguir.

![Diagrama de teste de valores de profundidade](images/zbuffer.png)

> [!Note]  
> Embora a maioria dos aplicativos não use esse recurso, você pode alterar a comparação que o Direct3D usa para determinar quais valores são colocados no buffer de profundidade e, posteriormente, na superfície de destino de renderização. Para fazer isso, altere o valor para o \_ estado de RENDERIZAÇÃO D3DRS ZFUNC. Em alguns itens de hardware, alterar a função de comparação pode desabilitar o teste z hierárquico.

 

Praticamente todos os aceleradores do mercado são compatíveis com o buffer z, o que o transforma no tipo mais comum de buffer de profundidade hoje. Mesmo onipresentes, os buffers z têm suas desvantagens. Devido à matemática envolvida, os valores z gerados em um buffer z tendem a não ser distribuídos uniformemente no intervalo do buffer z (normalmente 0,0 a 1,0, inclusive). Especificamente, a razão entre os planos de recorte distante e próximo afeta intensamente quanto os valores de z são distribuídos irregularmente. Usando uma razão de distância do plano distante para o plano próximo de 100, 90% do intervalo do buffer de profundidade são gastos nos primeiros 10% do intervalo de profundidade da cena. Os aplicativos típicos para diversão ou simulações visuais com cenas exteriores geralmente exigem razões de plano distante/plano próximo em algum ponto entre 1.000 e 10.000. Em uma razão de 1.000, 98% do intervalo são gastos nos primeiros 2% do intervalo de profundidade, e a distribuição fica pior com razões maiores. Isso pode causar artefatos de superfície ocultos em objetos distantes, especialmente ao usar buffers de profundidade de 16 bits, a profundidade de bits mais comumente compatível.

Um buffer de profundidade com base w, por outro lado, costuma ser distribuído mais uniformemente entre os planos de recorte próximo e distante do que um buffer z. O principal benefício é que a razão de distâncias para os planos de recorte distante e próximo não é mais um problema. Isso permite que os aplicativos sejam compatíveis com intervalos máximos grandes, ao mesmo tempo que ainda obtêm buffer de profundidade relativamente preciso perto do ponto ocular. Um buffer de profundidade com base w não é perfeito e, às vezes, pode apresentar artefatos de superfície ocultos para objetos próximos. Outra desvantagem na abordagem de buffer w está relacionada ao suporte de hardware: o buffer w não é tão amplamente compatível com itens de hardware como o buffer z.

O uso de um buffer z requer sobrecarga durante a renderização. Várias técnicas podem ser usadas para otimizar a renderização ao usar buffers z. Para obter detalhes, consulte [Z-buffer performance](performance-optimizations.md).

> [!Note]  
> A interpretação real de um valor de profundidade é específica para o renderizador.

 

Esta seção apresenta informações sobre como usar buffers de profundidade para a remoção da linha oculta e da superfície oculta.

-   [Consulta de suporte de buffer de profundidade (Direct3D 9)](querying-for-depth-buffer-support.md)
-   [Criando um buffer de profundidade (Direct3D 9)](creating-a-depth-buffer.md)
-   [Habilitando o buffer de profundidade (Direct3D 9)](enabling-depth-buffering.md)
-   [Recuperando um buffer de profundidade (Direct3D 9)](retrieving-a-depth-buffer.md)
-   [Limpando buffers de profundidade (Direct3D 9)](clearing-depth-buffers.md)
-   [Alteração do acesso de gravação do buffer de profundidade (Direct3D 9)](changing-depth-buffer-write-access.md)
-   [Alterando funções de comparação de buffer de profundidade (Direct3D 9)](changing-depth-buffer-comparison-functions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



