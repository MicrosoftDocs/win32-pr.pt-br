---
title: ld_structured (sm5 – asm)
description: Leitura de acesso aleatório de componentes de 1 a 4 de 32bits de um buffer estruturado.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfb3c19b56271a02c20ff85dd71352b545843f62b3d01292e87c2edbd6384d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562306"
---
# <a name="ld_structured-sm5---asm"></a>ld \_ estruturado (sm5 – asm)

Leitura de acesso aleatório de componentes de 1 a 4 de 32bits de um buffer estruturado.



| : ld \_ structured dst0 \[ .mask \] , srcAddress \[ .select component , \_ \] srcByteOffset \[ .select component , \_ \] src0 \[ .swizzle\] |
|-------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                                       | Descrição                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[em \] O endereço dos resultados da operação.<br/>                                                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>             | \[em \] Especifica o índice da estrutura a ser lida.<br/>                                                                                            |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[em \] Especifica o deslocamento de byte na estrutura da onde começar a leitura. <br/>                                                                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | O buffer do o que ler. Esse parâmetro deve ser um SRV (t \# ), UAV (u \# ). No sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ). <br/> |



 

## <a name="remarks"></a>Comentários

Os dados lidos da estrutura são equivalentes ao seguinte pseudocódigo: em que temos o deslocamento, o endereço, o ponteiro para o conteúdo do buffer, o passo a passo da origem e os dados armazenados linearmente.

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

Esse pseudocódigo mostra como a operação funciona, mas os dados reais não devem ser armazenados linearmente. Se os dados não são armazenados linearmente, a operação real da instrução precisa corresponder ao comportamento da operação acima.

Fora dos limites endereçamento em u /t de qualquer componente de 32 bits determinado retorna 0 para esse componente, exceto se \# \# *srcByteOffset*, mais swizzle é o que causa o acesso fora dos limites a você /t , o valor retornado para todos os componentes \# \# é indefinido.

O endereçamento fora dos limites em g (os limites desse g específico, em vez de toda a memória compartilhada) para qualquer componente de 32 bits específico retorna um resultado \# \# indefinido.

*srcByteOffset* é um argumento separado de *srcAddress* porque geralmente é um literal. Essa separação de parâmetros não foi feita para atômicos na memória estruturada.

Cs 4 0 e cs 4 1 são suporte a essa instrução para \_ \_ \_ \_ UAV, SRV e TGSM.

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



 

Cs 4 0 e cs 4 1 são suporte a essa \_ \_ \_ \_ instrução para UAV, SRV e TGSM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





