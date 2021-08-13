---
title: texld-ps_1_4
description: Carrega o registro de destino com dados de cores (RGBA) amostrados usando o conteúdo do registro de origem como coordenadas de textura. A textura amostrada é a textura associada ao número de registro de destino.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc940379c8910b45d3dcb476054cf4362a6a96bc2c5df784c8ed5ca815a093fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505800"
---
# <a name="texld---ps_1_4"></a>texld-PS \_ 1 \_ 4

Carrega o registro de destino com dados de cores (RGBA) amostrados usando o conteúdo do registro de origem como coordenadas de textura. A textura amostrada é a textura associada ao número de registro de destino.



| texld DST, src |
|----------------|



 

## <a name="registers"></a>Registros



| Valor         | Descrição                     | vn        | Hong  | TN  | RN  | Versão do sombreador de pixel              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| dst      | Registro de destino |           |     |     | x   | 1\_4         |
| src      | Registro de origem      |           |     | x   |     | 1 \_ 4 fase 1 |
|          |                      |           |     | x   | x   | \_fase 1 4   |



 

Ao usar r (n) como um registro de origem, os três primeiros componentes (XYZ) devem ter sido inicializados na fase anterior do sombreador.

Para saber mais sobre os registros, consulte [PS \_ 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Comentários

Esta instrução amostra a textura no estágio de textura associado ao número de registro de destino. A textura é amostrada usando dados de coordenadas de textura do registro de origem.

A sintaxe das instruções texld e texcrd expõe o suporte para uma divisão projetada com um modificador de registro de textura. Para o sombreador de pixel versão 1,4, o \_ sinalizador de transformação de textura projetada D3DTTFF é sempre ignorado.

Regras para usar texld:

1.  O mesmo modificador. xyz ou. xyw deve ser aplicado a cada leitura de um t (n) registro individual em ambas as instruções texcrd ou texld. Se. xyw estiver sendo usado nas leituras de registro t (n), isso poderá ser misturado com outras leituras do mesmo registro t (n) usando. xyw \_ DW.
2.  O \_ modificador de origem DZ só é válido em texld com o registro de origem r (n) (portanto, fase 2 somente).
3.  O \_ modificador de origem DZ pode ser usado não mais do que duas vezes por sombreador.



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texld                 |      |      |      | x    |      |      |       |      |       |



 

## <a name="examples"></a>Exemplos

A instrução texld oferece algum controle sobre quais componentes dos dados de coordenadas de textura de origem são usados. O conjunto completo de sintaxe permitida para texld segue e inclui todos os modificadores de registro de origem válidos, seletores e combinações de máscara de gravação.


```
texld  r(m), t(n).xyz
// Uses xyz from t(n) to sample 1D, 2D, or 3D texture
```




```
texld  r(m), t(n)
// Same as previous
```




```
texld  r(m), t(n).xyw
// Uses xyw (skipping z) from t(n) to sample 1D, 2D or 3D texture
```




```
texld  r(m), t(n)_dw.xyw  
// Samples 1D or 2D texture at x/w, y/w from t(n). The result
// is undefined for a cube-map lookup.
```




```
texld  r(m), r(n).xyz
// Samples 1D, 2D, or 3D texture at xyz from r(m) 
// This is possible in the second phase of the shader
```




```
texld  r(m), r(n)
// Same as previous
```




```
texld  r(m), r(n)_dz.xyz
// Samples 1D or 2D texture at x/z, y/z from r(m)
// Possible only in second phase
// The result is undefined for a cube-map lookup
```




```
texld  r(n), r(n)_dz
// Same as previous
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




