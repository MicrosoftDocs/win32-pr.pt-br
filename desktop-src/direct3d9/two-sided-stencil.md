---
description: Os volumes de sombra são usados para desenhar sombras com o buffer de estêncil.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Two-Sided estêncil (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bca0b960f96d1747b2b7ad51771276df2cfe1da1fa8ac9aa4d7c1ce8ea7c03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290506"
---
# <a name="two-sided-stencil-direct3d-9"></a>Two-Sided estêncil (Direct3D 9)

Os volumes de sombra são usados para desenhar sombras com o buffer de estêncil. O app calcula os volumes de sombra convertidos sobrepondo a geometria, calculando as bordas da silhueta e afastando-as da luz em um conjunto de volumes 3D. Em seguida, esses volumes são renderizados duas vezes no buffer de estêncil.

A primeira renderização desenha polígonos voltados para frente e aumenta os valores de buffer de estêncil. A segunda renderização desenha polígonos voltados para trás do volume de sombra e diminui os valores de buffer de estêncil. Normalmente, todos os valores incrementados e decrementados cancelam um ao outro. No entanto, a cena já foi renderizada com geometria normal, fazendo com que alguns pixels falhem no teste de buffer z, conforme o volume de sombra é renderizado. Os valores restantes no buffer de estêncil correspondem aos pixels que estão na sombra. Esse conteúdo restante do buffer de estêncil é usado como uma máscara, para fazer a combinação alfa de um quadrupleto preto grande e abrangente na cena. Com o buffer de estêncil atuando como uma máscara, o resultado será o escurecimento dos pixels que estão nas sombras.

Isso significa que a geometria de sombra é desenhada duas vezes por fonte de luz, exercendo assim pressão sobre a taxa de transferência de vértice da GPU. O recurso de estêncil de dois lados foi projetado para atenuar essa situação. Nesta abordagem, existem dois conjuntos de estado de estêncil (nomeados abaixo), um conjunto para os triângulos voltados para a frente e outro para os triângulos voltados para trás. Dessa forma, somente uma única passagem é desenhada por volume de sombra, por luz.

As alterações de API são restritas a um novo conjunto de estados de renderização. O novo estado de renderização D3DRS \_ Two \_ Sided \_ StencilMODE pode ser definido como **TRUE** ou **FALSE.** É **FALSE por** padrão, o que significa o comportamento atual (DirectX 8). Quando isso for definido como **TRUE** (funcionará somente se D3DSTENCILCAPS TWOSIDED estiver definido), os estados de renderização a seguir serão aplicados somente aos triângulos voltados para frente (no sentido \_ horário).



| Estado de renderização        | Descrição                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| D3DRS \_ STENCILFAIL  | D3DSTENCI LTDa para fazer se o teste de estêncil falhar.                                                |
| D3DRS \_ STENCILZFAIL | D3DSTENCI LTDa para fazer se o teste de estêncil for aprovado e z-test falhar.                              |
| D3DRS \_ STENCILPASS  | D3DSTENCI LTDa para fazer se os testes de estênceis e z são aprovados.                                     |
| D3DRS \_ STENCILFUNC  | D3DCMPFUNC fn. O teste de estêncil passa se ((ref & mask) oncilfn (estêncil & máscara)) é true. |



 

Um novo conjunto de estados de renderização se aplica aos triângulos voltados para trás (no sentido anti-horário).



| Estado de renderização             | Descrição                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| D3DRS \_ CCW \_ STENCILFAIL  | D3DSTENCI LTDa para fazer se o teste de estêncil falhar.                                                      |
| D3DRS \_ CCW \_ STENCILZFAIL | D3DSTENCI LTDa para fazer se o teste de estêncil for aprovado e z-test falhar.                                    |
| D3DRS \_ CCW \_ STENCILPASS  | D3DSTENCI LTDa para fazer se os testes de estênceis e z são aprovados.                                           |
| D3DRS \_ CCW \_ STENCILFUNC  | Função D3DCMPFUNC. O teste de estêncil é aprovado se ((ref & mask) oncilfn (estêncil & máscara)) for true. |



 

Os estados de renderização de estêncil restantes sempre se aplicam a triângulos no sentido horário e anti-horário.

D3DRS \_ Two Sided StencilMODE é ignorado para linhas e sprites de ponto, o que significa que o comportamento é inalterado \_ do \_ DirectX 8. Os estados de \_ renderização STENCIL do CCW D3DRS \_ são \* ignorados.

Um novo bit de limite indica se o dispositivo dá suporte a esse recurso. Os drivers que não têm suporte para esse recurso devem ignorar esses novos estados de renderização. Todos os outros bits de limite de estêncil se aplicam a ambos os modos de buffer de estêncil. Como o esêncil com dois lados implica a capacidade de desenhar com \_ D3DCULLMODE NONE definido, o limite correspondente deverá ser definido pelo driver se ele for compatível com esse novo modo de \_ \_ estêncil. O Microsoft Windows WHQL (Hardware Quality Labs) deve impor isso.

Novos estados de renderização:


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



Novo limite:


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Técnicas de buffer de estêncil](stencil-buffer-techniques.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
