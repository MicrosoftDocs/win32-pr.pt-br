---
title: store_raw (SM5-ASM)
description: Gravação de acesso aleatório de 1-4 de componentes de 32 bits em memória de tipo insuficiente.
ms.assetid: D166116A-CF4E-4020-9F6A-F9CEEFCDAB21
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44b4d22a576853fb8b7d2c43fcb6a2d7fc9a448
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365275"
---
# <a name="store_raw-sm5---asm"></a>armazenamento \_ bruto (SM5-ASM)

Gravação de acesso aleatório de 1-4 de componentes de 32 bits em memória de tipo insuficiente.



| armazenar a \_ \[ máscara dst0. Write, o \_ \] componente dstByteOffset \[ . Select \_ , o \] src0 \[ . swizzle\] |
|----------------------------------------------------------------------------------------|



 



| Item                                                                                                                       | Descrição                                |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[no \] endereço de memória.<br/>      |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*<br/> | \[no \] deslocamento.<br/>              |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[nos \] componentes a serem gravados.<br/> |



 

## <a name="remarks"></a>Comentários

Esta instrução executa \* componentes de 32 bits de componente 1-4 gravados de *src0* para *Dst0* no deslocamento em *dstByteOffset*. Não há conversão de formato.

*dst0* deve ser um UAV (u \# ) ou, no sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ).

*dstByteOffset* especifica o valor de base de 32 bits na memória para uma janela de 4 valores sequenciais de 32 bits nos quais os dados podem ser gravados, dependendo do swizzle e da máscara em outros parâmetros.

O local dos dados gravados é equivalente ao pseudocódigo a seguir, que mostra o endereço, o ponteiro para o conteúdo do buffer e os dados armazenados linearmente.

``` syntax
                    BYTE *BufferContents;          // from src0
                    UINT dstByteOffset;            // source register
                    BYTE *WriteLocation;           // value to calculate

                    // calculate writing location
                    WriteLocation = BufferContents 
                                + dstByteOffset;

                    // calculate the number of components to write
                    switch (dstWriteMask)
                    {
                        x:    WriteComponents = 1; break;
                        xy:   WriteComponents = 2; break;
                        xyz:  WriteComponents = 3; break;
                        xyzw: WriteComponents = 4; break;
                        default:  // only these masks are valid                              
                    }

                    // copy the data from the source register with
                    //    the swizzle applied
                    memcpy(WriteLocation, swizzle(src0, src0.swizzle), 
                             WriteComponents * sizeof(UINT32));
```

Esse pseudocódigo mostra como a operação funciona, mas os dados reais não precisam ser armazenados linearmente. *dst0* só pode ter uma máscara de gravação que seja uma das seguintes:. x,. XY,. xyz,. xyzw. A máscara de gravação determina o número de componentes de 32 bits a serem gravados sem intervalos.

O endereçamento fora dos limites em u \# significa que nada é gravado na memória fora dos limites; qualquer parte que esteja em limites é gravada corretamente.

O endereçamento fora dos limites em g \# (os limites desse g específico \# , em oposição a toda a memória compartilhada) para qualquer componente de 32 bits determinado faz com que todo o conteúdo de toda a memória compartilhada se torne indefinido.

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução para UAV.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.



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



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





