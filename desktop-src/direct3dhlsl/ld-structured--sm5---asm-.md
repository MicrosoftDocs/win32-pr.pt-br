---
title: ld_structured (SM5-ASM)
description: Leitura de acesso aleatório de 1-4 de componentes de 32 bits de um buffer estruturado.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a34bafdcfbe0658723dd83d62507e255ff4bfa
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365249"
---
# <a name="ld_structured-sm5---asm"></a>LD \_ estruturada (SM5-ASM)

Leitura de acesso aleatório de 1-4 de componentes de 32 bits de um buffer estruturado.



| : LD \_ dst0 \[ . Mask \] , srcAddress \[ . Selecione \_ componente \] , srcByteOffset \[ . Select \_ componente \] , src0 \[ . swizzle\] |
|-------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                                       | Descrição                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[no \] endereço dos resultados da operação.<br/>                                                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>             | \[in \] especifica o índice da estrutura a ser lida.<br/>                                                                                            |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[em \] especifica o deslocamento de bytes na estrutura da qual começar a ler. <br/>                                                                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | O buffer do qual ler. Esse parâmetro deve ser um SRV (t \# ), UAV (u \# ). No sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ). <br/> |



 

## <a name="remarks"></a>Comentários

Os dados lidos da estrutura são equivalentes ao seguinte pseudocódigo: onde temos o deslocamento, o endereço, o ponteiro para o conteúdo do buffer, o stride da fonte e os dados armazenados linearmente.

``` syntax
                    BYTE *BufferContents;         // from SRV or UAV
                    UINT BufferStride;            // from base resource
                    UINT srcAddress, srcByteOffset;   // from source registers
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + BufferStride * srcByteOffset
                                + srcOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

Esse pseudocódigo mostra como a operação funciona, mas os dados reais não precisam ser armazenados linearmente. Se os dados não forem armazenados linearmente, a operação real da instrução precisará corresponder ao comportamento da operação acima.

O endereçamento fora dos limites em u \# /t \# de qualquer componente de 32 bits especificado retorna 0 para esse componente, exceto *se srcByteOffset*, além de swizzle for o que faz com que o acesso a você/t seja \# \# indefinido, o valor retornado para todos os componentes é indefinida.

O endereçamento fora dos limites em g \# (os limites desse g específico \# , em oposição a toda a memória compartilhada) para qualquer componente de 32 bits determinado retorna um resultado indefinido.

*srcByteOffset* é um argumento separado de *srcAddress* porque é normalmente um literal. Essa separação de parâmetro não foi feita para Atomics na memória estruturada.

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução para UAV, SRV e TGSM.

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



 

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução para UAV, SRV e TGSM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





