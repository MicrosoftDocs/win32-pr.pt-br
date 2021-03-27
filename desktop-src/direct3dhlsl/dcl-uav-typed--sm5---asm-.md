---
title: dcl_uav_typed (SM5-ASM)
description: Declare um UAV (modo de exibição de acesso não ordenado) para uso por um sombreador. | dcl_uav_typed (SM5-ASM)
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b789714c7ec825620b73e387fa8a4dd73e1a590d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989252"
---
# <a name="dcl_uav_typed-sm5---asm"></a>DCL \_ UAV \_ tipado (SM5-ASM)

Declare um UAV (modo de exibição de acesso não ordenado) para uso por um sombreador.



| DCL \_ UAV \_ digitou \[ \_ GLC \] dstUAV, Dimension, Type |
|--------------------------------------------------|



 



| Item                                                                                           | Descrição                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[no \] UAV.<br/>                                                                        |
| <span id="dimension"></span><span id="DIMENSION"></span>*dimensões*<br/>                 | \[em \] especifica quantas dimensões as instruções que acessam o UAV estão fornecendo.<br/> |
| <span id="type"></span><span id="TYPE"></span>*Escreva*<br/>                                | \[no \] tipo de UAV.<br/>                                                            |



 

## <a name="remarks"></a>Comentários

*dstUAV* é um \# registro u sendo declarado como uma referência a um UnorderedAccessView que deve ser associado ao slot UAV \# na API.

A dimensão deve ser buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray ou Texture3D. Isso indica quantas dimensões todas as instruções que acessam o UAV estão fornecendo: 1 (Texture1D, buffer), 2 (Texture1DArray, Texture2D) ou 3 (Texture2DArray, Texture3D).

O tipo é {UNORM, SNORM, UINT, Santo, FLOAT}. As operações feitas com o u declarado \# devem ser compatíveis com o tipo declarado aqui e o UAV associado ao slot \# também deve ter o mesmo tipo.

O \_ sinalizador GLC significa "globalmente coerente". A ausência de \_ GLC significa que o UAV está sendo declarado somente como "grupo coerente" no sombreador de computação ou "coerente localmente" em uma invocação de sombreador de pixel único.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

> [!Note]  
> Não há suporte para essa instrução no sombreador de computação 4. x.

 

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

 

 





