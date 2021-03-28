---
title: store_uav_typed (SM5-ASM)
description: Gravação aleatória-acesso de um elemento em uma exibição de acesso não ordenado tipado (UAV).
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6243e6fbb2092bac699dbbce04cb3c3478880866
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006878"
---
# <a name="store_uav_typed-sm5---asm"></a>armazenar \_ UAV \_ tipados (SM5-ASM)

Gravação aleatória-acesso de um elemento em uma exibição de acesso não ordenado tipado (UAV).



| Store \_ UAV \_ tipada dstUAV. Xyzw, dstAddress \[ . swizzle \] , src0 \[ . swizzle\] |
|-------------------------------------------------------------------------|



 



| Item                                                                                                           | Descrição                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                 | \[in \] contém o resultado da operação.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[no \] endereço no qual gravar.<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[nos \] componentes a serem gravados.<br/>              |



 

## <a name="remarks"></a>Comentários

Essa instrução executa um elemento de 4 componentes de \* 32 bits gravado de *Src0* para *DstUAV* no endereço em *dstAddress*. *dstUAV* é um UAV tipado (u \# ).

O formato de UAV determina a conversão de formato.

O número de componentes inteiros sem sinal de 32 bits obtidos do endereço são determinados pela dimensionalidade do recurso declarado em *dstUAV*. Esse endereço está em elementos.

O endereçamento fora dos limites significa que nada é gravado na memória.

*dstUAV* sempre tem uma máscara de gravação. xyzw. Todos os componentes devem ser gravados.

Ele é inválido e não está definido para usar essa instrução em um UAV que não seja declarado como tipado. Ou seja, fazer isso em um UAV estruturado ou de tipo não é válido.

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

 

 





