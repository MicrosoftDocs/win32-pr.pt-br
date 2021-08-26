---
title: ld_uav_typed (SM5-ASM)
description: Acesso aleatório-a leitura de um elemento de uma exibição de acesso não ordenado tipado (UAV).
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9685341f4a3a2e6b22bbbcc4b36f6ecccc153f17c67f38c390e6beeef94358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982066"
---
# <a name="ld_uav_typed-sm5---asm"></a>LD \_ UAV \_ tipada (SM5-ASM)

Acesso aleatório-a leitura de um elemento de uma exibição de acesso não ordenado tipado (UAV).



| LD \_ UAV \_ digitou dst0 \[ . Mask \] , srcAddress \[ . swizzle \] , srcUAV \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| Item                                                                                                           | Descrição                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[no \] endereço dos resultados da operação.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/> | \[em \] especifica o endereço do qual ler.<br/>          |
| <span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*<br/>                 | \[na \] origem da qual ler. <br/>                    |



 

## <a name="remarks"></a>Comentários

Essa instrução executa um elemento de 4 componentes com leitura de *srcUAV* no endereço inteiro não assinado no *srcAddress*, convertido em 32 bits por componente com base no formato e gravado em *dst0* no sombreador.

*srcUAV* é um UAV (u \# ) declarado como tipado. No entanto, o tipo de recurso associado deve ser R32 \_ uint/Santo/float.

O número de componentes inteiros sem sinal de 32 bits obtidos do endereço são determinados pela dimensionalidade do recurso declarado em *srcUAV*. O endereçamento é o mesmo que a instrução [LD](ld--sm4---asm-.md) .

O endereçamento fora dos limites é o mesmo que a instrução **LD** .

O comportamento dessa instrução é idêntico à instrução **LD** se for chamado de **LD dst0 \[ . Mask \] , srcAddress \[ . swizzle \] , srcUAV \[ . swizzle \]**

Ele é inválido e não está definido para usar essa instrução em um UAV que não seja declarado como tipado. Fazer isso em um UAV estruturado ou de tipo não é válido.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
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

 

 





