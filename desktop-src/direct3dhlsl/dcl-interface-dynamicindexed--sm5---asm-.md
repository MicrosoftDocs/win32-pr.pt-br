---
title: dcl_interface_dynamicindexed (sm5 – asm)
description: Declarar ponteiros de tabela de funções (interfaces). | dcl_interface_dynamicindexed (sm5 – asm)
ms.assetid: 5C77EBB6-7AEC-4471-AA6E-0F6D3E215156
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4bc52dc841b2e6de3c5af9725faac2c6dc5900b95117a28f77d8bc5087248df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286048"
---
# <a name="dcl_interface_dynamicindexed-sm5---asm"></a>interface dcl \_ \_ dynamicindexed (sm5 - asm)

Declarar ponteiros de tabela de funções (interfaces).



| dcl \_ interface \_ dynamicindexed fp \# \[ arraySize \] \[ numCallSites \] = {ft , ft , \# \# ...} |
|--------------------------------------------------------------------------------------|



 



| Item                                                          | Descrição                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*Fp\#*<br/> | \[em \] Ponteiros da tabela de funções.<br/> |



 

## <a name="remarks"></a>Comentários

Cada interface precisa ser vinculada da API antes que o sombreador seja usável. A associação fornece uma referência a uma das tabelas de funções para que os slots de método possam ser preenchidos. O compilador não gerará ponteiros para objetos não marcados.

Um ponteiro de tabela de funções tem um conjunto completo de slots de método para evitar o nível extra de inderção que uma representação ponteiro para ponteiro para vtable do C++ exigiria. Isso também exigiria que esse ponteiro fosse de 5 tuplas. No modelo de emlining virtual HLSL, sempre se sabe qual variável/entrada global é usada para uma chamada para que possamos configurar tabelas por objeto raiz.

Declarações de ponteiro de função indicam quais tabelas de funções são legais de usar com elas. Isso também permite derivação de informações de correlação de método.

O primeiro \[ \] de uma declaração de interface é o tamanho da matriz. Se a indexação dinâmica for usada, a declaração indicará isso conforme mostrado. Uma matriz de ponteiros de interface também pode ser indexada estaticamente, não é necessário que matrizes de ponteiros de interface significam indexação dinâmica.

A numeração de ponteiros de interface começa em 0 para a primeira declaração e, posteriormente, leva em conta o tamanho da matriz, portanto, o primeiro ponteiro após uma matriz de quatro entradas fp0 \[ 4 1 seria \] \[ \] fp4 \[ \] \[ \] .

A segunda de uma declaração de interface é o número de sites de chamada, que deve corresponder ao número de corpos em cada tabela \[ \] referenciada na declaração.

Não há limites para quantas opções de tabela de funções (ft \# ) podem ser listadas em uma declaração de interface.

Uma determinada tabela de funções (ft \# ) pode aparecer mais de uma vez em uma ou mais declarações de interface.

### <a name="restrictions"></a>Restrições

-   O número de sites de objeto em um sombreador, que é a soma em todas as declarações *\# fp* de suas declarações arraySize, não deve ser maior que \[ \] 253. Esse número corresponde a quantos **ponteiros** podem estar presentes. O runtime impõe esse limite de 253 para manter um limite no tamanho do DDI para comunicar esses dados de ponteiro.
-   O número de sites de chamada em um sombreador, que é a soma em todas as instruções fcall do número de destinos de branch potenciais, não deve ser maior que 4096.

    Por exemplo, uma [fcall que](fcall--sm5---asm-.md) usa um índice estático para a primeira *dimensão fp \[ \] \[ \]* conta como um:

    `                       fcall fp0[0][0]         // +1`

    Uma **fcall que** usa um índice dinâmico conta como o número de elementos na matriz (primeiro \[ \] da **\_ interface dcl**):

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    Esse limite ajuda algumas implementações a ajustar facilmente tabelas de seleções de corpo da função no armazenamento constante semelhante ao buffer.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

Cs \_ 4 \_ 0 e cs \_ 4 \_ 1 são suporte a essa instrução para UAV e SRV.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





