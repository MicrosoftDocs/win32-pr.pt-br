---
title: ld_raw (sm5 – asm)
description: Leitura de acesso aleatório de componentes de 1 a 4 de 32bits de um buffer bruto.
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85fd8ec84b574d506a02812b20f4728e3f7a996ec76ad8569645d4c1643b0ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511086"
---
# <a name="ld_raw-sm5---asm"></a>ld \_ raw (sm5 - asm)

Leitura de acesso aleatório de componentes de 1 a 4 de 32bits de um buffer bruto.



| ld \_ raw dst0 \[ .mask , \] srcByteOffset \[ componente .select , \_ \] src0 \[ .swizzle\] |
|------------------------------------------------------------------------------|



 



| Item                                                                                                                       | Descrição                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[em \] O endereço do resultado da operação.<br/> |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[em \] Especifica o deslocamento a ser lido.<br/>          |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[em \] O componente a ser lido. <br/>                     |



 

## <a name="remarks"></a>Comentários

*src0* deve ser:

-   Qualquer estágio do sombreador: SRV (t \# )ld st
-   Sombreador de computação ou sombreador de pixel: UAV (u \# )
-   Sombreador de computação: memória compartilhada do grupo de threads (g \# )

*srcByteOffset* especifica o valor base de 32 bits na memória para uma janela de 4 valores sequenciais de 32 bits em que os dados podem ser lidos, dependendo do swizzle e da máscara em outros parâmetros.

Os dados lidos do buffer bruto são equivalentes ao seguinte pseudocódigo: em que temos o deslocamento, o endereço, o ponteiro para o conteúdo do buffer, o passo a passo da origem e os dados armazenados linearmente.

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

Fora dos limites endereçamento em u /t de qualquer componente \# \# de 32 bits determinado retorna 0 para esse componente.

O endereçamento fora dos limites em g (os limites desse g específico, em vez de toda a memória compartilhada) para qualquer componente de 32 bits específico retorna um resultado \# \# indefinido.

Cs \_ 4 \_ 0 e cs \_ 4 \_ 1 são suporte a essa instrução para UAV e SRV.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

Como os UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11.1, essa instrução se aplica a todos os estágios do sombreador para UAVs para o runtime do Direct3D 11.1, que está disponível a partir do Windows 8.



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

Cs \_ 4 \_ 0 e cs \_ 4 \_ 1 são suporte a essa instrução para UAV e SRV.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





