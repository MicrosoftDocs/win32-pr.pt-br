---
title: store_uav_typed (sm5 – asm)
description: Gravação de acesso aleatório de um elemento em uma UAV (exibição de acesso não ordem) digitada.
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc190662ebab4629c92bba8fafbe75fe23704f8543c7eb9ceba53b9ab02b1029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508236"
---
# <a name="store_uav_typed-sm5---asm"></a>store \_ uav \_ digitado (sm5 - asm)

Gravação de acesso aleatório de um elemento em uma UAV (exibição de acesso não ordem) digitada.



| store \_ uav \_ typed dstUAV.xyzw, dstAddress \[ .swizzle, \] src0 \[ .swizzle\] |
|-------------------------------------------------------------------------|



 



| Item                                                                                                           | Descrição                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                 | \[em \] Contém o resultado da operação.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[em \] O endereço no qual gravar.<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[em \] Os componentes a gravar.<br/>              |



 

## <a name="remarks"></a>Comentários

Essa instrução executa um elemento de 4 componentes de 32 bits escrito de \* *src0* para *dstUAV* no endereço *em dstAddress*. *dstUAV* é um UAV digitado (u \# ).

O formato da UAV determina a conversão de formato.

O número de componentes inteiros sem sinal de 32 bits retirados do endereço é determinado pela dimensionalidade do recurso declarado em *dstUAV*. Esse endereço está em elementos .

Endereçamento fora dos limites significa que nada é gravado na memória.

*dstUAV* sempre tem uma máscara de gravação .xyzw. Todos os componentes devem ser gravados.

É inválido e indefinido usar essa instrução em um UAV que não é declarado como digitado. Ou seja, fazer isso em um UAV estruturado ou sem tipo é inválido.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Como os UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11.1, essa instrução se aplica a todos os estágios do sombreador para o runtime do Direct3D 11.1, que está disponível a partir do Windows 8.



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



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





