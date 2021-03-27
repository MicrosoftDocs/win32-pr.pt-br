---
title: store_structured (SM5-ASM)
description: Gravação aleatória-acesso de componentes de 1-4 32 bits em um UAV (modo de exibição de acesso não ordenado) de buffer estruturado.
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5890d30fac57923365f0bdea89fcce55f7922c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006882"
---
# <a name="store_structured-sm5---asm"></a>armazenamento \_ estruturado (SM5-ASM)

Gravação aleatória-acesso de componentes de 1-4 32 bits em um UAV (modo de exibição de acesso não ordenado) de buffer estruturado.



| armazene a \_ \[ máscara dst0. Write \_ \] , dstAddress \[ . Select, o \_ componente \] dstByteOffset \[ . Select \_ \] , src0 \[ . swizzle\] |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                                       | Descrição                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[no \] endereço dos resultados da operação.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/>             | \[no \] endereço no qual gravar.<br/>               |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*<br/> | \[no \] índice da estrutura a ser gravada.<br/>         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[nos \] componentes a serem gravados.<br/>                     |



 

## <a name="remarks"></a>Comentários

Esta instrução executa \* componentes de 32 bits do componente de 1-4 gravados de *src0* para *Dst0* no endereço em *dstAddress* e *dstByteOffset*. Nenhuma conversão de formato.

*dst0* deve ser um UAV (u \# ). No sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ).

*dstAddress* especifica o índice da estrutura a ser gravada.

O local dos dados gravados é equivalente ao pseudocódigo a seguir, que mostra o deslocamento, o endereço, o ponteiro para o conteúdo do buffer, o stride da fonte e os dados armazenados linearmente.

``` syntax
                    BYTE *BufferContents;             // from dst0
                    UINT BufferStride;                // from dst0
                    UINT dstAddress, dstByteOffset;   // source registers
                    BYTE *WriteLocation;              // value to calculate

                    // calculate writing location
                     WriteLocation = BufferContents 
                                + BufferStride * dstAddress 
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
                             WriteComponents * sizeof(INT32));
```

Esse pseudocódigo mostra como a operação funciona, mas os dados reais não precisam ser armazenados linearmente. Se os dados não forem armazenados linearmente, a operação real da instrução precisará corresponder ao comportamento da operação acima.

*dst0* só pode ter uma máscara de gravação que seja uma das seguintes:. x,. XY,. xyz,. xyzw. A máscara de gravação determina o número de componentes de 32 bits a serem gravados sem intervalos.

O endereçamento fora dos limites em u \# casued by *dstAddress* significa que nada é gravado na memória fora dos limites.

Se o *dstByteOffset*, incluindo *dstWriteMask*, for o que faz com que os limites tenham acesso a você \# , todo o conteúdo do UAV se tornará indefinido.

O endereçamento fora dos limites em g \# (os limites desse g específico \# , em oposição a toda a memória compartilhada) para qualquer componente de 32 bits determinado faz com que todo o conteúdo de toda a memória compartilhada se torne indefinido.

*dstByteOffset* é um argumento separado de *dstAddress* porque é normalmente um literal. Essa separação de parâmetro não foi feita para Atomics na memória estruturada.

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução para UAV e TGSM.

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

 

 





