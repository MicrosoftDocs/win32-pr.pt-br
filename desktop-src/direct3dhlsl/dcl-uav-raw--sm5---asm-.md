---
title: dcl_uav_raw (sm5 – asm)
description: Declare uma UAV (exibição de acesso não organizado) para uso por um sombreador. | dcl_uav_raw (sm5 – asm)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b7af99a1747d23d6269ffc1b7199fb142277b46e73bfd822d31fd4b0fbf3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986686"
---
# <a name="dcl_uav_raw-sm5---asm"></a>dcl \_ uav \_ raw (sm5 - asm)

Declare uma UAV (exibição de acesso não organizado) para uso por um sombreador.



| dcl \_ uav \_ raw \[ \_ glc \] dstUAV |
|-------------------------------|



 



| Item                                                                                           | Descrição                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[no \] UAV.<br/> |



 

## <a name="remarks"></a>Comentários

*dstUAV* é um registro u declarado como uma referência a um UnorderedAccessView de um Buffer, em que o buffer aparece como uma matriz 1D simples de entradas sem tipo de \# 32 bits.

As operações executadas na memória podem interpretar implicitamente os dados como tendo um tipo.

O \_ sinalizador glc significa "globalmente coerente". A ausência de glc significa que o UAV está sendo declarado apenas como "coerente de grupo" no sombreador de computação ou "localmente coerente" em uma invocação de sombreador de \_ pixel único.

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



 

> [!Note]  
> Essa instrução tem suporte nos cs \_ 4 \_ 0 e cs \_ 4 \_ 1.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





