---
title: dcl_interface (SM5-ASM)
description: Declare ponteiros de tabela de função (interfaces). | dcl_interface (SM5-ASM)
ms.assetid: 5A4D911E-7117-409B-8FDC-9CEC2C185C15
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61435e06d0d5b88bb82ca91f758646d7911d3bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989171"
---
# <a name="dcl_interface-sm5---asm"></a>\_interface DCL (SM5-ASM)

Declare ponteiros de tabela de função (interfaces).



| \_interface DCL FP \# \[ \] \[ numCallSites \] = {ft \# , ft \# ,...} |
|----------------------------------------------------------------------|



 



| Item                                                          | Descrição                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*FP\#*<br/> | \[nos \] ponteiros de tabela de função.<br/> |



 

## <a name="remarks"></a>Comentários

Cada interface precisa ser associada da API para que o sombreador possa ser usado. A associação fornece uma referência a uma das tabelas de função para que os slots de método possam ser preenchidos. O compilador não gerará ponteiros para objetos não referenciados.

Um ponteiro de tabela de função tem um conjunto completo de Slots de método para evitar o nível extra de indireção que uma representação de ponteiro para vtable de C++ exigiria. Isso também exigiria que esses ponteiros fossem cinco tuplas. No modelo de inalinhamento virtual do HLSL, sempre é conhecido qual variável/entrada global é usada para uma chamada para que possamos configurar tabelas por objeto raiz.

Declarações de ponteiro de função indicam quais tabelas de função são legais para usar com elas. Isso também permite a derivação de informações de correlação de método.

O primeiro \[ \] de uma declaração de interface é o tamanho da matriz. Se a indexação dinâmica for usada, a declaração indicará que, conforme mostrado. Uma matriz de ponteiros de interface também pode ser indexada estaticamente, não é necessário que as matrizes de ponteiros de interface significam indexação dinâmica.

A numeração de ponteiros de interface começa em 0 para a primeira declaração e, subsequentemente, usa o tamanho da matriz em conta, portanto, o primeiro ponteiro após uma matriz de quatro entradas FP0 \[ 4 \] \[ 1 \] seria FP4 \[ \] \[ \] .

O segundo \[ \] de uma declaração de interface é o número de sites de chamada, que deve corresponder ao número de corpos em cada tabela referenciada na declaração.

Não há limites para quantas opções de tabela de função (ft \# ) podem ser listadas em uma declaração de interface.

Uma determinada tabela de função (ft \# ) pode aparecer mais de uma vez em uma ou mais declarações de interface.

### <a name="restrictions"></a>Restrições

-   O número de sites de objeto em um sombreador, que é a soma em todas as declarações de *FP \#* de suas \[ declarações de matrizes \] , não deve ser maior que 253. Esse número corresponde a **quantos desses** ponteiros podem estar presentes. O tempo de execução impõe esse limite de 253 para manter-se ligado ao tamanho da DDI para comunicar esses dados de ponteiro.
-   O número de sites de chamada em um sombreador, que é a soma em todas as instruções fcall do número de possíveis destinos de ramificação, não deve ser maior que 4096.

    Por exemplo, um [fcall](fcall--sm5---asm-.md) que usa um índice estático para a primeira *dimensão \[ \] \[ \] FP* conta como um:

    `                       fcall fp0[0][0]         // +1`

    Um **fcall** que usa um índice dinâmico conta como o número de elementos na matriz (primeiro \[ \] da **\_ interface DCL**):

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    Esse limite ajuda algumas implementações que se ajustam facilmente a tabelas das seleções do corpo da função em armazenamento constante, como o de buffer.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução para UAV e SRV.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





