---
title: ld_raw (SM5-ASM)
description: Leitura aleatória-acesso de componentes de 1-4 32 bits de um buffer bruto.
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4a9480ef60098b394e0eff2b06043fd9a32e45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967112"
---
# <a name="ld_raw-sm5---asm"></a>LD \_ bruto (SM5-ASM)

Leitura aleatória-acesso de componentes de 1-4 32 bits de um buffer bruto.



| LD \_ dst0 \[ . Mask \] , srcByteOffset \[ . Select bruto \_ \] , src0 \[ . swizzle\] |
|------------------------------------------------------------------------------|



 



| Item                                                                                                                       | Descrição                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[no \] endereço do resultado da operação.<br/> |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[em \] especifica o deslocamento do qual ler.<br/>          |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[no \] componente a ser lido. <br/>                     |



 

## <a name="remarks"></a>Comentários

*src0* deve ser:

-   Qualquer estágio do sombreador: SRV (t \# ) LD St
-   Sombreador de computação ou sombreador de pixel: UAV (u \# )
-   Sombreador de computação: memória compartilhada do grupo de threads (g \# )

*srcByteOffset* especifica o valor de base de 32 bits na memória para uma janela de 4 valores sequenciais de 32 bits nos quais os dados podem ser lidos, dependendo do swizzle e da máscara em outros parâmetros.

Os dados lidos do buffer bruto são equivalentes ao seguinte pseudocódigo: onde temos o deslocamento, o endereço, o ponteiro para o conteúdo do buffer, o stride da origem e os dados armazenados linearmente.

``` syntax
                    BYTE *BufferContents;         // from src0
                    UINT srcByteOffset;           // from srcRegister
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + srcByteOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

O endereçamento fora dos limites em u \# /t \# de qualquer componente de 32 bits especificado retorna 0 para esse componente.

O endereçamento fora dos limites em g \# (os limites desse g específico \# , em oposição a toda a memória compartilhada) para qualquer componente de 32 bits determinado retorna um resultado indefinido.

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução para UAV e SRV.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

Como UAVs estão disponíveis em todos os estágios de sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios de sombreador para UAVs para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.



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

 

 





