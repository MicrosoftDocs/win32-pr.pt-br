---
title: C (OpenGL)
description: Definições de termos openGL que começam com a letra C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- computadores cliente
- memória do cliente
- coordenadas de clipe
- recorte
- índice de cores
- modo de índice de cores
- mapas de cores
- components
- contextos
- Convexo
- forma convexa
- sistema de coordenadas
- Abate
- matriz atual
- posição de raster atual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39007e4719e1f4507555bf5aafa3187a897756d1d33580e9facc8fa0f6d8fa3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675986"
---
# <a name="c-opengl"></a>C (OpenGL)

[A](a.md) [B](b.md) C [D](d.md) [E](e.md) F [G](f.md) [](g.md) [H](h.md) [I](i.md) [J K](jk.md) L [M](l.md) [](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) U [V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**computador cliente**
</dt> <dd>

O computador do qual os comandos OpenGL são emitidos. O computador que emite comandos OpenGL pode ser conectado por meio de uma rede a um computador diferente que executa os comandos ou comandos podem ser emitidos e executados no mesmo computador. Consulte também [servidor](s.md).

</dd> <dt>

<span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**memória do cliente**
</dt> <dd>

A memória principal (em que as variáveis de programa são armazenadas) do computador cliente.

</dd> <dt>

<span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**coordenadas de clipe**
</dt> <dd>

O sistema de coordenadas que segue a transformação pela matriz de projeção e precede a divisão de perspectiva. O recorte de volume de exibição é feito em coordenadas de recorte, mas o recorte específico do aplicativo não é. Consulte também recorte [específico do aplicativo.](a.md)

</dd> <dt>

<span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**Recorte**
</dt> <dd>

Eliminando a parte de um primitivo geométrico que está fora do meio espaço definido por um plano de recorte. Os pontos são simplesmente rejeitados se estão fora. A parte de uma linha ou de um polígono que está fora do meio espaço é eliminada e os vértices adicionais são gerados conforme necessário para concluir o primitivo dentro do espaço de recorte. Primitivos geométricos e a posição atual do raster (quando especificado) são sempre recortados em relação aos seis espaços de intervalo definidos pelos planos esquerdo, direito, inferior, superior, próximo e distante do volume de exibição. Os aplicativos podem especificar planos de recorte opcionais específicos do aplicativo a serem aplicados em coordenadas de olho.

</dd> <dt>

<span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**índice de cores**
</dt> <dd>

Um único valor que representa uma cor por nome, em vez de por valor. Índices de cores OpenGL são tratados como valores contínuos (por exemplo, números de ponto flutuante), enquanto operações como interpolação e dithering são executadas neles. Índices de cores armazenados no buffer de quadro são sempre valores inteiros, no entanto. Índices de ponto flutuante são convertidos em inteiros arredondando para o valor inteiro mais próximo.

</dd> <dt>

<span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**modo de índice de cores**
</dt> <dd>

Modo de um contexto OpenGL no qual seus buffers de cores armazenam índices de cores, em vez de componentes de cor vermelho, verde, azul e alfa.

</dd> <dt>

<span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**mapa de cores**
</dt> <dd>

Uma tabela de mapeamentos de índice para RGB que é acessada pelo hardware de exibição. Cada índice de cores é lido do buffer de cores, convertido em um triplo RGB por lookup no mapa de cores e enviado para o monitor.

</dd> <dt>

<span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**Componente**
</dt> <dd>

Um único valor contínuo (por exemplo, ponto flutuante) que representa uma intensidade ou quantidade. Normalmente, um valor de componente de zero representa o valor mínimo ou a intensidade e um valor de componente de um representa o valor máximo ou a intensidade, embora outras normalizações às vezes sejam usadas. Como os valores de componente são interpretados em um intervalo normalizado, eles são especificados independentemente da resolução real. Por exemplo, o triplo RGB (1, 1, 1) é branco, independentemente de os buffers de cor armazenarem 4, 8 ou 12 bits cada. Componentes fora do intervalo normalmente são fixados ao intervalo normalizado, não truncados ou interpretados de outra forma. Por exemplo, o triplo RGB (1.4, 1.5, 0,9) é fixado para (1,0, 1,0, 0,9) antes de ser usado para atualizar o buffer de cores. Vermelho, verde, azul, alfa e profundidade são sempre tratados como componentes, nunca como índices.

</dd> <dt>

<span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**Contexto**
</dt> <dd>

Um conjunto completo de variáveis de estado OpenGL. Observe que o conteúdo do framebuffer não faz parte do estado OpenGL, mas que a configuração do framebuffer é.

</dd> <dt>

<span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**Convexo**
</dt> <dd>

Condição de um polígono no qual nenhuma linha reta no plano do polígono cruza o polígono mais de duas vezes.

</dd> <dt>

<span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**convexa**
</dt> <dd>

A menor região convexa que inclui um grupo de pontos especificado. Em duas dimensões, o chassi convexa é encontrado conceitualmente alongando uma faixa de borracha em torno dos pontos para que todos os pontos se couvem dentro da faixa.

</dd> <dt>

<span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**sistema de coordenadas**
</dt> <dd>

No espaço n-dimensional, um conjunto de n vetores independentes linearmente ancorados a um ponto (denominado a origem). Um grupo de coordenadas especifica um ponto no espaçoNo espaço ndimensional, um conjunto de n vetores linearmente independentes ancorados em um ponto (chamado de origem). Um grupo de coordenadas especifica um ponto no espaço (ou um vetor da origem) indicando a distância em cada vetor para alcançar o ponto (ou a ponta do vetor). (ou um vetor da origem) indicando a distância de viagem ao longo de cada vetor para alcançar o ponto (ou a dica do vetor).

</dd> <dt>

<span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**Abate**
</dt> <dd>

O processo de eliminação de um rosto frontal ou de um polígono para que o rosto não seja desenhado.

</dd> <dt>

<span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**matriz atual**
</dt> <dd>

Uma matriz que transforma coordenadas em um sistema de coordenadas em coordenadas de outro sistema. Há três matrizes atuais no OpenGL: a matriz modelview, que transforma coordenadas de objeto (coordenadas especificadas pelo programador) em coordenadas de olho; a matriz de perspectiva, que transforma coordenadas de olho em coordenadas de corte; e a matriz de textura, que transforma as coordenadas de textura especificadas ou geradas, conforme descrito pela matriz. Cada matriz atual é o elemento superior em uma pilha de matrizes. Cada uma das três pilhas pode ser manipulada com comandos de manipulação de matriz OpenGL.

</dd> <dt>

<span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**posição de raster atual**
</dt> <dd>

Uma posição de coordenada de janela que especifica o posicionamento de uma imagem primitiva quando ela é rasterizada. A posição atual do raster e outros parâmetros de raster atuais são atualizados quando glRasterpos é chamado.

</dd> </dl>

 

 




