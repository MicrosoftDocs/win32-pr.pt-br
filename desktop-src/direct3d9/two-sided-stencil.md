---
description: Os volumes de sombra são usados para desenhar sombras com o buffer de estêncil.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Estêncil de Two-Sided (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b238c4b778b9894029764032e76b60c476a891a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105798524"
---
# <a name="two-sided-stencil-direct3d-9"></a>Estêncil de Two-Sided (Direct3D 9)

Os volumes de sombra são usados para desenhar sombras com o buffer de estêncil. O app calcula os volumes de sombra convertidos sobrepondo a geometria, calculando as bordas da silhueta e afastando-as da luz em um conjunto de volumes 3D. Em seguida, esses volumes são renderizados duas vezes no buffer de estêncil.

A primeira renderização desenha polígonos voltados para frente e aumenta os valores de buffer de estêncil. A segunda renderização desenha polígonos voltados para trás do volume de sombra e diminui os valores de buffer de estêncil. Normalmente, todos os valores incrementados e decrementados cancelam um ao outro. No entanto, a cena já foi renderizada com geometria normal, fazendo com que alguns pixels falhem no teste de buffer z, conforme o volume de sombra é renderizado. Os valores restantes no buffer de estêncil correspondem aos pixels que estão na sombra. Esse conteúdo restante do buffer de estêncil é usado como uma máscara, para fazer a combinação alfa de um quadrupleto preto grande e abrangente na cena. Com o buffer de estêncil atuando como uma máscara, o resultado será o escurecimento dos pixels que estão nas sombras.

Isso significa que a geometria de sombra é desenhada duas vezes por fonte de luz, exercendo assim pressão sobre a taxa de transferência de vértice da GPU. O recurso de estêncil de dois lados foi projetado para atenuar essa situação. Nesta abordagem, existem dois conjuntos de estado de estêncil (nomeados abaixo), um conjunto para os triângulos voltados para a frente e outro para os triângulos voltados para trás. Dessa forma, somente uma única passagem é desenhada por volume de sombra, por luz.

As alterações de API são restritas a um novo conjunto de Estados de renderização. O novo estado de renderização D3DRS \_ dois \_ estênceis do lado \_ pode ser definido como **verdadeiro** ou **falso**. Ele é **false** por padrão, o que significa o comportamento atual (DirectX 8). Quando definido como **true** (funcionará somente se D3DSTENCILCAPS \_ TWOSIDED for definido), os seguintes Estados de renderização serão aplicados somente aos triângulos (no sentido horário) da frente.



| Estado de renderização        | Descrição                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| D3DRS \_ STENCILFAIL  | D3DSTENCILOP para fazer se o teste de estêncil falhar.                                                |
| D3DRS \_ STENCILZFAIL | D3DSTENCILOP a fazer se o teste de estêncil passar e o teste de z falhar.                              |
| D3DRS \_ STENCILPASS  | D3DSTENCILOP para fazer se os testes de estêncil e z forem aprovados.                                     |
| D3DRS \_ STENCILFUNC  | D3DCMPFUNC FN. O teste de estêncil passa se ((ref & Mask) stencilfn (estêncil & Mask)) é true. |



 

Um novo conjunto de Estados de renderização se aplica aos triângulos de volta (sentido anti-horário).



| Estado de renderização             | Descrição                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| D3DRS \_ CCW \_ STENCILFAIL  | D3DSTENCILOP para fazer se o teste de estêncil falhar.                                                      |
| D3DRS \_ CCW \_ STENCILZFAIL | D3DSTENCILOP a fazer se o teste de estêncil passar e o teste de z falhar.                                    |
| D3DRS \_ CCW \_ STENCILPASS  | D3DSTENCILOP para fazer se os testes de estêncil e z forem aprovados.                                           |
| D3DRS \_ CCW \_ STENCILFUNC  | Função D3DCMPFUNC. O teste de estêncil passa se ((ref & Mask) stencilfn (estêncil & Mask)) é true. |



 

Os Estados de renderização de estêncil restantes sempre se aplicam aos triângulos no sentido horário e anti-horário.

O D3DRS de \_ dois \_ lados laterais \_ é ignorado para linhas e sprites de ponto, o que significa que o comportamento não é alterado do DirectX 8. Os \_ Estados de renderização do estêncil CCW D3DRS \_ \* são ignorados.

Um novo bit de extremidade indica se o dispositivo dá suporte a esse recurso. Espera-se que os drivers que não dão suporte a esse recurso ignorem esses novos Estados de renderização. Todos os outros bits de extremidade do estêncil se aplicam aos dois modos de buffer de estêncil. Como dois \_ estênceis laterais \_ implica a capacidade de desenhar com D3DCULLMODE \_ None definido, a Cap correspondente deve ser definida pelo driver se ele der suporte a esse novo modo de estêncil. O Microsoft Windows Hardware Quality Labs (WHQL) deve impor isso.

Novos Estados de renderização:


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

 

 
