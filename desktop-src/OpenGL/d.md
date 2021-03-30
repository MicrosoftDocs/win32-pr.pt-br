---
title: D (OpenGL)
description: Definições de termos OpenGL que começam com a letra D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f97470e7-a500-47d7-84f0-b3045d04b8fc
keywords:
- depth
- advertência de profundidade
- Exibir listas
- pontilhado
- buffer duplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cb068f06135c6ba29e8a61f472d98907090a78
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644149"
---
# <a name="d-opengl"></a>D (OpenGL)

[A](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**Detalhado**
</dt> <dd>

Geralmente refere-se à coordenada de janela z.

</dd> <dt>

<span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**advertência de profundidade**
</dt> <dd>

Uma técnica de renderização que atribui cor com base na distância do ponto de vista.

</dd> <dt>

<span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**lista de exibição**
</dt> <dd>

Uma lista nomeada de comandos OpenGL. As listas de exibição são sempre armazenadas no servidor, portanto, as listas de exibição podem ser usadas para reduzir o tráfego de rede em ambientes de cliente/servidor. O conteúdo de uma lista de exibição pode ser pré-processado e, portanto, pode ser executado com mais eficiência do que o mesmo conjunto de comandos OpenGL executados no modo imediato. Esse pré-processamento é especialmente importante para a computação de comandos intensivos, como [**glTexImage**](glteximage1d.md).

</dd> <dt>

<span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**pontilhado**
</dt> <dd>

Uma técnica para aumentar o intervalo percebido de cores em uma imagem no custo da resolução espacial. Os pixels adjacentes são atribuídos a valores de cor diferentes. Quando visualizados de uma distância, essas cores parecem misturar em uma única cor intermediária. A técnica é semelhante ao meio-Toning usado em publicações em preto e branco para obter sombras de cinza.

</dd> <dt>

<span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**buffer duplo**
</dt> <dd>

Usando contextos OpenGL no qual os buffers de cor frontal e traseira são armazenados em buffer duplo. A animação suave é realizada pela renderização somente no buffer de fundo (que não é exibido), fazendo com que os buffers de frente e de trás sejam trocados.

</dd> </dl>

 

 




