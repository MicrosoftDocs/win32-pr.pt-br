---
title: texcrd-PS
description: Copia dados de coordenadas de textura do iterador de coordenadas de origem registrar como dados de cores no registro de destino.
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1b7bda7ab06c4af43eaa40393d2c5d64b09d9f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988663"
---
# <a name="texcrd---ps"></a>texcrd-PS

Copia dados de coordenadas de textura do iterador de coordenadas de origem registrar como dados de cores no registro de destino.

## <a name="syntax"></a>Syntax



| texcrd DST, src |
|-----------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcrd                |      |      |      | x    |      |      |       |      |       |



 

Essa instrução interpreta os dados de coordenadas como dados de cores (RGBA).

Nenhuma textura é amostrada por essa instrução. Somente as coordenadas de textura definidas neste estágio de textura são relevantes.

Ao usar o texcrd, tenha em mente os detalhes a seguir sobre como os dados são copiados do registro de origem para o registro de destino. O registro de coordenadas de textura de origem (t \# ) contém dados no intervalo \[ -D3DCAPS9. MaxTextureRepeat, D3DCAPS9. MaxTextureRepeat \] , enquanto o registro de destino (r \# ) pode armazenar dados somente no intervalo (provavelmente menor) \[ -D3DCAPS9. PixelShader1xMaxValue, D3DCAPS9. PixelShader1xMaxValue \] . Observe que para o sombreador de pixel versão 1 \_ 4, D3DCAPS9. PixelShader1xMaxValue deve ser um mínimo de oito. A instrução texcrd, no processo de dados de origem fixação MSS que está fora do alcance do registro de destino, provavelmente se comportará de forma diferente em um hardware diferente. O primeiro pixel shader versão 1 \_ 4 hardware no mercado executará um fixe especial para valores fora do intervalo. Esse fixe foi projetado para produzir um número que possa se ajustar ao registro de destino, mas também para preservar o comportamento de endereçamento de textura para dados fora do intervalo (consulte [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) se os dados forem usados posteriormente para amostragem de textura. No entanto, um novo hardware de fabricantes diferentes pode não apresentar esse comportamento e pode apenas Chop dados para se ajustarem ao intervalo de registro de destino. Portanto, o curso de ação mais seguro ao usar o sombreador de pixel versão 1 \_ 4 texcrd é fornecer dados de coordenadas de textura apenas para o sombreador de pixel que já está dentro do intervalo \[ de 8, oito \] para que você não confie na maneira como o hardware coloca.

Ao contrário \_ de texcoord, texcrd não fixe valores entre 0 e 1.

Regras para usar texcrd:

1.  O mesmo modificador. xyz ou. xyw deve ser aplicado a todas as leituras de um registro t (n) individual em uma instrução texcrd ou texld.
2.  O quarto resultado de canal de texcrd é undefined/indefinido em todos os casos.
3.  O terceiro canal é desdefinido/indefinida para o \_ caso xyw DW.

## <a name="examples"></a>Exemplos

O conjunto completo de sintaxe permitida para texcrd, levando em conta todas as combinações válidas de modificador de origem/seletor e máscara de gravação de destino, é mostrada abaixo. Observe que a notação. RGBA e. xyzw pode ser usada de forma intercambiável.

Copia os três primeiros canais do registro do iterador de coordenadas de textura, t (n), em r (m). O quarto canal de r (m) não foi inicializado.


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



Coloca o primeiro, o segundo e o quarto componente de t (n) nos três primeiros canais de r (m). O quarto canal de r (m) não foi inicializado.


```
texcrd  r(m).rgb, t(n).xyw
```



Aqui está um exemplo de divisão projetada usando o \_ modificador de DW.

Este exemplo copia x/w e y/w de t (n) para os dois primeiros canais de r (m). O terceiro e o quarto canais de r (m) não são inicializados. Todos os dados gravados anteriormente no terceiro canal de r (m) serão perdidos. Os dados no quarto canal de r (m) são perdidos devido ao marcador de fase. Para a versão 1 \_ 4, o \_ sinalizador projetado D3DTTFF é ignorado.


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 