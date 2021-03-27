---
title: dcl_uav_raw (SM5-ASM)
description: Declare um UAV (modo de exibição de acesso não ordenado) para uso por um sombreador. | dcl_uav_raw (SM5-ASM)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f47614d5a9327f2d686a36db6bfe4afeb653788
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989176"
---
# <a name="dcl_uav_raw-sm5---asm"></a>DCL \_ UAV \_ bruto (SM5-ASM)

Declare um UAV (modo de exibição de acesso não ordenado) para uso por um sombreador.



| DCL \_ UAV \_ RAW \[ \_ GLC \] dstUAV |
|-------------------------------|



 



| Item                                                                                           | Descrição                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[no \] UAV.<br/> |



 

## <a name="remarks"></a>Comentários

*dstUAV* é um \# registro u declarado como uma referência a um UnorderedAccessView de um buffer, em que o buffer aparece como uma matriz 1D simples de entradas não tipadas de 32 bits.

As operações executadas na memória podem interpretar implicitamente os dados como tendo um tipo.

O \_ sinalizador GLC significa "globalmente coerente". A ausência de \_ GLC significa que o UAV está sendo declarado somente como "grupo coerente" no sombreador de computação ou "coerente localmente" em uma invocação de sombreador de pixel único.

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



 

> [!Note]  
> Essa instrução tem suporte em cs \_ 4 \_ 0 e cs \_ 4 \_ 1.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





