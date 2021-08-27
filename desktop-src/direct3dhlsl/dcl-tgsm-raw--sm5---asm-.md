---
title: dcl_tgsm_raw (SM5-ASM)
description: Declare uma referência a uma região de espaço de memória compartilhada disponível para o grupo de threads do sombreador de computação.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0945cde7719129ca43368e50258c02727103209b8d467932e79acd1e1150c89f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024686"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a>DCL \_ tgsm \_ bruto (SM5-ASM)

Declare uma referência a uma região de espaço de memória compartilhada disponível para o grupo de threads do sombreador de computação.



| DCL \_ tgsm \_ bruto g \# , byteCount |
|-------------------------------|



 



| Item                                                                                                       | Descrição                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*m\#*<br/>                                                 | \[em \] uma referência a um bloco de tamanho *byteCount* de memória compartilhada não tipada. <br/> |
| <span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*<br/> | \[in \] deve ser um múltiplo de 4. <br/>                                             |



 

## <a name="remarks"></a>Comentários

O armazenamento total para todos os g \# deve ser <= a quantidade de memória compartilhada disponível por grupo de threads, que é 32 KB.

Em um caso extremo, você pode declarar o total de 8192 g \# s, cada um com um *byteCount* de 4.

No lado oposto, você pode declarar um g único \# com um *byteCount* de 32768.

> [!Note]  
> o cs \_ 4 \_ 0 e o cs \_ 4 \_ 1 dão suporte ao [ \_ tgsm DCL \_ estruturado](dcl-tgsm-structured--sm5---asm-.md), mas não ao **DCL \_ tgsm \_ RAW**.

 

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 





