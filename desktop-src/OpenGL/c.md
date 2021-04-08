---
title: C (OpenGL)
description: Definições de termos OpenGL que começam com a letra C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- computadores cliente
- memória do cliente
- coordenadas do clipe
- recorte
- índice de cores
- modo de índice de cor
- mapas de cores
- components
- contextos
- convexa
- forma convexa
- sistema de coordenadas
- escolhidos
- matriz atual
- posição de rasterização atual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c9534052533745b1037aa80f26f435a163ee46
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008760"
---
# <a name="c-opengl"></a>C (OpenGL)

[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**computador cliente**
</dt> <dd>

O computador do qual os comandos OpenGL são emitidos. O computador que emite comandos OpenGL pode ser conectado por meio de uma rede a um computador diferente que executa os comandos, ou os comandos podem ser emitidos e executados no mesmo computador. Consulte também [servidor](s.md).

</dd> <dt>

<span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**memória do cliente**
</dt> <dd>

A memória principal (onde as variáveis do programa são armazenadas) do computador cliente.

</dd> <dt>

<span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**coordenadas do clipe**
</dt> <dd>

O sistema de coordenadas que segue a transformação pela matriz de projeção e precede a divisão em perspectiva. Exibição-o recorte de volume é feito em coordenadas de clipe, mas o recorte específico do aplicativo não é. Consulte também [recorte específico do aplicativo](a.md).

</dd> <dt>

<span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**recorte**
</dt> <dd>

Eliminar a parte de um primitivo Geométrico que está fora do meio de espaço definido por um plano de recorte. Os pontos são simplesmente rejeitados se estiverem fora do. A parte de uma linha ou de um polígono que está fora do espaço é eliminada e os vértices adicionais são gerados conforme a necessidade para concluir o primitivo dentro do espaço de recorte. Primitivos geométricos e a posição atual de rasterização (quando especificado) são sempre recortados em relação aos seis espaços de meia definição pelos planos esquerdo, direito, inferior, superior, próximo e distante do volume de exibição. Os aplicativos podem especificar planos opcionais de recorte específicos do aplicativo a serem aplicados em coordenadas de olho.

</dd> <dt>

<span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**índice de cores**
</dt> <dd>

Um único valor que representa uma cor por nome, em vez de por valor. Os índices de cores OpenGL são tratados como valores contínuos (por exemplo, números de ponto flutuante) enquanto operações como interpolação e pontilhamento são executadas neles. No entanto, os índices de cores armazenados no buffer de quadros são sempre valores inteiros. Os índices de ponto flutuante são convertidos em inteiros arredondando para o valor inteiro mais próximo.

</dd> <dt>

<span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**modo de índice de cor**
</dt> <dd>

Modo de um contexto OpenGL no qual seus buffers de cor armazenam índices de cores, em vez de componentes de cores vermelho, verde, azul e alfa.

</dd> <dt>

<span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**mapa de cores**
</dt> <dd>

Uma tabela de mapeamentos de índice para RGB que é acessada pelo hardware de vídeo. Cada índice de cor é lido do buffer de cores, convertido em um triplo RGB por pesquisa no mapa de cores e enviado ao monitor.

</dd> <dt>

<span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**componente**
</dt> <dd>

Um valor único, contínuo (por exemplo, ponto flutuante) que representa uma intensidade ou quantidade. Normalmente, um valor de componente igual a zero representa o valor mínimo ou intensidade, e um valor de componente de um representa o valor máximo ou intensidade, embora outras normalizações sejam usadas às vezes. Como os valores de componente são interpretados em um intervalo normalizado, eles são especificados independentemente da resolução real. Por exemplo, o RGB triplo (1, 1, 1) é branco, independentemente se os buffers de cor armazenam 4, 8 ou 12 bits cada. Os componentes fora do intervalo normalmente são clampeds ao intervalo normalizado, não truncado ou interpretado de outra forma. Por exemplo, o triplo RGB (1,4, 1,5, 0,9) é clamped para (1,0, 1,0, 0,9) antes de ser usado para atualizar o buffer de cores. Vermelho, verde, azul, alfa e profundidade são sempre tratados como componentes, nunca como índices.

</dd> <dt>

<span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**noticioso**
</dt> <dd>

Um conjunto completo de variáveis de estado OpenGL. Observe que o conteúdo do framebuffer não faz parte do estado do OpenGL, mas que a configuração do framebuffer é.

</dd> <dt>

<span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**convexa**
</dt> <dd>

Condição de um polígono no qual nenhuma linha reta no plano do polígono intersecciona o polígono mais de duas vezes.

</dd> <dt>

<span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**convexa envoltória**
</dt> <dd>

A menor região convexa que envolve um grupo de pontos especificado. Em duas dimensões, o convexa envoltória é encontrado conceitualmente ao esticar uma faixa de borracha ao lado dos pontos para que todos os pontos estejam dentro da banda.

</dd> <dt>

<span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**sistema de coordenadas**
</dt> <dd>

No espaço n-dimensional, um conjunto de n vetores independentes linearmente ancorados a um ponto (denominado a origem). Um grupo de coordenadas especifica um ponto no espaço n-dimensional, um conjunto de n vetores independentes lineares ancorados a um ponto (chamado de origem). Um grupo de coordenadas especifica um ponto no espaço (ou um vetor da origem) indicando a distância em cada vetor para alcançar o ponto (ou a ponta do vetor). (ou um vetor da origem), indicando a distância de viagem em cada vetor para alcançar o ponto (ou a ponta do vetor).

</dd> <dt>

<span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**escolhidos**
</dt> <dd>

O processo de eliminar uma face frontal ou um verso de um polígono para que a face não seja desenhada.

</dd> <dt>

<span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**matriz atual**
</dt> <dd>

Uma matriz que transforma coordenadas em um sistema de coordenadas para coordenadas de outro sistema. Há três matrizes atuais no OpenGL: a matriz modelview, que transforma coordenadas de objetos (coordenadas especificadas pelo programador) em coordenadas de olho; a matriz de perspectiva, que transforma as coordenadas de olho em coordenadas do clipe; e a matriz de textura, que transforma as coordenadas de textura especificadas ou geradas conforme descrito pela matriz. Cada matriz atual é o elemento superior em uma pilha de matrizes. Cada uma das três pilhas pode ser manipulada com comandos de manipulação de matriz OpenGL.

</dd> <dt>

<span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**posição de rasterização atual**
</dt> <dd>

Uma posição de coordenada de janela que especifica o posicionamento de uma imagem primitiva quando ela é rasterizada. A posição de rasterização atual e outros parâmetros de rasterização atuais são atualizados quando glRasterpos é chamado.

</dd> </dl>

 

 




